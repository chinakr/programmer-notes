# 用nginx+Puma+Mina部署Rails应用程序


## 参考资料

* [Rails笔记 > Rails应用的部署](rails-notes.md)
* [nginx笔记](../../server/nginx/nginx-notes.md)
* [Puma笔记](../../server/puma/puma-notes.md)
* [Mina笔记](../../deploy/mina/mina-notes.md)

* [自动化部署工具 Capistrano 与 Mina](http://blog.naixspirit.com/2014/12/14/cap_and_mina/ "Google关键字：mina vs capistrano 3")
* [有人有兴趣翻译 Capistrano (部署工具) 的官网文档吗？](https://ruby-china.org/topics/30147)：众多资深用户一致推荐Mina，理由是Mina的部署速度要快很多。
* [Mina项目主页](https://github.com/mina-deploy/mina)：最新版本`0.3.4`(2015-03-27)。
    + [Mina](http://nadarei.co/mina/)：一个漂亮但有点过时的网站，最新版本仅为`0.2.0`。
* [自动化部署工具 Capistrano 与 Mina](http://blog.naixspirit.com/2014/12/14/cap_and_mina/ "Google关键字：mina vs capistrano 3")：Mina 相对于 Cap 来说，较为简洁，只有基本的几个 Task(可用 mina -T 查看)，有点 Sinatra VS Rails 的感觉，其服务器部署结构与 Cap 类似。
    + 对于部署而言，工具不必像Rails这么重量级，功能太完备带来的复杂性增加了学习成本和潜在的调试成本，像Sinatra这样简洁够用的设计理念在这种情况下是非常适用的。
* [Rails 中自动布署工具 mina 的经验谈](https://ruby-china.org/topics/25529)：在敏捷开发中，如果说自动化测试是它的一条腿，自动化布署就是它的另一条腿，缺一不可。
* [Ruby on Rails 部署方案 Nginx + Mina + Puma](https://ruby-china.org/topics/26132)
* [`mina-puma`gem项目主页](https://github.com/sandelius/mina-puma)

* [用Mina-Puma-Nginx部署Rails](http://xufei.logdown.com/posts/2014/03/05/rails-mina-puma-nginx "Google关键字：puma-manager restart.txt mina")
    + `gem 'mina-puma'`
    + `require 'mina/puma'`
    + `set :shared_paths, ['log'] # 这个网上很多都加了database.yml这类数据库文件路径，不过我实际用内容为空，就删了`
        - 我也遇到了这个问题，为什么呢？
* [Deply Rails App with Puma and Nginx via Mina](https://gist.github.com/xhj/5938280 "Google关键字：nginx puma mina rails")：配置文件不完整，参考价值不大。
    + 重点看`config/puma.rb`、`config/deploy.rb`、`nginx.conf`、`/etc/puma.conf`中`sockets`目录的配置。
    + `config/deploy.rb`
        - `set :deploy_to, '/home/ubuntu/apps/xxx.com'`
        - `queue! %[mkdir -p "#{deploy_to}/shared/tmp/pids"]`
        - `queue! %[mkdir -p "#{deploy_to}/shared/tmp/sockets"]`
    + `config/puma.rb`
        - `bind "unix:///home/ubuntu/apps/esdb.cn/shared/tmp/sockets/puma.sock"`
        - `pidfile "/home/ubuntu/apps/esdb.cn/shared/tmp/pids/puma.pid"`
* [Deploying Rails application with Nginx, Puma and Mina](http://thelazylog.com/deploying-rails-application-with-nginx-puma-and-mina/ "Google关键字：nginx puma mina rails")
    + 重点看`config/puma.rb`、`config/deploy.rb`、`nginx.conf`、`/etc/puma.conf`中`sockets`目录的配置。
    + `config/deploy.rb`
        - `set :deploy_to, '/var/www/myapp'`
    + `/etc/nginx/sites-available/my_app.conf`
        - `unix:///var/www/myapp/shared/tmp/sockets/puma.sock;`
    + `config/puma.rb`
        - `bind "unix:///var/www/myapp/shared/tmp/sockets/puma.sock"`
        - `pidfile "/var/www/myapp/shared/tmp/pids/puma.pid"`
* [nginx + puma + mina](https://ruby-china.org/topics/18756 "Google关键字：nginx puma mina rails")
    + 重点看`config/puma.rb`、`config/deploy.rb`、`nginx.conf`、`/etc/puma.conf`中`sockets`目录的配置。
    + `config/deploy.rb`
        - `set :base_name, 'fmxc'`
        - `set :deploy_to, "/home/#{base_name}/app"`
    + `/etc/nginx/conf.d/fmxcdemo.tyt.com.conf`
        - `proxy_pass   http://unix:/home/fmxcdemo/app/current/tmp/puma.sock;`
    + `config/puma.rb`
        - `bind "unix:///home/#{base_name}/app/current/tmp/puma.sock?mask=0777"`
        - `pidfile "/home/#{base_name}/app/current/tmp/puma.pid"`

* [puma/lib/puma/configuration.rb](https://github.com/puma/puma/blob/master/lib/puma/configuration.rb)
    + `imp = %W(config/puma/#{@options[:environment]}.rb config/puma.rb).find { |f| File.exist?(f) }`

## 配置

### nginx的配置

    # remote server
    sudo vim /etc/nginx/sites-enabled/chejjpd

        upstream chejjpd {
            server unix:///home/deploy/pd.chejj.com.cn/chejjpd/shared/tmp/sockets/puma.sock fail_timeout=0;
        }

        server {
            listen 80;
            #server_name pd.chejj.com.cn;
            #server_name pd.haijia.net.cn pd.chejj.com.cn;
            server_name pd.haijia.net.cn;

            access_log /var/log/nginx/chejjpd.access.log;
            error_log /var/log/nginx/chejjpd.error.log info;

            location /assets/ {
                root /home/deploy/pd.chejj.com.cn/chejjpd/current/public;
            }

            location / {
                proxy_pass http://chejjpd;
            }
        }

### Puma的配置

Puma的配置分为本地和远程服务器两部分：

* 远程服务器
    + `/etc/init/puma-manager.conf`：为多个Rails应用程序启动Puma服务。(批处理，指挥官)
    + `/etc/init/puma.conf`：为指定Rails应用程序启动Puma服务。(干活主要在这里)
    + `/etc/puma.conf`：设置Rails应用程序的路径。(简单的配置文件)
* 本地
    + `Gemfile`
    + `config/puma.rb`：部署用，针对生产力环境。
    + `config/puma/development.rb`：本地测试用，针对`rails s`。

需要注意的两个问题：

1. `mina-puma`和Puma官方提供的Upstart脚本不兼容，故弃用。(否则会同时启动两个不同实例，不能按预期方式工作)
2. 需要建立`config/puma/development.rb`以便本地的`rails s`和远程服务器上的生产力环境都能正常工作。

远程服务器配置：

    # remote server
    sudo vim /etc/init/puma-manager.conf

        # /etc/init/puma-manager.conf - manage a set of Pumas

        # This example config should work with Ubuntu 12.04+.  It
        # allows you to manage multiple Puma instances with
        # Upstart, Ubuntu's native service management tool.
        #
        # See puma.conf for how to manage a single Puma instance.
        #
        # Use "stop puma-manager" to stop all Puma instances.
        # Use "start puma-manager" to start all instances.
        # Use "restart puma-manager" to restart all instances.
        # Crazy, right?
        #

        description "Manages the set of puma processes"

        # This starts upon bootup and stops on shutdown
        start on runlevel [2345]
        stop on runlevel [06]

        # Set this to the number of Puma processes you want
        # to run on this machine
        env PUMA_CONF="/etc/puma.conf"

        pre-start script
          for i in `cat $PUMA_CONF`; do
            app=`echo $i | cut -d , -f 1`
            logger -t "puma-manager" "Starting $app"
            start puma app=$app
          done
        end script

    sudo vim /etc/init/puma.conf

        # /etc/init/puma.conf - Puma config

        # This example config should work with Ubuntu 12.04+.  It
        # allows you to manage multiple Puma instances with
        # Upstart, Ubuntu's native service management tool.
        #
        # See workers.conf for how to manage all Puma instances at once.
        #
        # Save this config as /etc/init/puma.conf then manage puma with:
        #   sudo start puma app=PATH_TO_APP
        #   sudo stop puma app=PATH_TO_APP
        #   sudo status puma app=PATH_TO_APP
        #
        # or use the service command:
        #   sudo service puma {start,stop,restart,status}
        #

        description "Puma Background Worker"

        # no "start on", we don't want to automatically start
        stop on (stopping puma-manager or runlevel [06])

        # change apps to match your deployment user if you want to use this as a less privileged user (recommended!)
        setuid deploy
        setgid deploy

        respawn
        respawn limit 3 30

        instance ${app}

        script
        # this script runs in /bin/sh by default
        # respawn as bash so we can source in rbenv/rvm
        # quoted heredoc to tell /bin/sh not to interpret
        # variables

        # source ENV variables manually as Upstart doesn't, eg:
        #. /etc/environment

        exec /bin/bash <<'EOT'
          # set HOME to the setuid user's home, there doesn't seem to be a better, portable way
          export HOME="$(eval echo ~$(id -un))"

          if [ -d "/usr/local/rbenv/bin" ]; then
            export PATH="/usr/local/rbenv/bin:/usr/local/rbenv/shims:$PATH"
          elif [ -d "$HOME/.rbenv/bin" ]; then
            export PATH="$HOME/.rbenv/bin:$HOME/.rbenv/shims:$PATH"
          elif [ -f  /etc/profile.d/rvm.sh ]; then
            source /etc/profile.d/rvm.sh
          elif [ -f /usr/local/rvm/scripts/rvm ]; then
            source /etc/profile.d/rvm.sh
          elif [ -f "$HOME/.rvm/scripts/rvm" ]; then
            source "$HOME/.rvm/scripts/rvm"
          elif [ -f /usr/local/share/chruby/chruby.sh ]; then
            source /usr/local/share/chruby/chruby.sh
            if [ -f /usr/local/share/chruby/auto.sh ]; then
              source /usr/local/share/chruby/auto.sh
            fi
            # if you aren't using auto, set your version here
            # chruby 2.0.0
          fi

          cd $app
          logger -t puma "Starting server: $app"

          rvm use 2.2.1@rails42

          export SECRET_KEY_BASE=72afbe0ae3484c413b3b3b75fb651ab6de254514a0c8f7f865d812c9ffb5a5b61952c519f8a98d2ec1ba75237fa2a83d21de5502d91e24151e58616cd6bf60e6

          exec bundle exec puma -e production -C config/puma.rb
        EOT
        end script

    sudo vim /etc/puma.conf

        /home/deploy/1edu.haijia.net.cn/cdict/current
        /home/deploy/1edu.haijia.net.cn/yiedu/current
        /home/deploy/pd.chejj.com.cn/chejjpd/current

本地配置：

    # local
    subl Gemfile

        # Use Puma as the app server
        gem 'puma', '~> 3.0'

        # Use Mina for deployment
        #gem 'mina-puma', require: false, group: :development

    subl config/puma.rb

        # Puma can serve each request in a thread from an internal thread pool.
        # The `threads` method setting takes two numbers a minimum and maximum.
        # Any libraries that use thread pools should be configured to match
        # the maximum value specified for Puma. Default is set to 5 threads for minimum
        # and maximum, this matches the default thread size of Active Record.
        #
        threads_count = ENV.fetch("RAILS_MAX_THREADS") { 5 }.to_i
        threads threads_count, threads_count

        # Specifies the `port` that Puma will listen on to receive requests, default is 3000.
        #
        port        ENV.fetch("PORT") { 3000 }

        # Specifies the `environment` that Puma will run in.
        #
        environment ENV.fetch("RAILS_ENV") { "development" }

        # Specifies the number of `workers` to boot in clustered mode.
        # Workers are forked webserver processes. If using threads and workers together
        # the concurrency of the application would be max `threads` * `workers`.
        # Workers do not work on JRuby or Windows (both of which do not support
        # processes).
        #
        workers ENV.fetch("WEB_CONCURRENCY") { 2 }

        # Use the `preload_app!` method when specifying a `workers` number.
        # This directive tells Puma to first boot the application and load code
        # before forking the application. This takes advantage of Copy On Write
        # process behavior so workers use less memory. If you use this option
        # you need to make sure to reconnect any threads in the `on_worker_boot`
        # block.
        #
        preload_app!

        # The code in the `on_worker_boot` will be called if you are using
        # clustered mode by specifying a number of `workers`. After each worker
        # process is booted this block will be run, if you are using `preload_app!`
        # option you will want to use this block to reconnect to any threads
        # or connections that may have been created at application boot, Ruby
        # cannot share connections between processes.
        #
        on_worker_boot do
          ActiveRecord::Base.establish_connection if defined?(ActiveRecord)
        end

        # Allow puma to be restarted by `rails restart` command.
        plugin :tmp_restart

        app_dir = File.expand_path("../..", __FILE__)    # current
        shared_dir = "#{app_dir}/../../shared"    # root of app
        bind "unix://#{shared_dir}/tmp/sockets/puma.sock"
        stdout_redirect "#{shared_dir}/log/puma.stdout.log", "#{shared_dir}/log/puma.stderr.log", true
        pidfile "#{shared_dir}/tmp/pids/puma.pid"
        state_path "#{shared_dir}/tmp/pids/puma.state"
        activate_control_app

    mkdir -p config/puma/

    subl config/puma/development.rb

        # Puma can serve each request in a thread from an internal thread pool.
        # The `threads` method setting takes two numbers a minimum and maximum.
        # Any libraries that use thread pools should be configured to match
        # the maximum value specified for Puma. Default is set to 5 threads for minimum
        # and maximum, this matches the default thread size of Active Record.
        #
        threads_count = ENV.fetch("RAILS_MAX_THREADS") { 5 }.to_i
        threads threads_count, threads_count

        # Specifies the `port` that Puma will listen on to receive requests, default is 3000.
        #
        port        ENV.fetch("PORT") { 3000 }

        # Specifies the `environment` that Puma will run in.
        #
        environment ENV.fetch("RAILS_ENV") { "development" }

        # Specifies the number of `workers` to boot in clustered mode.
        # Workers are forked webserver processes. If using threads and workers together
        # the concurrency of the application would be max `threads` * `workers`.
        # Workers do not work on JRuby or Windows (both of which do not support
        # processes).
        #
        # workers ENV.fetch("WEB_CONCURRENCY") { 2 }

        # Use the `preload_app!` method when specifying a `workers` number.
        # This directive tells Puma to first boot the application and load code
        # before forking the application. This takes advantage of Copy On Write
        # process behavior so workers use less memory. If you use this option
        # you need to make sure to reconnect any threads in the `on_worker_boot`
        # block.
        #
        # preload_app!

        # The code in the `on_worker_boot` will be called if you are using
        # clustered mode by specifying a number of `workers`. After each worker
        # process is booted this block will be run, if you are using `preload_app!`
        # option you will want to use this block to reconnect to any threads
        # or connections that may have been created at application boot, Ruby
        # cannot share connections between processes.
        #
        # on_worker_boot do
        #   ActiveRecord::Base.establish_connection if defined?(ActiveRecord)
        # end

        # Allow puma to be restarted by `rails restart` command.
        plugin :tmp_restart

### Mina的配置

Mina的配置涉及两个文件

* `Gemfile`
* `config/deploy.rb`

本地配置：

    # local
    subl Gemfile

        # Use Mina for deployment
        gem 'mina', group: :development
        #gem 'mina-puma', require: false, group: :development

    bundle

    subl config/deploy.rb

        require 'mina/bundler'
        require 'mina/rails'
        require 'mina/git'
        # require 'mina/rbenv'  # for rbenv support. (http://rbenv.org)
        require 'mina/rvm'    # for rvm support. (http://rvm.io)
        require 'mina/puma'    # for puma support. (https://github.com/sandelius/mina-puma)

        # Basic settings:
        #   domain       - The hostname to SSH to.
        #   deploy_to    - Path to deploy into.
        #   repository   - Git repo to clone from. (needed by mina/git)
        #   branch       - Branch name to deploy. (needed by mina/git)

        set :domain, 'pd.chejj.com.cn'
        set :deploy_to, '/home/deploy/pd.chejj.com.cn/chejjpd'
        set :repository, 'https://github.com/chinakr/chejjpd.git'
        set :branch, 'master'

        # For system-wide RVM install.
        #   set :rvm_path, '/usr/local/rvm/bin/rvm'

        # Manually create these paths in shared/ (eg: shared/config/database.yml) in your server.
        # They will be linked in the 'deploy:link_shared_paths' step.
        set :shared_paths, ['config/database.yml', 'config/secrets.yml', 'log']

        # Optional settings:
        set :user, 'deploy'    # Username in the server to SSH to.
        #   set :port, '30000'     # SSH port number.
        #   set :forward_agent, true     # SSH forward_agent.

        # This task is the environment that is loaded for most commands, such as
        # `mina deploy` or `mina rake`.
        task :environment do
          # If you're using rbenv, use this to load the rbenv environment.
          # Be sure to commit your .ruby-version or .rbenv-version to your repository.
          # invoke :'rbenv:load'

          # For those using RVM, use this to load an RVM version@gemset.
          invoke :'rvm:use[2.3@rails5]'
        end

        # Put any custom mkdir's in here for when `mina setup` is ran.
        # For Rails apps, we'll make some of the shared paths that are shared between
        # all releases.
        task :setup => :environment do
          queue! %[mkdir -p "#{deploy_to}/#{shared_path}/log"]
          queue! %[chmod g+rx,u+rwx "#{deploy_to}/#{shared_path}/log"]

          queue! %[mkdir -p "#{deploy_to}/#{shared_path}/config"]
          queue! %[chmod g+rx,u+rwx "#{deploy_to}/#{shared_path}/config"]

          queue! %[touch "#{deploy_to}/#{shared_path}/config/database.yml"]
          queue! %[touch "#{deploy_to}/#{shared_path}/config/secrets.yml"]
          queue  %[echo "-----> Be sure to edit '#{deploy_to}/#{shared_path}/config/database.yml' and 'secrets.yml'."]

          queue! %[mkdir -p "#{deploy_to}/#{shared_path}/tmp/sockets"]
          queue! %[mkdir -p "#{deploy_to}/#{shared_path}/tmp/pids"]

          if repository
            repo_host = repository.split(%r{@|://}).last.split(%r{:|\/}).first
            repo_port = /:([0-9]+)/.match(repository) && /:([0-9]+)/.match(repository)[1] || '22'

            queue %[
              if ! ssh-keygen -H  -F #{repo_host} &>/dev/null; then
                ssh-keyscan -t rsa -p #{repo_port} -H #{repo_host} >> ~/.ssh/known_hosts
              fi
            ]
          end
        end

        desc "Deploys the current version to the server."
        task :deploy => :environment do
          to :before_hook do
            # Put things to run locally before ssh
          end
          deploy do
            # Put things that will set up an empty directory into a fully set-up
            # instance of your project.
            invoke :'git:clone'
            #invoke :'deploy:link_shared_paths'
            invoke :'bundle:install'
            invoke :'rails:db_migrate'
            invoke :'rails:assets_precompile'
            invoke :'deploy:cleanup'

            to :launch do
              queue "mkdir -p #{deploy_to}/#{current_path}/tmp/"
              queue "touch #{deploy_to}/#{current_path}/tmp/restart.txt"
            end
          end
        end

        # For help in making your deploy script, see the Mina documentation:
        #
        #  - http://nadarei.co/mina
        #  - http://nadarei.co/mina/tasks
        #  - http://nadarei.co/mina/settings
        #  - http://nadarei.co/mina/helpers

### 部署操作

    # run once
    mina setup  --verbose

    git push

    mina deploy --verbose

    mina "run[sudo restart puma-manager]"
    mina "run[sudo service nginx restart]"


