# Rails笔记


## 参考资料

* 电子书
    + [Ruby on Rails Tutorial by Michael Hartl](https://www.railstutorial.org/book "Learn Web Development with Rails")：在线阅读免费。Michael Hartl因其对Ruby社区所作的贡献，获得了“Ruby Hero Adward”。
        - the Rails way
        - Git
        - GitHub
        - Heroku
        - example, demo, a real-world project
    + [Rails 5 开发进阶](https://www.gitbook.com/book/kelby/rails-beginner-s-guide/details)：自己使用 Rails 已经有几年时间了，我一直想对它有个全面、系统的了解。所以编写、整理了这本书，供自己学习和使用，尽量做到全面、系统，有讲概念，有讲原理。 — kelby
        - 本书主要包括两部分：Rails 源码剖析和 Rails 使用指南。Rails 是一个 Web 开发框架，也是一个工具。"工欲善其事必先利其器"，想要更好的使用 Rails 这个工具，清楚其背后的魔法，阅读源代码是必备功课。
        - 本书尽量做到系统、全面，从源码出发，会讲解到原理。本书大部分内容为原创，少数内容为整理网上资料，鉴于参考资料太多，恕我不能一一列举来源。
* 教程
    + [xdite：我的学习经验](https://ruby-china.org/topics/30294)
        - (语言平实达意，逻辑性清晰、环环相扣，因此可读性很强——数学系的写文字其实也有优势，让人容易理解)
        - 练习数学要写证明题，假设一道证题有10个步骤，如果你答题只写`1,2,7,8`的话，老师只会给`1,2`的分。你跳答，老师就知道你作弊了。这样强制数学系的人养成一个习惯，做事情都要从根本想起，把问题想透。 (数学对逻辑的训练：做事情都要从根本想起，把问题想透)
        - 于是就开了GROWTHSCHOOL，别入是教你入门，我是教你变成职业程序员。因为我之前培养出很多职业程序员，所以很清楚入门技能、方法、职业要求。 (入门级程序员和职业程序员)
            * 用户故事是教学的好方法，容易理解，对于高级程序员和初级程序员都是如此。
                + 用户故事教学就是按照用户的使用流程梳理需求和解决方案，然后层层拆解的过程。一直拆解，直到能直接写出程序为止。例如网店管理员需要一个管理后台，首先需要有帐号密码才能登录，登录后要有一个商品列表，能够添加、修改、删除，还要有一个订单列表，能够发货、退换货。
        - 找到Ruby on Rails，我写大型程序的速度有了很大提升。但后来我发现，自己写程序很快没有用，要很多人一起写才有用。但哪怕只是三、四个人的团队，有效沟通都是一个很大问题。所以要让一个网站快速发展就需要学习项目管理，否则很多事情都乱糟糟的，效率就无法提升。 (编程和项目管理)
        - 把项目管理练习到极致后，我又发现开发和产品必须结合，否则一味跟从产品经理和老板的意见，最后就会失去热情，做出的产品也不真正满足市场需要——一句话，学编程就要懂产品。 (编程和产品)
            * 产品和商品不同。产品的价值很低，但商品是有价值的。程序员要想让自己生产的产品变成有价值的商品，就需要懂产品，而不只是别人让你干什么你就干什么，把编程纯粹当作一项工作来做。
        - 有些新手只想跟大师学，问了一个问题，希望大师回答你。但大师有大师的风格，如果你的问题太蠢太无俚头的话，大师是没有兴趣和你聊天的，这样就会有挫折感。然后新手就会怀疑是自己的问题，还是大师的问题。但事实上根本不是这回事，是你自己没有达到那个境界，频率对不上，问问题的方式也不对。 (境界达不到，频率对不上，就没办法和高手对话)
        - 大家往往都习惯于选择远大的目标，但事实上学习需要选择适合的目标。 (学习需要选择适合的目标)
            * 解决问题的能力很重要。有了这个能力，不管软件开发怎么发展，你还是可以用相同的方法找到自己的途径，而与你用什么编程语言无关。例如，我学习iOS编程，它和我之前接触的语言无关，我用相同的方法，把每一个难题控制在我通过努力就可以解决的范围。如果不这么做，我就没办法克服眼前学习上的难关，也就无法继续下去，就会有很强的挫折感。 (控制问题的规模很重要)
        - 看书、研讨会、工作坊、学习别人的经验是学习编程最快最便宜的办法。因为自学要花时间，而时间是不可逆货币，太贵了。 (时间成本是最高的成本)
        - 我的哲学是：先做出可以解决问题的东西。 (实用主义) (不忘初心很重要：为了解决问题)
        - 学会用程序员思维去思考问题，对于没办法手动解决的问题，可以试着用程序去解决看看。比如记帐、计步。 (程序员思维) (也是产品经理思维)
            * 程序员思维就是把未知的问题列出来，找出已有的模式、已有的解决方案，再用有效率的方法，把大的难题拆解成小的难题然后再支解决，在这个过程中不断学习。 (从未知到已知，从问题到解决问题的过程)
            * 不具有程序员思维的人，根本不会编程。 (程序员思维是程序员的基本素质)
        - 学习编程是为了解决生活中困扰我们的问题。今天，对于每个人来说学习编程都很重要，因为未来通过编程解决问题的需求只会越来越多。 (语言、数学、编程是三门基础课程)
        - 程序是编程的结果，编程语言是表达想法的工具。Web编程，是把日常的商业模式变成网上的商业模式的过程。重点在于如何想出解决问题的方法，并把它具体化，而不在于使用什么编程语言。 (重点是提出解决问题的方法并具体实现)
        - 程序员的自我奖励：热情、进步、成就感。
* 开发环境配置
    + [InstallRails.com](http://installrails.com/steps/choose_os)
    * [Could9](https://c9.io/)：`ruby -v`，`gem install rails -v 5.0.0.rc1`，`rails -v`，`rvm gemset create rails5`，`rvm use 2.3@rails5 --default`，`rails new myapp`，`cd myapp/`，`rails s -b $IP -p $PORT`。
        + 注意禁用AdBlock Plus，否则语法高亮会失效。
        + 在右上角的`Settings`中设置`Code Editor (Ace) > Soft Tabs`为`2`(默认为`4`)。
        + 在右上角的`Share`中设置`Links to share > Application > Public`为打勾，并复制外部访问Rails应用程序的URL。
    * `Linux笔记`
    * `macOS笔记`
    * `Git笔记`
* 命令行
    + [The Rails Command Line](http://guides.rubyonrails.org/command_line.html)
* 路由
    + [Rails 5 improves searching for routes with advanced options](http://blog.bigbinary.com/2016/02/16/rails-5-options-for-rake-routes.html)
    + [Rails Routing from the Outside In](http://guides.rubyonrails.org/routing.html)
    + [ActionDispatch::Routing](http://api.rubyonrails.org/classes/ActionDispatch/Routing.html)
* 数据库
    + [Populating the Database with seeds.rb](http://www.xyzpub.com/en/ruby-on-rails/3.2/seed_rb.html)
    + [Purge or recreate a Ruby on Rails database](http://stackoverflow.com/questions/4116067/purge-or-recreate-a-ruby-on-rails-database)
* 日期时间
    + [rails generates model field:type, what are the options for field:type?](http://stackoverflow.com/questions/4384284/rails-generates-model-fieldtype-what-are-the-options-for-fieldtype)：`:primary_key, :string, :text, :integer, :float, :decimal, :datetime, :timestamp, :time, :date, :binary, :boolean, :references`
* Model
    + [Active Record Basics](http://guides.rubyonrails.org/active_record_basics.html)
    + [Advanced Rails model generators](http://railsguides.net/advanced-rails-model-generators/)：`rails generate model photo album:references`
* View
    + [Form Helpers](http://guides.rubyonrails.org/form_helpers.html)
    + `Foundation笔记`
    + `Sass笔记`
* 静态文件
    + [The Asset Pipeline](http://guides.rubyonrails.org/asset_pipeline.html)：挺长的一个文档，不过写得很清楚。
    + [Where do you put CSS files in a rails app directory?](http://stackoverflow.com/questions/1058886/where-do-you-put-css-files-in-a-rails-app-directory)
* 测试
    + [TDD is dead. Long live testing.](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html "By David Heinemeier Hansson on April 23, 2014")
* 项目实例
    + `用Rails 5和Foundation 6开发在线报名系统`


## 中英文对照

| 英文                              | 中文                  |
|-----------------------------------|-----------------------|
| automated testing                 | 自动化测试            |
| TDD (Test-Driven Development)     | 测试驱动开发          |
| test suite                        | 测试套件              |
| regression                        | 退化                  |
| "Red, Green, Refactor" cycle      | “红、绿、重构”循环    |
| ERb (embedded Ruby)               | ERb模板系统(嵌入Ruby) |
| stack trace                       | 栈追踪                |
| backtrace                         | 向后追踪              |
| silencer                          | 消音器                |
| CSRF (Cross-Site Request Forgery) | 跨站脚本攻击          |
| layout                            | 布局文件              |
| asset                             | 资源                  |
| pipeline                          | 管道                  |
| manifest                          | 清单                  |


## 新特性

  * Rails 5的新特性
      + [What’s New in Rails 5](http://www.sitepoint.com/whats-new-rails-5/)
          - [Rails 5 有什么新特性？](http://www.linuxidc.com/Linux/2015-06/119345.htm)
          - Rails 5合并了`rails-api`gem，可以直接作为JSON API使用。
          - Rails 5仅支持Ruby 2.2.1及以上版本。
          - Rails 5支持Turbolinks 3。
          - Rails 5支持Action Cable。
          - Rails 5用`rails`代替了`rake`命令行工具。
  * 升级到Rails 5
      + [Updating to Rails 5.0](http://railsapps.github.io/updating-rails.html)


## 知识体系

* 开发环境配置
    + 安装Ruby
    + 安装Rails
    + 配置IDE
        - 缩进
        - 语法高亮
* Web开发的一般原则
* Web开发的最佳实践
* 版本控制系统的使用(Git)
    + 公共仓库GitHub
    + 私有仓库BitBucket
* Rails应用程序的开发流程
    + 脚手架的使用(scaffolding)
        - 视图
            * HTML
            * CSS
            * JavaScript
        - 模型
        - URL
        - 控制器
    + 测试驱动开发(TDD)
* Rails应用程序的测试(minitest)
    + 单元测试
    + 功能测试
    + 集成测试
* Rails应用程序的部署(部署到生产环境)
    + 部署到VPS
        - `nginx + Puma + Mina`
    + 部署到Heroku
        - PostgreSQL
        - Git


## 对Rails的粗浅认识

### 什么是Rails

Rails是一个用Ruby编写的Web开发框架。

### 总体认识

rails不是一个简单的gem，而是由一系列gem组成的精密系统，其中包括了一系列方便的命令行工具。

rails应用的rails及ruby版本升级实例：

  1. rvm install ruby 2.2
  2. rvm gemset create rails42
  3. rvm use 2.2@rails42
  4. gem insall rails -v 4.2.1
  5. mv myapp/ myapp_old/
  6. rails new myapp
  7. cd myapp
  8. subl Gemfile # 添加需要使用的gems
  9. bundle
  10. rails g devise:install # 如果使用了devise
  11. rails g rails-foundation # 如果使用了rails-foundation
  12. cp -r ../myapp_old/config/* config/
  13. cp -r ../myapp_old/app/* app/
  14. rails s

小结：对于一个rails应用，`Gemfile`、`config/`和`app/`是关键，然后是所依赖的gems。为了减少不可控因素，不是必须的gems尽量不用。

### Rails控制台(console)

Rails控制台是和Rails应用程序交互的有用工具。通过控制台，可以方便地查询Rails或Ruby的API，做一些简单的代码测试。

启动控制台：

    rails console

或

    rails c

使用`exit`或`quit`命令(或`Ctrl + D`快捷键)退出控制台，返回终端。使用`Ctrl + C`中断当前执行。

在沙箱中运行Rails控制台：

    rails c --sandbox

注：沙箱的含义是在退出控制台时，所做修改都会回滚。

以生产环境启动控制台(默认为开发环境)：

    RAILS_ENV=production rails c

示例代码-在控制台下查询模型对象的一对多关系(来自`The Rails Tutorial > Chapter 2: Toy app`)：

    rails c
    > first_user = User.first
    > first_user.microposts
    > one_micropost = first_user.microposts.first
    > one_microposts.user

配置Rails控制台(基于irb)：

    vim ~/.irbrc

        IRB.conf[:PROMPT_MODE] = :SIMPLE
        IRB.conf[:AUTO_INDENT_MODE] = false

## Rails开发环境的配置

参考资料：

* [Ruby官网](https://www.ruby-lang.org/en/)：最新版本`2.3.1`。
* [Rails官网](http://rubyonrails.org/)：最新版本`5.0.0.rc1`。

相关代码：

    rvm install 2.3.1
    rvm use 2.3.1 --default
    ruby -v

    rvm gemset create rails5
    rvm use 2.3.1@rails5 --default
    rvm gemset list

    gem install rails -v 5.0.0.rc1 --no-rdoc --no-ri --verbose
    rails -v

    mkdir -p ~/workspace/
    cd ~/workspace/
    rails new myapp
    cd myapp/

### Rails环境变量

    rails c

        Rails.env    # => "development"
        Rails.env.development?    # => true
        Rails.env.production?    # => false

    rails c production

        Rails.env    # => "production"
        Rails.env.production?    # => true

    heroku run console

        Rails.env    # => "production"
        Rails.env.production?    # => true


## Rails的基本用法

### Bundler的基本用法

    subl Gemfile
    bundle

注：

1. `bundle`是`bundle install`的简写。
2. 以`bundle exec`为前缀的命令将使用和Gemfile对应的软件版本，如`bundle exec rails db:migrate`，在一些系统上`bundle exec`可省略，即`rails db:migrate`。可以总是省略`bundle exec`，仅在遇到问题时再加上它试一下。

按照`Gemfile`中指定的版本更新已安装的gem：

    bundle update

注：如果`bundle install`运行正常，但`rails test`提示找不到某些gem，这时可以试着运行一下`bundle update`。

在本地(开发环境)安装gem，忽略生产环境下需要的gem：

    bundle --without production

注：bundler会记信`--without production`这个选项，因此只需要运行一次`bundle --without production`，之后就可以用`bundle`代替了。

### gem的基本用法

    gem list sqlite3

        *** LOCAL GEMS ***
        sqlite3 (1.3.11)

    gem list puma

        *** LOCAL GEMS ***
        puma (3.4.0)

### Rails命令行基本用法

查看Rails命令行使用帮助：

    rails help

        Usage:
          rails new APP_PATH [options]

        Options:
          -r, [--ruby=PATH]                                      # Path to the Ruby binary of your choice
                                                                 # Default: /Users/chinakr/.rvm/rubies/ruby-2.3.0/bin/ruby
          -m, [--template=TEMPLATE]                              # Path to some application template (can be a filesystem path or URL)
          -d, [--database=DATABASE]                              # Preconfigure for selected database (options: mysql/oracle/postgresql/sqlite3/frontbase/ibm_db/sqlserver/jdbcmysql/jdbcsqlite3/jdbcpostgresql/jdbc)
                                                                 # Default: sqlite3
          -j, [--javascript=JAVASCRIPT]                          # Preconfigure for selected JavaScript library
                                                                 # Default: jquery
              [--skip-gemfile], [--no-skip-gemfile]              # Don't create a Gemfile
          -B, [--skip-bundle], [--no-skip-bundle]                # Don't run bundle install
          -G, [--skip-git], [--no-skip-git]                      # Skip .gitignore file
              [--skip-keeps], [--no-skip-keeps]                  # Skip source control .keep files
          -M, [--skip-action-mailer], [--no-skip-action-mailer]  # Skip Action Mailer files
          -O, [--skip-active-record], [--no-skip-active-record]  # Skip Active Record files
          -P, [--skip-puma], [--no-skip-puma]                    # Skip Puma related files
          -C, [--skip-action-cable], [--no-skip-action-cable]    # Skip Action Cable files
          -S, [--skip-sprockets], [--no-skip-sprockets]          # Skip Sprockets files
              [--skip-spring], [--no-skip-spring]                # Don't install Spring application preloader
              [--skip-listen], [--no-skip-listen]                # Don't generate configuration that depends on the listen gem
          -J, [--skip-javascript], [--no-skip-javascript]        # Skip JavaScript files
              [--skip-turbolinks], [--no-skip-turbolinks]        # Skip turbolinks gem
          -T, [--skip-test], [--no-skip-test]                    # Skip test files
              [--dev], [--no-dev]                                # Setup the application with Gemfile pointing to your Rails checkout
              [--edge], [--no-edge]                              # Setup the application with Gemfile pointing to Rails repository
              [--rc=RC]                                          # Path to file containing extra configuration options for rails command
              [--no-rc], [--no-no-rc]                            # Skip loading of extra configuration options from .railsrc file
              [--api], [--no-api]                                # Preconfigure smaller stack for API only apps

        Runtime options:
          -f, [--force]                    # Overwrite files that already exist
          -p, [--pretend], [--no-pretend]  # Run but do not make any changes
          -q, [--quiet], [--no-quiet]      # Suppress status output
          -s, [--skip], [--no-skip]        # Skip files that already exist

        Rails options:
          -h, [--help], [--no-help]        # Show this help message and quit
          -v, [--version], [--no-version]  # Show Rails version number and quit

        Description:
            The 'rails new' command creates a new Rails application with a default
            directory structure and configuration at the path you specify.

            You can specify extra command-line arguments to be used every time
            'rails new' runs in the .railsrc configuration file in your home directory.

            Note that the arguments specified in the .railsrc file don't affect the
            defaults values shown above in this help message.

        Example:
            rails new ~/Code/Ruby/weblog

            This generates a skeletal Rails installation in ~/Code/Ruby/weblog.

    rails s --help

        Usage: rails server [mongrel, thin etc] [options]
            -p, --port=port                  Runs Rails on the specified port.
                                             Default: 3000
            -b, --binding=IP                 Binds Rails to the specified IP.
                                             Default: localhost
            -c, --config=file                Uses a custom rackup configuration.
            -d, --daemon                     Runs server as a Daemon.
            -e, --environment=name           Specifies the environment to run this server under (test/development/production).
                                             Default: development
            -P, --pid=pid                    Specifies the PID file.
                                             Default: tmp/pids/server.pid
            -C, --[no-]dev-caching           Specifies whether to perform caching in development.
                                             true or false

            -h, --help                       Shows this help message.

    rails g

        Running via Spring preloader in process 74763
        Usage: rails generate GENERATOR [args] [options]

        General options:
          -h, [--help]     # Print generator's options and usage
          -p, [--pretend]  # Run but do not make any changes
          -f, [--force]    # Overwrite files that already exist
          -s, [--skip]     # Skip files that already exist
          -q, [--quiet]    # Suppress status output

        Please choose a generator below.

        Rails:
          assets
          channel
          controller
          generator
          helper
          integration_test
          jbuilder
          job
          mailer
          migration
          model
          resource
          scaffold
          scaffold_controller
          task

        Coffee:
          coffee:assets

        Js:
          js:assets

        TestUnit:
          test_unit:generator
          test_unit:plugin


    rails g controller

        Running via Spring preloader in process 74783
        Usage:
          rails generate controller NAME [action action] [options]

        Options:
              [--skip-namespace], [--no-skip-namespace]  # Skip namespace (affects only isolated applications)
              [--skip-routes], [--no-skip-routes]        # Don't add routes to config/routes.rb.
          -e, [--template-engine=NAME]                   # Template engine to be invoked
                                                         # Default: erb
          -t, [--test-framework=NAME]                    # Test framework to be invoked
                                                         # Default: test_unit

        Runtime options:
          -f, [--force]                    # Overwrite files that already exist
          -p, [--pretend], [--no-pretend]  # Run but do not make any changes
          -q, [--quiet], [--no-quiet]      # Suppress status output
          -s, [--skip], [--no-skip]        # Skip files that already exist

        Description:
            Stubs out a new controller and its views. Pass the controller name, either
            CamelCased or under_scored, and a list of views as arguments.

            To create a controller within a module, specify the controller name as a
            path like 'parent_module/controller_name'.

            This generates a controller class in app/controllers and invokes helper,
            template engine, assets, and test framework generators.

        Example:
            `rails generate controller CreditCards open debit credit close`

            CreditCards controller with URLs like /credit_cards/debit.
                Controller: app/controllers/credit_cards_controller.rb
                Test:       test/controllers/credit_cards_controller_test.rb
                Views:      app/views/credit_cards/debit.html.erb [...]
                Helper:     app/helpers/credit_cards_helper.rb

    rails g model

        Running via Spring preloader in process 74804
        Usage:
          rails generate model NAME [field[:type][:index] field[:type][:index]] [options]

        Options:
              [--skip-namespace], [--no-skip-namespace]  # Skip namespace (affects only isolated applications)
              [--force-plural], [--no-force-plural]      # Forces the use of the given model name
          -o, --orm=NAME                                 # ORM to be invoked
                                                         # Default: active_record

        ActiveRecord options:
              [--migration], [--no-migration]        # Indicates when to generate migration
                                                     # Default: true
              [--timestamps], [--no-timestamps]      # Indicates when to generate timestamps
                                                     # Default: true
              [--parent=PARENT]                      # The parent class for the generated model
              [--indexes], [--no-indexes]            # Add indexes for references and belongs_to columns
                                                     # Default: true
              [--primary-key-type=PRIMARY_KEY_TYPE]  # The type for primary key
          -t, [--test-framework=NAME]                # Test framework to be invoked
                                                     # Default: test_unit

        TestUnit options:
              [--fixture], [--no-fixture]   # Indicates when to generate fixture
                                            # Default: true
          -r, [--fixture-replacement=NAME]  # Fixture replacement to be invoked

        Runtime options:
          -f, [--force]                    # Overwrite files that already exist
          -p, [--pretend], [--no-pretend]  # Run but do not make any changes
          -q, [--quiet], [--no-quiet]      # Suppress status output
          -s, [--skip], [--no-skip]        # Skip files that already exist

        Description:
            Stubs out a new model. Pass the model name, either CamelCased or
            under_scored, and an optional list of attribute pairs as arguments.

            Attribute pairs are field:type arguments specifying the
            model's attributes. Timestamps are added by default, so you don't have to
            specify them by hand as 'created_at:datetime updated_at:datetime'.

            As a special case, specifying 'password:digest' will generate a
            password_digest field of string type, and configure your generated model and
            tests for use with Active Model has_secure_password (assuming the default ORM
            and test framework are being used).

            You don't have to think up every attribute up front, but it helps to
            sketch out a few so you can start working with the model immediately.

            This generator invokes your configured ORM and test framework, which
            defaults to Active Record and TestUnit.

            Finally, if --parent option is given, it's used as superclass of the
            created model. This allows you create Single Table Inheritance models.

            If you pass a namespaced model name (e.g. admin/account or Admin::Account)
            then the generator will create a module with a table_name_prefix method
            to prefix the model's table name with the module name (e.g. admin_accounts)

        Available field types:

            Just after the field name you can specify a type like text or boolean.
            It will generate the column with the associated SQL type. For instance:

                `rails generate model post title:string body:text`

            will generate a title column with a varchar type and a body column with a text
            type. If no type is specified the string type will be used by default.
            You can use the following types:

                integer
                primary_key
                decimal
                float
                boolean
                binary
                string
                text
                date
                time
                datetime

            You can also consider `references` as a kind of type. For instance, if you run:

                `rails generate model photo title:string album:references`

            It will generate an `album_id` column. You should generate these kinds of fields when
            you will use a `belongs_to` association, for instance. `references` also supports
            polymorphism, you can enable polymorphism like this:

                `rails generate model product supplier:references{polymorphic}`

            For integer, string, text and binary fields, an integer in curly braces will
            be set as the limit:

                `rails generate model user pseudo:string{30}`

            For decimal, two integers separated by a comma in curly braces will be used
            for precision and scale:

                `rails generate model product 'price:decimal{10,2}'`

            You can add a `:uniq` or `:index` suffix for unique or standard indexes
            respectively:

                `rails generate model user pseudo:string:uniq`
                `rails generate model user pseudo:string:index`

            You can combine any single curly brace option with the index options:

                `rails generate model user username:string{30}:uniq`
                `rails generate model product supplier:references{polymorphic}:index`

            If you require a `password_digest` string column for use with
            has_secure_password, you can specify `password:digest`:

                `rails generate model user password:digest`

            If you require a `token` string column for use with
            has_secure_token, you can specify `auth_token:token`:

                `rails generate model user auth_token:token`

        Examples:
            `rails generate model account`

                For Active Record and TestUnit it creates:

                    Model:      app/models/account.rb
                    Test:       test/models/account_test.rb
                    Fixtures:   test/fixtures/accounts.yml
                    Migration:  db/migrate/XXX_create_accounts.rb

            `rails generate model post title:string body:text published:boolean`

                Creates a Post model with a string title, text body, and published flag.

            `rails generate model admin/account`

                For Active Record and TestUnit it creates:

                    Module:     app/models/admin.rb
                    Model:      app/models/admin/account.rb
                    Test:       test/models/admin/account_test.rb
                    Fixtures:   test/fixtures/admin/accounts.yml
                    Migration:  db/migrate/XXX_create_admin_accounts.rb

    rails g scaffold

        Running via Spring preloader in process 74817
        Usage:
          rails generate scaffold NAME [field[:type][:index] field[:type][:index]] [options]

        Options:
              [--skip-namespace], [--no-skip-namespace]             # Skip namespace (affects only isolated applications)
              [--force-plural], [--no-force-plural]                 # Forces the use of the given model name
          -o, --orm=NAME                                            # ORM to be invoked
                                                                    # Default: active_record
              [--model-name=MODEL_NAME]                             # ModelName to be used
              [--resource-route], [--no-resource-route]             # Indicates when to generate resource route
                                                                    # Default: true
          -y, [--stylesheets], [--no-stylesheets]                   # Generate Stylesheets
                                                                    # Default: true
          -se, [--stylesheet-engine=STYLESHEET_ENGINE]              # Engine for Stylesheets
                                                                    # Default: scss
              [--assets], [--no-assets]                             # Indicates when to generate assets
                                                                    # Default: true
          -ss, [--scaffold-stylesheet], [--no-scaffold-stylesheet]  # Indicates when to generate scaffold stylesheet
                                                                    # Default: true
          -c, --scaffold-controller=NAME                            # Scaffold controller to be invoked
                                                                    # Default: scaffold_controller

        ActiveRecord options:
              [--migration], [--no-migration]        # Indicates when to generate migration
                                                     # Default: true
              [--timestamps], [--no-timestamps]      # Indicates when to generate timestamps
                                                     # Default: true
              [--parent=PARENT]                      # The parent class for the generated model
              [--indexes], [--no-indexes]            # Add indexes for references and belongs_to columns
                                                     # Default: true
              [--primary-key-type=PRIMARY_KEY_TYPE]  # The type for primary key
          -t, [--test-framework=NAME]                # Test framework to be invoked
                                                     # Default: test_unit

        TestUnit options:
              [--fixture], [--no-fixture]   # Indicates when to generate fixture
                                            # Default: true
          -r, [--fixture-replacement=NAME]  # Fixture replacement to be invoked

        ScaffoldController options:
              [--helper], [--no-helper]  # Indicates when to generate helper
                                         # Default: true
              [--api], [--no-api]        # Generates API controller
          -e, [--template-engine=NAME]   # Template engine to be invoked
                                         # Default: erb
              [--jbuilder]               # Indicates when to generate jbuilder
                                         # Default: true

        Asset options:
          -j, [--javascripts], [--no-javascripts]       # Generate JavaScripts
                                                        # Default: true
          -je, [--javascript-engine=JAVASCRIPT_ENGINE]  # Engine for JavaScripts
                                                        # Default: coffee

        Runtime options:
          -f, [--force]                    # Overwrite files that already exist
          -p, [--pretend], [--no-pretend]  # Run but do not make any changes
          -q, [--quiet], [--no-quiet]      # Suppress status output
          -s, [--skip], [--no-skip]        # Skip files that already exist

        Description:
            Scaffolds an entire resource, from model and migration to controller and
            views, along with a full test suite. The resource is ready to use as a
            starting point for your RESTful, resource-oriented application.

            Pass the name of the model (in singular form), either CamelCased or
            under_scored, as the first argument, and an optional list of attribute
            pairs.

            Attributes are field arguments specifying the model's attributes. You can
            optionally pass the type and an index to each field. For instance:
            'title body:text tracking_id:integer:uniq' will generate a title field of
            string type, a body with text type and a tracking_id as an integer with an
            unique index. "index" could also be given instead of "uniq" if one desires
            a non unique index.

            As a special case, specifying 'password:digest' will generate a
            password_digest field of string type, and configure your generated model,
            controller, views, and test suite for use with Active Model
            has_secure_password (assuming they are using Rails defaults).

            Timestamps are added by default, so you don't have to specify them by hand
            as 'created_at:datetime updated_at:datetime'.

            You don't have to think up every attribute up front, but it helps to
            sketch out a few so you can start working with the resource immediately.

            For example, 'scaffold post title body:text published:boolean' gives
            you a model with those three attributes, a controller that handles
            the create/show/update/destroy, forms to create and edit your posts, and
            an index that lists them all, as well as a resources :posts declaration
            in config/routes.rb.

            If you want to remove all the generated files, run
            'rails destroy scaffold ModelName'.

        Examples:
            `rails generate scaffold post`
            `rails generate scaffold post title:string body:text published:boolean`
            `rails generate scaffold purchase amount:decimal tracking_id:integer:uniq`
            `rails generate scaffold user email:uniq password:digest`

### Rails应用程序(项目)的目录结构

参考资料：

* [Ruby on Rails - Directory Structure](http://www.tutorialspoint.com/ruby-on-rails/rails-directory-structure.htm "Google关键字：rails directory structure")
* [Rails 4 Directory Structure](http://raysrashmi.com/2013/07/09/rails4-directory-structure/ "Google关键字：rails 5 directory structure")

示例代码：

    rails new cdict
    cd cdict

    tree

        .
        ├── Gemfile
        ├── Gemfile.lock
        ├── README.md
        ├── Rakefile
        ├── app
        │   ├── assets
        │   │   ├── config
        │   │   │   └── manifest.js
        │   │   ├── images
        │   │   ├── javascripts
        │   │   │   ├── application.js
        │   │   │   ├── cable.coffee
        │   │   │   └── channels
        │   │   └── stylesheets
        │   │       └── application.css
        │   ├── channels
        │   │   └── application_cable
        │   │       ├── channel.rb
        │   │       └── connection.rb
        │   ├── controllers
        │   │   ├── application_controller.rb
        │   │   └── concerns
        │   ├── helpers
        │   │   └── application_helper.rb
        │   ├── jobs
        │   │   └── application_job.rb
        │   ├── mailers
        │   │   └── application_mailer.rb
        │   ├── models
        │   │   ├── application_record.rb
        │   │   └── concerns
        │   └── views
        │       └── layouts
        │           ├── application.html.erb
        │           ├── mailer.html.erb
        │           └── mailer.text.erb
        ├── bin
        │   ├── bundle
        │   ├── rails
        │   ├── rake
        │   ├── setup
        │   ├── spring
        │   └── update
        ├── config
        │   ├── application.rb
        │   ├── boot.rb
        │   ├── cable.yml
        │   ├── database.yml
        │   ├── environment.rb
        │   ├── environments
        │   │   ├── development.rb
        │   │   ├── production.rb
        │   │   └── test.rb
        │   ├── initializers
        │   │   ├── active_record_belongs_to_required_by_default.rb
        │   │   ├── application_controller_renderer.rb
        │   │   ├── assets.rb
        │   │   ├── backtrace_silencers.rb
        │   │   ├── callback_terminator.rb
        │   │   ├── cookies_serializer.rb
        │   │   ├── filter_parameter_logging.rb
        │   │   ├── inflections.rb
        │   │   ├── mime_types.rb
        │   │   ├── per_form_csrf_tokens.rb
        │   │   ├── request_forgery_protection.rb
        │   │   ├── session_store.rb
        │   │   └── wrap_parameters.rb
        │   ├── locales
        │   │   └── en.yml
        │   ├── puma.rb
        │   ├── routes.rb
        │   └── secrets.yml
        ├── config.ru
        ├── db
        │   └── seeds.rb
        ├── lib
        │   ├── assets
        │   └── tasks
        ├── log
        ├── public
        │   ├── 404.html
        │   ├── 422.html
        │   ├── 500.html
        │   ├── apple-touch-icon-precomposed.png
        │   ├── apple-touch-icon.png
        │   ├── favicon.ico
        │   └── robots.txt
        ├── test
        │   ├── controllers
        │   ├── fixtures
        │   │   └── files
        │   ├── helpers
        │   ├── integration
        │   ├── mailers
        │   ├── models
        │   └── test_helper.rb
        ├── tmp
        │   └── cache
        │       └── assets
        └── vendor
            └── assets
                ├── javascripts
                └── stylesheets

        44 directories, 59 files

其中

* `app/`为应用程序代码的核心目录，包括了模型、视图、控制器和helper
* `app/assets/`存放应用程序的asset，包括CSS、JS和图片
* `bin/`为二进制可执行文件
* `config/`为应用程序的配置文件
* `db/`为应用程序的数据库文件
* `lib/`为库模块
* `lib/assets/`为库模块的asset，包括CSS、JS和图片
* `log/`为应用程序的日志文件
* `public/`为Web服务器可直接访问的目录，包括错误信息页面等
* `test/`为应用程序的测试代码
* `tmp/`为临时文件
* `vendor/`为第三方代码，如插件、gem
* `Gemfile`列出应用程序所依赖的gem
* `Gemfile.lock`列出了应用程序所依赖的gem的当前版本
* `Rakefile`定义了可用的rake任务
* `config.ru`：Rack中间件的配置文件

另外

* `.gitignore`是Git配置文件，指定了版本仓库中应忽略的文件目录

### Rails应用程序依赖的gem

    subl Gemfile

        source 'https://rubygems.org'

        # Bundle edge Rails instead: gem 'rails', github: 'rails/rails'
        gem 'rails', '>= 5.0.0.rc1', '< 5.1'
        # Use sqlite3 as the database for Active Record
        gem 'sqlite3'
        # Use Puma as the app server
        gem 'puma', '~> 3.0'
        # Use SCSS for stylesheets
        gem 'sass-rails', '~> 5.0'
        # Use Uglifier as compressor for JavaScript assets
        gem 'uglifier', '>= 1.3.0'
        # Use CoffeeScript for .coffee assets and views
        gem 'coffee-rails', '~> 4.1.0'
        # See https://github.com/rails/execjs#readme for more supported runtimes
        # gem 'therubyracer', platforms: :ruby

        # Use jquery as the JavaScript library
        gem 'jquery-rails'
        # Turbolinks makes navigating your web application faster. Read more: https://github.com/turbolinks/turbolinks
        gem 'turbolinks', '~> 5.x'
        # Build JSON APIs with ease. Read more: https://github.com/rails/jbuilder
        gem 'jbuilder', '~> 2.0'
        # Use Redis adapter to run Action Cable in production
        # gem 'redis', '~> 3.0'
        # Use ActiveModel has_secure_password
        # gem 'bcrypt', '~> 3.1.7'

        # Use Capistrano for deployment
        # gem 'capistrano-rails', group: :development

        group :development, :test do
          # Call 'byebug' anywhere in the code to stop execution and get a debugger console
          gem 'byebug', platform: :mri
        end

        group :development do
          # Access an IRB console on exception pages or by using <%= console %> anywhere in the code.
          gem 'web-console'
          gem 'listen', '~> 3.0.5'
          # Spring speeds up development by keeping your application running in the background. Read more: https://github.com/rails/spring
          gem 'spring'
          gem 'spring-watcher-listen', '~> 2.0.0'
        end

        # Windows does not include zoneinfo files, so bundle the tzinfo-data gem
        gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]

指定gem版本号的几种方式：

* `gem 'uglifier', '>= 1.3.0'`：高于(含)`1.3.0`的版本号都是可用的。
* `gem 'rails', '>= 5.0.0.rc1', '< 5.1'`：高于(含)`5.0.0.rc1`、低于(不含)`5.1`的版本号都是可用的。
* `gem 'puma', '~> 3.0'`：像`3.0.x`或`3.0.x.x`这样的版本号都是可用的。

指定gem依赖关系所属环境的两种方法：

方法一：

    gem 'capistrano-rails', group: :development

方法二：

    group :development do
      gem 'spring'
      gem 'spring-watcher-listen', '~> 2.0.0'
    end

或

    group :development, :test do
      gem 'spring'
      gem 'spring-watcher-listen', '~> 2.0.0'
    end

### 资源管道的用法(Asset Pipeline)

注：asset或可翻译为资源。

Rails通过`sprockets-rails`这个gem提供了资源管道(Asset Pipeline)功能。资源管道主要有3个作用：

1. 把CSS和JS文件分别组装为单个文件(`application.css`和`application.js`)，这样可以减少Web浏览器的请求数量，提高页面加截速度；
2. 压缩CSS和JS文件(通过删除空白字符)，减小文件体积，提高页面加截速度；
3. 使用Sass来编写CSS，使用CoffeScript来编写JavaScript，提高编程效率。

这样，在开发环境下可以把CSS、JS代码放在多个文件中以实现良好的逻辑结构，并通过缩进和空格实现良好的代码风格，从面得到良好的编程体验；在生产环境下，又可以得到数量最少、体积最小的CSS和JS文件，从而得到高性能；可谓两全其美的解决方案。

注：Sass 3.0开始使用Scss语法，Scss语法向下兼容CSS语法。

如果不想使用资源管道，可以使用`rails new appname --skip-sprockets`来新建Rails应用。

使用资源管道需要搞清楚三个问题：1) 资源目录(assets)；2) 清单文件(manifest)；3) 预处理引擎。

一、文件存放位置

需要预处理的文件存放的位置：

  * `app/assets/stylesheets/`：存放CSS文件。
  * `app/assets/javascripts/`：存放JS文件。
  * `app/assets/images/`：存放图片。

注：在生产环境下，这些文件经过预处理后，将存放在`public/assets/`目录下。

不需要预外理的文件存放的位置：

  * `public/stylesheets/`：存放CSS文件。
  * `public/javascripts/`：存放JS文件。
  * `public/images/`：存放图片。

注：仅当`config.serve_static_files = true`时，`public/`下的文件才会被当作静态文件处理。

关于文件存放位置的更多选择：

  * `app/assets/`：用于存放应用自己的CSS、JS和图片文件。
  * `lib/assets/`：用于存放跨应用的CSS、JS和图片文件(库)。
  * `vendor/assets/`：用于存放第三方提供的文件，如CSS框架和JavaScript插件。

二、清单文件(manifest)

Rails按照清单文件，把资源目录下的CSS和JS文件分别组装成单个文件。

应用的清单文件包括：

    app/assets/stylesheets/application.css
    app/assets/javascripts/application.js

CSS的清单文件：

    subl app/assets/stylesheets/application.css

        /*
         *
         *= require_tree .
         *= require_self
        */

其中`require_tree .`的作用是把`app/assets/stylesheets/`目录及其子目录下的所有CSS文件包含到应用程序CSS文件中。`require_self`的作用是把`application.css`文件自己包含到应用程序CSS文件中。

三、对资源文件的引用(asset)

官方文档给出的例子：

    app/assets/javascripts/home.js
    lib/assets/javascripts/moovinator.js
    vendor/assets/javascripts/slider.js
    app/assets/javascripts/sub/something.js

对上述文件，都可以通过下面的方法来引用

    //= require home
    //= require moovinator
    //= require slider
    //= require sub/something

同时还要加上

    <%= stylesheet_link_tag "application", media: "all", "data-turbolinks-track" => true %>
    <%= javascript_include_tag "application", "data-turbolinks-track" => true %>

对图片的引用：

    public/assets/images/rails.png
    public/assets/images/icons/favicon.png

    <%= image_tag "rails.png" %>
    <%= image_tag "icons/favicon.png" %>

以下均为在erb文件中引用CSS、JS和图片文件。

在CSS中引用图片：

    .class { background-image: url(<%= asset_path 'image.png' %>) }

在JS中引用图片：

    $('#logo').attr({ src: "<%= asset_path('logo.png') %>" });

四、预处理引擎(preprocessing engines)

在Rails按照清单文件把资源文件(CSS、JS)分别组装成单个文件之前，会使用预处理引擎对这些资源文件进行预处理。Rails会根据资源文件的后缀选用合适的预处理引擎。例如`*.scss`的CSS文件，`*.coffee`的JS文件，`*.erb`的模板文件。

对于复杂后缀的资源文件，Rails会按照后缀从右到左的顺序依次调用合适的预处理引擎，例如对`mycontroller.js.erb.coffee`会依次调用CoffeeScript和ERb预处理引擎。

五、生产环境下的部署

    RAILS_ENV=production rails assets:precompile

### 新建Rails应用

    rails new signup

              create
              create  README.md
              create  Rakefile
              create  config.ru
              create  .gitignore
              create  Gemfile
              create  app
              create  app/assets/config/manifest.js
              create  app/assets/javascripts/application.js
              create  app/assets/javascripts/cable.coffee
              create  app/assets/stylesheets/application.css
              create  app/channels/application_cable/channel.rb
              create  app/channels/application_cable/connection.rb
              create  app/controllers/application_controller.rb
              create  app/helpers/application_helper.rb
              create  app/jobs/application_job.rb
              create  app/mailers/application_mailer.rb
              create  app/models/application_record.rb
              create  app/views/layouts/application.html.erb
              create  app/views/layouts/mailer.html.erb
              create  app/views/layouts/mailer.text.erb
              create  app/assets/images/.keep
              create  app/assets/javascripts/channels
              create  app/assets/javascripts/channels/.keep
              create  app/controllers/concerns/.keep
              create  app/models/concerns/.keep
              create  bin
              create  bin/bundle
              create  bin/rails
              create  bin/rake
              create  bin/setup
              create  bin/update
              create  config
              create  config/routes.rb
              create  config/application.rb
              create  config/environment.rb
              create  config/secrets.yml
              create  config/cable.yml
              create  config/puma.rb
              create  config/environments
              create  config/environments/development.rb
              create  config/environments/production.rb
              create  config/environments/test.rb
              create  config/initializers
              create  config/initializers/active_record_belongs_to_required_by_default.rb
              create  config/initializers/application_controller_renderer.rb
              create  config/initializers/assets.rb
              create  config/initializers/backtrace_silencers.rb
              create  config/initializers/callback_terminator.rb
              create  config/initializers/cookies_serializer.rb
              create  config/initializers/cors.rb
              create  config/initializers/filter_parameter_logging.rb
              create  config/initializers/inflections.rb
              create  config/initializers/mime_types.rb
              create  config/initializers/per_form_csrf_tokens.rb
              create  config/initializers/request_forgery_protection.rb
              create  config/initializers/session_store.rb
              create  config/initializers/wrap_parameters.rb
              create  config/locales
              create  config/locales/en.yml
              create  config/boot.rb
              create  config/database.yml
              create  db
              create  db/seeds.rb
              create  lib
              create  lib/tasks
              create  lib/tasks/.keep
              create  lib/assets
              create  lib/assets/.keep
              create  log
              create  log/.keep
              create  public
              create  public/404.html
              create  public/422.html
              create  public/500.html
              create  public/apple-touch-icon-precomposed.png
              create  public/apple-touch-icon.png
              create  public/favicon.ico
              create  public/robots.txt
              create  test/fixtures
              create  test/fixtures/.keep
              create  test/fixtures/files
              create  test/fixtures/files/.keep
              create  test/controllers
              create  test/controllers/.keep
              create  test/mailers
              create  test/mailers/.keep
              create  test/models
              create  test/models/.keep
              create  test/helpers
              create  test/helpers/.keep
              create  test/integration
              create  test/integration/.keep
              create  test/test_helper.rb
              create  tmp
              create  tmp/.keep
              create  tmp/cache
              create  tmp/cache/assets
              create  vendor/assets/javascripts
              create  vendor/assets/javascripts/.keep
              create  vendor/assets/stylesheets
              create  vendor/assets/stylesheets/.keep
              remove  config/initializers/cors.rb
                 run  bundle install
        Fetching gem metadata from https://rubygems.org/...........
        Fetching version metadata from https://rubygems.org/...
        Fetching dependency metadata from https://rubygems.org/..
        Resolving dependencies....
        Installing rake 11.1.1
        Using concurrent-ruby 1.0.1
        Using i18n 0.7.0
        Installing minitest 5.8.4
        Using thread_safe 0.3.5
        Using builder 3.2.2
        Using erubis 2.7.0
        Using mini_portile2 2.0.0
        Using json 1.8.3
        Using nio4r 1.2.1
        Using websocket-extensions 0.1.2
        Using mime-types 2.99.1
        Using arel 7.0.0
        Using bundler 1.11.2
        Installing byebug 8.2.2 with native extensions
        Installing coffee-script-source 1.10.0
        Installing execjs 2.6.0
        Using method_source 0.8.2
        Using thor 0.19.1
        Installing debug_inspector 0.0.2 with native extensions
        Installing ffi 1.9.10 with native extensions
        Installing multi_json 1.11.2
        Installing rb-fsevent 0.9.7
        Installing puma 3.2.0 with native extensions
        Installing sass 3.4.21
        Installing tilt 2.0.2
        Installing spring 1.6.4
        Installing sqlite3 1.3.11 with native extensions
        Installing turbolinks-source 5.0.0.beta3
        Using tzinfo 1.2.2
        Using nokogiri 1.6.7.2
        Using rack 2.0.0.alpha
        Using websocket-driver 0.6.3
        Using mail 2.6.3
        Installing coffee-script 2.4.1
        Installing uglifier 2.7.2
        Installing rb-inotify 0.9.7
        Installing turbolinks 5.0.0.beta2
        Using activesupport 5.0.0.beta3
        Using loofah 2.0.3
        Using rack-test 0.6.3
        Using sprockets 3.5.2
        Installing listen 3.0.6
        Using rails-deprecated_sanitizer 1.0.3
        Using globalid 0.3.6
        Using activemodel 5.0.0.beta3
        Installing jbuilder 2.4.1
        Using rails-html-sanitizer 1.0.3
        Installing spring-watcher-listen 2.0.0
        Using rails-dom-testing 1.0.7
        Using activejob 5.0.0.beta3
        Using activerecord 5.0.0.beta3
        Using actionview 5.0.0.beta3
        Using actionpack 5.0.0.beta3
        Using actioncable 5.0.0.beta3
        Using actionmailer 5.0.0.beta3
        Using railties 5.0.0.beta3
        Using sprockets-rails 3.0.4
        Installing coffee-rails 4.1.1
        Installing jquery-rails 4.1.1
        Installing web-console 3.1.1
        Using rails 5.0.0.beta3
        Installing sass-rails 5.0.4
        Bundle complete! 15 Gemfile dependencies, 63 gems now installed.
        Use `bundle show [gemname]` to see where a bundled gem is installed.
                 run  bundle exec spring binstub --all
        * bin/rake: spring inserted
        * bin/rails: spring inserted

### 新建脚手架

注：

通过脚手架(scaffold)我们可以快速建立可用的Rails应用程序框架，在此基础上还需要进一步完成

* 在模型中添加数据校验(data validation)
* 为管理页面添加用户认证(authentication)
* 添加测试代码(test)
* 使用布局文件(layout)实现统一的页面风格(styling)和导航(navigation)

一、最简单的Model

    rails g scaffold Product order:integer name:string price:integer note:string category:string schedule:string license:string car:string

        Running via Spring preloader in process 42550
              invoke  active_record
              create    db/migrate/20160321133636_create_products.rb
              create    app/models/product.rb
              invoke    test_unit
              create      test/models/product_test.rb
              create      test/fixtures/products.yml
              invoke  resource_route
               route    resources :products
              invoke  scaffold_controller
              create    app/controllers/products_controller.rb
              invoke    erb
              create      app/views/products
              create      app/views/products/index.html.erb
              create      app/views/products/edit.html.erb
              create      app/views/products/show.html.erb
              create      app/views/products/new.html.erb
              create      app/views/products/_form.html.erb
              invoke    test_unit
              create      test/controllers/products_controller_test.rb
              invoke    helper
              create      app/helpers/products_helper.rb
              invoke      test_unit
              invoke    jbuilder
              create      app/views/products/index.json.jbuilder
              create      app/views/products/show.json.jbuilder
              invoke  assets
              invoke    coffee
              create      app/assets/javascripts/products.coffee
              invoke    scss
              create      app/assets/stylesheets/products.scss
              invoke  scss
           identical    app/assets/stylesheets/scaffolds.scss

    rails db:migrate

        == 20160321124850 CreateProducts: migrating ===================================
        -- create_table(:products)
           -> 0.0012s
        == 20160321124850 CreateProducts: migrated (0.0013s) ==========================

二、带有外键的Model

    rails g scaffold Order datetime:datetime name:string mobile:string note:string product:references

        Running via Spring preloader in process 43249
              invoke  active_record
              create    db/migrate/20160321154404_create_orders.rb
              create    app/models/order.rb
              invoke    test_unit
              create      test/models/order_test.rb
              create      test/fixtures/orders.yml
              invoke  resource_route
               route    resources :orders
              invoke  scaffold_controller
              create    app/controllers/orders_controller.rb
              invoke    erb
              create      app/views/orders
              create      app/views/orders/index.html.erb
              create      app/views/orders/edit.html.erb
              create      app/views/orders/show.html.erb
              create      app/views/orders/new.html.erb
              create      app/views/orders/_form.html.erb
              invoke    test_unit
              create      test/controllers/orders_controller_test.rb
              invoke    helper
              create      app/helpers/orders_helper.rb
              invoke      test_unit
              invoke    jbuilder
              create      app/views/orders/index.json.jbuilder
              create      app/views/orders/show.json.jbuilder
              invoke  assets
              invoke    coffee
              create      app/assets/javascripts/orders.coffee
              invoke    scss
              create      app/assets/stylesheets/orders.scss
              invoke  scss
           identical    app/assets/stylesheets/scaffolds.scss

    rails db:migrate

        == 20160321154404 CreateOrders: migrating =====================================
        -- create_table(:orders)
           -> 0.0036s
        == 20160321154404 CreateOrders: migrated (0.0037s) ============================


### 删除脚手架

    rails destroy scaffold Product
    rails db:drop
    rails db:migrate

### 新建控制器

语法说明：

    rails g controller ControllerName <optional action names>.

示例代码：

    rails g controller HelloWorld hello bye

### 删除控制器

    rails destroy controller HelloWorld hello bye

注：动作名称参数(`hello`和`bye`)不能省略。

### 新建模型

    rails g model User name:string email:string

### 删除模型

    rails destroy model User

注：字段参数可以省略。这一点和删除控制器不同。

### 应用数据迁移(migrations)

在开发环境下应用数据迁移

    rails db:migrate

注：

1. 本地默认为开发环境，但Heroku默认为生产环境，这一点需要注意。
2. 生成的数据迁移文件位于`db/migrate/`目录下，文件名以时间戳开头，这种命名方式可以避免多人协同开发时出现文件名冲突。

在生产环境下应用数据迁移：

    RAILS_ENV=production rails db:migrate

### 撤销数据迁移(migrations)

撤销最后一次数据迁移(migration)：

    rails db:rollback

撤销所有数据迁移(migrations)：

    rails db:rollback VERSION=0

注：对于可逆的数据库操作，数据迁移只需定义`change`方法；但对于不可逆的数据库操作，数据迁移需分别定义`up`和`down`方法。

### 清空数据库(reset)

示例代码：

    rails db:migrate:reset

### 查看URL路由

Rails采用RESTful风格的路由机制。例如在`config/routes.rb`中定义`resources :users`时，对模型对象`User`的创建(create)、查看(show)、修改(update)、删除(destroy)操作将对应于HTTP的POST、GET、PATCH、DELETE操作，对应的URL如`/users`、`/users/1`、`/users/1`、`/users/1`。

HTTP基本操作-四种请求类型：

| HTTP动词 | 定义               |
|----------|--------------------|
| GET      | 读取页面；读取数据 |
| POST     | 提交表单；创建对象 |
| PATCH    | 修改对象           |
| DELETE   | 删除对象           |

查看Rails应用程序的URL路由配置：

    rails routes

              Prefix Verb   URI Pattern                  Controller#Action
            products GET    /products(.:format)          products#index
                     POST   /products(.:format)          products#create
         new_product GET    /products/new(.:format)      products#new
        edit_product GET    /products/:id/edit(.:format) products#edit
             product GET    /products/:id(.:format)      products#show
                     PATCH  /products/:id(.:format)      products#update
                     PUT    /products/:id(.:format)      products#update
                     DELETE /products/:id(.:format)      products#destroy

注：使用Rails路由至少有两个好处，1) 节约了思考设计和实际编程的时间；2) 统一了设计风格。

### 自定义路由

参考资料：Rails Guides > Rails Routing from the Outside In

示例代码：

    get 'welcome/hello'    # controller WelcomeController and action hello
    get '/patients/:id', to: 'patients#show'

实例：

    subl config/routes.rb

参考资料：[How to add a custom action to the controller in Rails 3](http://stackoverflow.com/questions/13763818/how-to-add-a-custom-action-to-the-controller-in-rails-3)

使用说明：

    resources :items do
      collection do
        post :schedule
        put :save_scheduling
      end
    end
    This is going to create URLs like

    /items/schedule
    /items/save_scheduling
    Because you're passing an item into your schedule_... route method, you likely want member routes instead of collection routes.

    resources :items do
      member do
        post :schedule
        put :save_scheduling
      end
    end
    This is going to create URLs like

    /items/:id/schedule
    /items/:id/save_scheduling

设置主页URL：

    root to: 'orders#new'

或

    root 'order#show'

为自定义Action设置URL：

          resources :orders do
            collection do
              get :welcome
            end
          end

### 命名路径(named routes)

路由定义、命名路径和URL的对应关系：

* `root 'welcome#home'` -> `root_path` -> `/`
    + `root_url` -> `http://www.example.com/`
* `get 'about' => 'welcome#about'` -> `about_path` -> `/about`
    + `about_url` -> `http://www.example.com/about`
* `get 'welcome#hello'` -> `welcome_hello_path` -> `/welcome/hello`

命名路径的使用：

    <%= link_to 'About', about_path %>

### 页面跳转

参考资料：[ActionController::Redirecting](http://api.rubyonrails.org/classes/ActionController/Redirecting.html)

不带id：

    subl config/routes.rb

          resources :orders do
            collection do
              get :welcome
            end
          end

    subl app/controllers/orders_controller.rb

        format.html { redirect_to action: 'welcome' }

带id：

    subl config/routes.rb

          resources :orders do
            member do
              get :welcome
            end
          end

    subl app/controllers/orders_controller.rb

        before_action :set_order, only: [:welcome]

        format.html { redirect_to action: 'welcome', id: @order }

在控制器中实现页面跳转：

    # app/controllers/users_controllers.rb
    def create
      @user = User.new(users_params)
      if @user.save
        redirect_to @user
      else
        render 'new'
      end
    end

其中`redirect_to @user`等价于`redirect_to user_url(@user)`。

### 插入测试数据

    subl db/seeds.rb

        product_list = [
          [1, '手动挡预约班(C1)，周一至周五，比亚迪', 4700, '自行预约，单人单车，周一至周五训练时段，适合自由职业者。', '预约班', '周一至周五', 'C1', '比亚迪'],
          [2, '手动挡预约班(C1)，周一至周五，桑塔纳', 4800, '自行预约，单人单车，周一至周五训练时段，适合自由职业者。', '预约班', '周一至周五', 'C1', '桑塔纳'],
          [3, '手动挡预约班(C1)，周一至周日，比亚迪', 5100, '自行预约，单人单车，周一至周日训练时段，适合上班族及自由职业者。', '预约班', '周一至周日', 'C1', '比亚迪'],
          [4, '手动挡预约班(C1)，周一至周日，桑塔纳', 5200, '自行预约，单人单车，周一至周日训练时段，适合上班族及自由职业者。', '预约班', '周一至周日', 'C1', '桑塔纳'],
        ]

        product_list.each do |order, name, price, note, category, schedule, license, car|
          Product.create(order: order, name: name, price: price, note: note, category: category, schedule: schedule, license: license, car: car)
        end

    rails db:seed

### 清空测试数据

    rails db:drop
    rails db:migrate

    rails db:seed

### 直接返回HTML代码

参考资料：[How to return HTML directly from a Rails controller?](http://stackoverflow.com/questions/1958759/how-to-return-html-directly-from-a-rails-controller "Google关键字：rails render raw html")

示例代码：

    render text: '<p>Hello world!</p>'


> DEPRECATION WARNING: `render :text` is deprecated because it does not actually render a `text/plain` response. Switch to `render plain: 'plain text'` to render as `text/plain`, `render html: '<strong>HTML</strong>'` to render as `text/html`, or `render body: 'raw'` to match the deprecated behavior and render with the default Content-Type, which is `text/plain`. (called from query at /Users/chinakr/workspace/ruby/rails/cdict/app/controllers/dicts_controller.rb:67)
  Rendering text template
  Rendered text template (0.0ms)

示例代码：

    render html: '<p>Hello world!</p>'

### 启动Web服务器

启动Web服务器：

    rails s

其中`s`是`server`的简写。

重启Web服务器：

    rails restart

在生产环境下启动Web服务器：

    rails s --environment production

或

    RAILS_ENV=production rails s

### 把提示信息改为中文

参考资料：

  * [Rails 国际化 API](http://guides.ruby-china.org/i18n.html)
      + 易于使用、可扩展的多语言支持
      + 国际化就是把所有字符串和本地化相关的信息从应用程序中抽取出来
          - 提供i18n支持的gem，本地化字典，locale相关设置
      + 本地化就是为这些信息提供翻译
          - 替换或补全默认的locale，把提示信息、View中的静态文本抽取为字典
      + 正确使用Rails提供的i18n API
          - i18n的工作机制：完整的i18n支持
          - 如何在RESTful应用程序中正确使用i18n
          - 如何用i18n翻译ActiveRecord错误提示和ActionMailer邮件
      + 需要重点学习的内容：
          - 3 Internationalizing your Application (Step by Step教程)
          - 4.6 Translations for Active Record Models
              * 字段(属性)
              * 4.6.1 Error Message Scopes
              * 4.6.2 Error Message Interpolation
  * [在 Rails 中友好的展示错误信息](http://mednoter.com/better-errors.html)
  * [Rails I18N: ActiveRecord对象本地化](http://blog.ashchan.com/archive/2008/11/24/rails-i18n-activerecord-model-human-name-made-easy/)
  * [多國語系及時區](https://ihower.tw/rails4/i18n.html)
  * [rails-i18n/rails/locale/en.yml](https://github.com/svenfuchs/rails-i18n/blob/master/rails/locale/en.yml)
  * [rails-i18n/rails/locale/zh-CN.yml](https://raw.githubusercontent.com/svenfuchs/rails-i18n/master/rails/locale/zh-CN.yml)：可以直接放在`config/locales/`目录下并使用。
  * [Devise Wiki > I18n](https://github.com/plataformatec/devise/wiki/I18n "Google关键字：rails devise i18n zh-CN")
      + [适用于Devise 3.5.2的zh-CN i18n](https://gist.github.com/Kenrick-Zhou/7909822)
  * [How to use Rails I18n.t to translate an ActiveRecord attribute?](http://stackoverflow.com/questions/1863526/how-to-use-rails-i18n-t-to-translate-an-activerecord-attribute "Google关键字：rails i18n activerecord.attributes")

简介：

Rails的i18n支持由Public i18n API和Simple后端组成。

Public i18n API是一个Ruby模块，定义了i18n相关的公有方法，也即定义了i18n库的行为。

Simple后端是默认后端，后端是对Public i18n API的具体实现。可以用可强大的其他后端来代替Simple后端。

Public i18n API最重要的两个方法是`translate`和`localize`，前者用于查询文本翻译，后者用于查询本地化信息(如日期时间对象)，可分别简写为`t`和`l`(别名)。

用法示例：

    I18n.t 'store.title'
    I18n.l Time.now

示例代码-静态文本的翻译：

    # app/controllers/application_controller.rb
    class ApplicationController < ActionController::Base
      before_action :set_locale

      def set_locale
        I18n.locale = params[:locale] || I18n.default_locale
      end
    end

    # app/controllers/home_controller.rb
    class HomeController < ApplicationController
      def index
        flash[:notice] = t(:hello_flash)
      end
    end

    # app/views/home/index.html.erb
    <h1><%=t :hello_world %></h1>
    <p><%= flash[:notice] %></p>

    # config/locales/en.yml
    en:
      hello_world: Hello world!
      hello_flash: Hello flash!

    # config/locales/pirate.yml
    pirate:
      hello_world: Ahoy World
      hello_flash: Ahoy Flash

    firefox http://localhost:3000?locale=pirate

示例代码-在翻译中使用变量：

    # app/views/home/index.html.erb
    <%=t 'greet_username', user: "Bill", message: "Goodbye" %>

    # config/locales/en.yml
    en:
      greet_username: "%{message}, %{user}!"

示例代码-使用本地化日期时间：

    # app/views/home/index.html.erb
    <p><%= l Time.now, format: :short %></p>

    # config/locales/pirate.yml
    pirate:
      time:
        formats:
          short: "arrrround %H'ish"

示例代码-Model属性名称的中文本地化：

    # config/locales/en.yml
    en:
      activerecord:
        models:
          user: Dude
        attributes:
          user:
            login: 'Handle'

    # View
    User.model_name.human    # Dude
    User.human_attribute_name(:login)    # Handle

示例代码-在console下测试：

    rails c
    > I18n.t :hello

相关代码：

    rails console

        order = Order.new
        order.valid?    # => false
        order.errors.full_messages
        # => ["Product must exist", "Name can't be blank", "Mobile can't be blank"]

    subl Gemfile

        # To use simpified Chinese for error messages
        gem 'rails-i18n'

    subl config/application.rb

        config.i18n.default_locale = 'zh-CN'

    subl config/locales/zh-CN.yml

        zh-CN:
          hello: '你好！'
          activerecord:
            attributes:
              order:
                product: '课程'
                name: '姓名'
                mobile: '手机'
            errors:
              models:
                order:
                  attributes:
                    product:
                      required: '必须填写'
                      blank: '必须填写'
                    name:
                      blank: '必须填写'
                    mobile:
                      blank: '必须填写'

    subl app/views/orders/_form.html.erb

        <h2>订单提交出现<%= order.errors %>个错误：</h2>

    rails console

        order = Order.new
        order.valid?    # => false
        order.errors.full_messages
        => ["课程必须填写", "姓名必须填写", "手机必须填写"]


### 获取访客IP

参考资料：[Rails: Get Client IP address](http://stackoverflow.com/questions/4465476/rails-get-client-ip-address)

语法：


    request.remote_ip


示例代码：


    rails g migration add_ip_to_orders ip:string

        Running via Spring preloader in process 88154
            invoke  active_record
            create    db/migrate/20160326072416_add_ip_to_orders.rb

    rails db:migrate

        == 20160326072416 AddIpToOrders: migrating ====================================
        -- add_column(:orders, :ip, :string)
         -> 0.0043s
        == 20160326072416 AddIpToOrders: migrated (0.0043s) ===========================

    subl app/controllers/orders_controller.rb

        def create
          ...
          @order.ip = request.remote_ip
          ...
        end

    subl app/views/orders/show.html.erb

        <p>
          <strong>IP:</strong>
          <%= @order.ip %>
        </p>

    subl app/views/orders/index.html.erb

        <th>IP</th>

        <td><%= order.ip %></td>

    subl app/views/user_mailer/new_order_email.html.erb

        <li>IP：<%= @order.ip %></li>


## 模型(Model)

### 模型的基本操作

添加记录：

    user = User.new(name: 'chinakr', email: 'chinakr@gmail.com')
    user.valid?
    user.save

或

    user = User.create(name: 'chinakr', email: 'chinakr@gmail.com')

注：如果保存失败，`user.save`会返回`false`。

查询记录：

    user = User.find(1)
    user.name
    user.email
    user.updated_at

或

    user = User.find_by(email: 'chinakr@gmail.com')

注：

1. 其中`1`是某条记录的id。
2. 如果相关记录不存在，会抛出一个`ActiveRecord::RecordNotFound`异常。

获得第一条记录：

    user = User.first

获得完整的记录列表：

    users = User.all

获得记录的总条数：

    total = User.count

修改记录(更新记录)：

    user = User.find(1)
    user.name = Ye
    user.save

或

    user = User.find(1)
    user.update_attribute(name: 'Ye')

或

    user = User.find(1)
    user.update_attributes(name: 'Ye', email: 'chinakr@hotmail.com')

注：`update_attributes`可以同时更新记录的多个属性。

删除记录：

    user = User.find(1)
    user.destroy

复制记录：

    dup_user = user.dup

查看错误信息：

    user.errors.full_messages

### 为用户模型增加加密密码

示例代码：

    # app/models/user.rb
    class User < ActiveRecord
      ...
      has_secure_password
    end

`has_secure_password`方法完成的工作：

1. 把加密后的密码`password_digest`保存到数据库；
2. 强制校验`password`和`password_confirmation`属性；
3. 增加了`authenticate`方法，当输入密码正确时返回`ture`，错误时返回`false`。

要使用`has_secure_password`方法，用户表必须具有`password_digest`字段，即：

    rails g model User name:string email:string password_digest:string
    rails db:migrate

或

    rails g model User name:string email:string
    rails db:migrate
    ...
    rails g migration add_password_digest_to_users password_digest:string
    rails db:migrate

还需要安装`bcrypt`这个gem用于密码加密：

    subl Gemfile

        gem 'bcrypt'

    bundle

校验密码：1) 不能为空；2) 不能少于6个字符。

    # app/models/user.rb
    class User < ActiveRecord
      ...
      has_secure_password
      validates :password, presence: true, length: {minimum: 6}
    end

相关测试代码：

    # test/models/user_test.rb
    require 'test_helper'
    class UserTest < ActiveSupport::TestCase
      def setup
        @user = User.create(name: 'chinakr', email: 'chinakr@gmail.com', password: 'helloworld', password_confirmation: 'helloworld')
      end
      test 'should be valid' do
        assert @user.valid?
      end
      test 'password should not be blank' do
        @user.password = @user.password_confirmation = ' ' * 6
        assert_not @user.valid?
      end
      test 'password should have more than 6 characters' do
        @user.password = @user.password_confirmation = 'a' * 5
        assert_not @user.valid?
      end
     end

在终端添加一个用户：

    rails c

        User.create(name: 'chinakr', email: 'chinakr@gmail.com', password: 'helloworld', password_confirmation: 'helloworld')

在终端删除一个用户：

    rails c

        user = User.find_by(name: 'chinakr')
        user.destroy

在终端验证用户密码：

    rails c

        user = User.find_by(name: 'chinakr')
        user.authenticate('wrongpassword')    # => false
        user.authenticate('helloworld')    # 返回`user`对象，在判断语句中相当于布尔值`true`

### SQLite数据库浏览器

[DB Browser for SQLite官网](http://sqlitebrowser.org)：可打开本地SQLite 3数据库文件。

DB Browser for SQLite是一个高质量、可视化、开源的工具，可以创建、设计、编辑SQLite数据库文件。操作对象包括数据库文件、数据表、索引、记录，还支持数据导入导出(`text`、`csv`和`sql`)、SQL语句执行和日志。

DB Browser不能代替SQLite命令行工具。

在macOS上可以用Homebrew安装DB Browser：

    brew cask install sqlitebrowser

### 控制器中模型相关的常用操作

获得全部象列表：

    @users = User.all

根据ID获得指定对象：

    @user = User.find(parmas[:id])

### 确保字段不为空

参考资料：Rails Guides > Active Record Validations > 2.9 presence

示例代码：

    class Person < ActiveRecord::Base
      validates :name, :login, :email, presence: true
    end

    validates :content, uniqueness: true, presence: true    # 同时应用多个约束条件

对应的测试代码：

    # test/models/user_test.rb
    require 'test_helper'
    class UserTest < ActiveSupport::TestCase
      def setup
        @user = User.create(name: 'chinakr', email: 'chinakr@gmail.com')
      end
      test 'should be valid' do
        assert @user.valid?
      end
      test 'name should not be blank' do
        @user.name = ''
        assert_not @user.valid?
      end
    end

### 确保字段值的唯一性(校验和索引)

参考资料：Rails Guides > Active Record Validations > 2.11 uniqueness

示例代码一：

    class Account < ActiveRecord::Base
      validates :email, uniqueness: true
    end

示例代码二：

    class Account < ActiveRecord::Base
      validates :email, uniqueness: {case_sensitive: false}
    end

注：唯一性校验默认是大小写敏感的，可通过`case_sensitive: false`设置为大小写不敏感。

需要注意的是，为避免用户连续提交表单，导致多条相同的记录在保存至数据库之前已通过校验，有必要在模型层面之外，也就是数据库层面设置唯一性校验，即为具有唯一值的字段加上索引。

在数据库层面为字段加上索引：

    rails g migration add_index_to_users_email
    rails db:migrate

注：如果`rails db:migrate`失败，可以`ps -aux | grep console`，然后`kill -9 <pid>`。这样做是为了杀死`rails c --sandbox`进程，因为这个进程会锁定数据库，导致数据迁移失败。

### 设置字段的最大长度

示例代码：

    class Micropost < ApplicationRecord
      validates :content, length: {maximum: 256}
    end

对应的测试代码：

    # test/models/user_test.rb
    require 'test_helper'
    class UserTest < ActiveSupport::TestCase
      def setup
        @user = User.create(name: 'chinakr', email: 'chinakr@gmail.com')
      end
      test 'email should not be too long' do
        @user.email = 'a' * 255 + '@example.com'
        assert_not @user.valid?
      end
    end

### 校验字符串的格式

应用场景：网址、电子邮箱、手机号等。

示例代码：

    class Account < ActiveRecord::Base
      validates :email, format: {with: /\A[\w+\-.]+@[a-z\d\-.]+\.[a-z]+\z/i}
    end

其中`\A`匹配字符串开头，`\z`匹配字符串结尾。

### 为多个字段设置多个校验条件

示例代码：

    class Person < ActiveRecord::Base
      validates :name, :login, :email, presence: true, length: {maximun: 256}
    end

### 模型的一对多关系

    # app/models/user.rb
    class User < ApplicationRecord
      has_many :microposts
    end

    # app/models/micropost.rb
    class Micropost < ApplicationRecord
      belongs_to :user
    end

### `befor_save`回调方法

示例代码-保存记录前把邮件统一改为小写：

    class User < ActiveRecord::Base
      before_save { self.email = email.downcase }
      ...
    end

或

    class User < ActiveRecord::Base
      before_save { email.downcase! }
      ...
    end

注：`email.downcase`本应写作`self.email.downcase`，但在模型中，`=`右侧的`self`可以省略。

相关测试代码：

    require 'test_helper'
    class UserTest < ActiveSupport::TestCase
      def setup
        @user = User.create(name: 'chinakr', email: 'chinakr@gmail.com', password: 'helloworld', password_confirmation: 'helloworld')
      end
      test 'should be valid' do
        assert @user.valid?
      end
      test 'email should be saved as lower-case' do
        mixed_case_email = 'WWW@example.Com'
        @user.email = mixed_case_email
        @user.save
        assert_equal mixed_case_email.downcase, @user.reload.email
      end
    end


### 选取指定字段

参考资料：Rails Guides > Active Record Query Interface > 4 Selecting Specific Fields

示例代码：

    Client.select("viewable_by, locked")
    Client.select(:name).distinct

### 查询结果排序

参考资料：Rails Guides > Active Record Query Interface

示例代码：

    Client.order(:created_at)
    Client.order("created_at")
    Client.order("created_at DESC")
    Client.order("created_at ASC")
    Client.order("orders_count ASC, created_at DESC")

    @words = Word.order('created_at desc')


## View(视图)

### ERb模板文件

示例代码-语法：

    # app/views/users/index.html.erb
    <ul>
    <% @users.each do |user| %>
      <li><%= user.name %></li>
    <% end %>
    </ul>

如上所示，`<% ... %>`和`<%= ... %>`是ERb的两个基本用法，前者针对命令，无输出，后者针对表达式，有输出。

示例代码-设置网站标题：

    <title><%= title ||= 'Site Name' %></title>

### 表单操作(form)

一、最基本的表单(`form_tag`)：

    <%= form_tag do %>
      Form contents
    <% end %>

生成的HTML为

    <form accept-charset="UTF-8" action="/" method="post">
      <input name="utf8" type="hidden" value="&#x2713;" />
      <input name="authenticity_token" type="hidden" value="J7CBxfHalt49OSHp27hblqK20c9PgwJ108nDHX/8Cts=" />
      Form contents
    </form>

二、通用的搜索表单(`form_tag`)：

    <%= form_tag("/search", method: "get") do %>
      <%= label_tag(:q, "Search for:") %>
      <%= text_field_tag(:q) %>
      <%= submit_tag("Search") %>
    <% end %>

生成的HTML为

    <form accept-charset="UTF-8" action="/search" method="get">
      <input name="utf8" type="hidden" value="&#x2713;" />
      <label for="q">Search for:</label>
      <input id="q" name="q" type="text" />
      <input name="commit" type="submit" value="Search" />
    </form>

三、使用表单的例子(`form_for`)：

    subl app/views/orders/new.html.erb

        <%= render 'form', order: @order %>

    subl app/views/orders/_form.html.erb

        <%= form_for(order) do |f| %>
          <% if order.errors.any? %>
            <div id="error_explanation">
              <h2><%= pluralize(order.errors.count, "error") %> prohibited this order from being saved:</h2>
              <ul>
              <% order.errors.full_messages.each do |message| %>
                <li><%= message %></li>
              <% end %>
              </ul>
            </div>
          <% end %>
          <div class="field">
            <%= f.label :datetime %>
            <%= f.datetime_select :datetime %>
          </div>
          <div class="field">
            <%= f.label :name %>
            <%= f.text_field :name %>
          </div>
          <div class="actions">
            <%= f.submit %>
          </div>
        <% end %>

四、应用了Bootstrap的用户注册表单

    <h1>Sign up</h1>
    <div class="row">
      <div class="col-sm-6 col-sm-offset-3">
        <%= form_for(@user) do |f| %>
          <fieldset class="form-group">
            <%= f.label :name %>
            <%= f.text_field :name, class: 'form-control' %>
          </fieldset>
          <fieldset class="form-group">
            <%= f.label :email %>
            <%= f.email_field :email, class: 'form-control' %>
          </fieldset>
          <fieldset class="form-group">
            <%= f.label :password %>
            <%= f.password_field :password, class: 'form-control' %>
          </fieldset>
          <fieldset class="form-group">
            <%= f.label :password_confirmation, 'Confirmation' %>
            <%= f.password_field :password_confirmation, class: 'form-control' %>
          </fieldset>
          <%= f.submit 'Create account', class: 'btn btn-primary' %>
        <% end %>
      </div>
    </div>

生成的HTML代码为：

    <h1>Sign up</h1>
    <div class="row">
      <div class="col-sm-6 col-sm-offset-3">
        <form class="new_user" id="new_user" action="/users" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="zdnaHvMgdbsamFdTMa4PLvuvJO+Z8q2t4FsF+E85Kx0pJKdu7NTTHWOeohVtM9DuN91bo9vcslGrtDMUY56YHQ==" />
          <fieldset class="form-group">
            <label for="user_name">Name</label>
            <input class="form-control" type="text" name="user[name]" id="user_name" />
          </fieldset>
          <fieldset class="form-group">
            <label for="user_email">Email</label>
            <input class="form-control" type="email" name="user[email]" id="user_email" />
          </fieldset>
          <fieldset class="form-group">
            <label for="user_password">Password</label>
            <input class="form-control" type="password" name="user[password]" id="user_password" />
          </fieldset>
          <fieldset class="form-group">
            <label for="user_password_confirmation">Confirmation</label>
            <input class="form-control" type="password" name="user[password_confirmation]" id="user_password_confirmation" />
          </fieldset>
          <input type="submit" name="commit" value="Create account" class="btn btn-primary" data-disable-with="Create account" />
        </form>
      </div>
    </div>

### 显示错误信息

    # app/views/users/new.html.erb
    <%= form_for(@user) do |f| %>
      <%= render 'shared/error_messages' %>
      ...
    <% end %>

    mkdir -p app/views/shared/

    # app/views/shared/_error_messages.html.erb
    <% if @user.errors.any? %>
      <div class="error-explanation">
        <div class="alert alert-danger" role="alert">
          The form contains <%= pluralize(@user.errors.count, 'error') %>
        </div>
        <ul>
        <% @user.errors.full_messages.each do |msg| %>
          <li><%= msg %></li>
        <% end %>
        </ul>
      </div>
    <% end %>

注：

1. `if @user.errors.any?`也可以换成`if @user.errors.empty?`；
2. `pluralize`helper方法用于生成`error`的正确的单复数形式。

`pluralize`helper方法的用法：

    rails c

        include ActionView::Helpers::TextHelper
        pluralize(1, 'error')    # => "1 error"
        pluralize(3, 'error')    # => "3 errors"
        pluralize(1, 'person')    # => "1 person"
        pluralize(3, 'person')    # => "3 people"

### 在erb中引用URL

参考资料：[Rails Routing from the Outside In](http://guides.rubyonrails.org/routing.html#generating-paths-and-urls-from-code)

对于路由`resources :photos`：

  * `photos_path`：返回`/photos`。
  * `new_photo_path`：返回`/photos/new`。
  * `edit_photo_path(:id)`：返回`/photos/:id/edit`，例如`edit_photo_path(10)`返回`/photos/10/edit`。
  * `photo_path(:id)`：返回`/photos/:id`， 例如`photo_path(10)`返回`/photos/10`。

注：`photos_path`返回路径，`photos_url`返回URL，后者除了路径，还包括了域名，例如`https://www.example.com/photos`。

使用示例：


    <%= link_to '订单', orders_path %>

### 布局文件

在使用`rails new ...`创建Rails应用程序时就生成了布局文件`app/views/layouts/application.html.erb`。

布局文件的作用是消除视图中的重复代码。对于一个网站，页面结构、网站导航这些风格需要统一的东西通常都是在布局文件中定义的。

布局文件中的`<%= yield %>`会被具体页面的视图文件内容所代替。

布局文件中的

    <%= stylesheet_link_tag    'application', media: 'all', 'data-turbolinks-track': 'reload' %>
    <%= javascript_include_tag 'application', 'data-turbolinks-track': 'reload' %>

用于包含CSS和JS文件，它们都是asset pipeline的一部分。

布局文件中的`<%= csrf_meta_tags %>`用于防止跨站脚本攻击。

### 为不同页面设置不同标题

    # app/views/layouts/application.html.erb
    <title><%= yield :title %></title>

    # app/views/welcome/hello.html.erb
    <% provide :title, 'Hello Page' %>

之前我的解决方案是：

    # app/views/layouts/application.html.erb
    <title><%= @title %></title>

    # app/views/welcome/hello.html.erb
    <% @title = 'Hello Page' %>

两种方法看起来是等效的。

### 在Rails中应用Foundation

注：首先拷贝Foundation文件，然后修改Rails布局文件。

参考资料：`Foundation笔记 > 布局文件`

### 使用片断(partial)

通过片断(partial)可以消除视图中的重复代码，同时也使视图代码更清晰。

示例代码：

    subl app/views/layouts/application.html.erb

        <%= render 'layouts/header' %>

    subl app/views/layouts/_header.html.erb

### 使用helper

在Rails中定义了大量helper，使用起来非常方便。

生成超链接的helper：

    <%= link_to 'Baidu', 'https://www.baidu.com/' %>
    <%= link_to image_tag('baidu.gif', alt: 'Baidu'), 'https://www.baidu.com/' %>
    <%= link_to 'Submit', '#', class: 'button' %>

以上分别为文本超链接、图片超链接和按钮。图片文件位于`app/assets/images/`目录下。

支持无限参数的helper：

    <%= link_to 'Baidu', 'https://www.baidu.com/', id: 'search-engine', class: 'main' %>

实际上是以散列表为helper的最后一个参数，`{}`省略后看起来就像支持无限参数一样，实际上也实现了这样的效果。

### 自定义helper

helper是在Rails中使用的内置函数，自定义helper是自定义的Rails函数，它们都可以在视图中使用。自定义helper位于`app/helpers/`目录下，也是应用程序代码的一部分。

    # app/helper/application_helper.rb
    module ApplicationHelper
      # Return full title of a page
      def full_title(page_title='')
        base_title = 'Ruby on Rails Tutorial Sample App'
        if page_title.empty?
          base_title
        else
          page_title + '|' + base_title
        end
      end
    end

    # app/views/layouts/applicatio.html.erb
    <title><%= full_title yield(:title) %></title>

### 自定义Helper-显示Gravatar头像

参考资料：

* [Ruby on Rails Tutorial > Chapter 7 Sign up > 7.1.4 A Gravatar image and a sidebar](https://www.railstutorial.org/book/sign_up#sec-a_gravatar_image)

Gravatar是一个免费的互联网产品，为用户提供头像上传和展示服务。

示例代码：

    # app/helpers/users_helper.rb
    module UsersHelper
      def gravatar_for(user)
        gravatar_id = Digest::MD5::hexdigest(user.email.downcase)
        gravatar_url = "https://secure.gravatar.com/avatar/#{gravatar_id}"
        image_tag(gravatar_url, alt: user.name, class: 'gravatar')
      end
    end

    # app/views/users/show.html.erb
    <h1>
      <%= gravatar_for @user %>
      <%= @user.name %>
    </h1>


### 在试图中显示调试信息

示例代码：

    # app/views/layouts/application.html.erb
    <!DOCTYPE html>
    <html>
      ...
      <body>
        ...
        <%= render 'layouts/footer' %>
        <%= debug(params) if Rails.env.development? %>
      </body>
    </html>

其中`debug(params)`用于在页面上显示当前的`params`，`if Rails.env.development?`确保调试信息仅在开发模式下显示。

## Controller(控制器)

### 使用强制参数(strong parameters)

参考资料：[Action Controller Overview > 4.5 Strong Parameters](http://edgeguides.rubyonrails.org/action_controller_overview.html#strong-parameters)

示例代码：

    # app/controllers/users_controller.rb
    class UsersController < ApplicationController
      def show
        @user = User.find(params[:id])
        #debugger
      end
      def create
        @user = User.new(user_params)
        if @user.save
          redirect_to @user
        else
          render 'new'
        end
      end
      private
        def user_params
          params.require(:user).permit(:name, :email, :password, :password_confirmation)
        end
    end

也就是说在Rails中，通过GET方式提交的参数不需要使用强制参数，通过POST方式提交的参数必须使用强制参数。

### 使用`byebug`提高调试效率

参考资料：

* [Ruby on Rails Tutorial > Chapter 7 Sign up > 7.1.3 Debugger](https://www.railstutorial.org/book/sign_up#sec-debugger)

示例代码：

    # Rails 5中默认启用
    subl Gemfile

        group :development, :test do
          # Call 'byebug' anywhere in the code to stop execution and get a debugger console
          gem 'byebug', platform: :mri
        end

    # app/controllers/users_controller.rb
    def show
      @user = User.find(params[:id])
      debugger
    end

这样当访问`/users/show/123`页面时，Web服务器就会停止输出并进入`(byebug)`交互模式。

此时可以直接输入变量名以查看其值：

    (byebug) @user.name
    "chinakr"
    (byebug) @user.email
    "chinakr@gmail.com"
    (byebug) user_params[:id]
    "2"

输入`continue`可以继续输出页面。输入`quit`可以使Web服务器停止运行。

输入`help`可以查看byebug的其他使用方法：

    (byebug) help

      break      -- Sets breakpoints in the source code
      catch      -- Handles exception catchpoints
      condition  -- Sets conditions on breakpoints
      continue   -- Runs until program ends, hits a breakpoint or reaches a line
      debug      -- Spawns a subdebugger
      delete     -- Deletes breakpoints
      disable    -- Disables breakpoints or displays
      display    -- Evaluates expressions every time the debugger stops
      down       -- Moves to a lower frame in the stack trace
      edit       -- Edits source files
      enable     -- Enables breakpoints or displays
      finish     -- Runs the program until frame returns
      frame      -- Moves to a frame in the call stack
      help       -- Helps you using byebug
      history    -- Shows byebug's history of commands
      info       -- Shows several informations about the program being debugged
      interrupt  -- Interrupts the program
      irb        -- Starts an IRB session
      kill       -- Sends a signal to the current process
      list       -- Lists lines of source code
      method     -- Shows methods of an object, class or module
      next       -- Runs one or more lines of code
      pry        -- Starts a Pry session
      quit       -- Exits byebug
      restart    -- Restarts the debugged program
      save       -- Saves current byebug session to a file
      set        -- Modifies byebug settings
      show       -- Shows byebug settings
      source     -- Restores a previously saved byebug session
      step       -- Steps into blocks or methods one or more times
      thread     -- Commands to manipulate threads
      tracevar   -- Enables tracing of a global variable
      undisplay  -- Stops displaying all or some expressions when program stops
      untracevar -- Stops tracing a global variable
      up         -- Moves to a higher frame in the stack trace
      var        -- Shows variables and its values
      where      -- Displays the backtrace

### 显示临时信息(flash)

示例代码：

    # app/views/layouts/application.html.erb
    <%= render 'layouts/flash' %>

    # app/views/layouts/_flash.html.erb
    <% flash.each do |message_type, message| %>
      <div class="alert alert-<%= message_type %>"><%= message %></div>
    <% end %>

    # app/controllers/users_controllers.rb
    class UsersController < ApplicationController
      ...
      def create
        @user = User.new(user_params)
        if @user.save
          flash[:success] = 'Welcome to the Sample App!'
          redirect_to @user
        else
          render 'new'
        end
      end
      ...
    end

`flash`方法的语法：

    rails c

        flash = {success: 'It works!', warning: 'It failed!'}
        flash.each do |message_type, message|
          puts "#{message_type}: #{message}"
        end

        输出结果：

            success: It works!
            warning: It failed!


## Rails测试

参考资料：

* Rails Guides > Testing Rails Applicatinos (A Guide to Testing Rails Applications)
    - 测试是Rails内建的重要功能
    - 知识点：测试相关术语，单元测试、功能测试、集成测试，其他常用测试手段和插件
* [Rails Fixtures](http://api.rubyonrails.org/classes/ActiveRecord/FixtureSet.html)
* [Rails fixtures — how do you set foreign keys?](http://stackoverflow.com/questions/510195/rails-fixtures-how-do-you-set-foreign-keys "Google关键字：rails fixtures references")
* [Rails实战测试](https://ihower.tw/rails4/testing.html)
* [How To: Test controllers with Rails 3 and 4 (and RSpec)](https://github.com/plataformatec/devise/wiki/How-To:-Test-controllers-with-Rails-3-and-4-(and-RSpec) "Google关键字：rails devise unit test")

注：以下内容针对MiniTest而非RSpec。

### 术语中英文对照

* Unit Test：单元测试(确保各个组件工作正常；测试粒度最小)
* Functional Test：功能测试
* Integration Test：集成测试
    + 确保不同组件协作正常；测试粒度较大
    + 跨模型、视图和控制器的功能测试代码
    + 模拟了用户和应用程序交互的过程
    + 相对复杂，也更加重要
* Acceptance Test：验收测试(从用户角度测试整个应用程序；测试粒度最大)

### 目的、特性

通过Rails命令行工具自动生成Model和Controller代码时，同时生成了测试骨架代码，这样编写测试代码就变得非常容易。编写和运行测试，主要是为了测试应用程序功能的正确性(正确性)和保证重构后正确性(回归测试，稳定性)。

Rails测试可以模仿Web浏览器请求，并测试应用程序做出的响应，从而避免了在浏览器中手动进行测试。

TDD(测试驱动开发)是先编写测试再编写程序的开发方式，编写程序的目标变成为了通过测试。这是从API使用者的解度看待应用程序，有利于写出更高质量的API。

测试代码也是应用程序的文档，告诉我们如何使用程序提供的API。

有了自动化测试，每次完成新代码后，就不必在Web浏览器中打开相应页面进行手动检查了，只需要运行自动测试即可，这样可以大大提高开发效率，节省开发时间。

### 使用测试的三个好处

1. 避免退化，即开发过程某些功能忽然失效；
2. 更放心地进行代码重构；
3. 作为了解程序运行方式和API设计的示例代码。

### 什么是测试驱动开发(TDD)

测试驱动开发(TDD，Test-Driven Development)要求在编写应用程序代码前先完成测试代码，从而把整个编程过程变成一个编写代码以通过测试的过程。

### 什么时候应该先写测试代码

注：测试代码位于`test/`目录下。

* 如果测试代码比应用程序代码 简单得多，那么应该先写测试代码。
* 对于有安全隐患的功能，应该先写测试代码。

### 什么时候应该先写应用程序代码

注：应用程序代码位于`app/`目录下。

* 如果一边设计一边写程序，那么应该先写应用程序代码 。

### 其他应该写测试代码的情况

* 当程序出现Bug，就应该编写测试代码来触发这个Bug，然后编写应用程序代码 修复这个Bug。
* 对于未来可能需要修改的应用程序代码 ，应该编写测试代码。
* 对于重构过程中可能出错的应用程序代码 ，应该在重构之前编写测试代码。

### 什么情况下可以不写测试代码

* 对于不容易出错，也不太可能需要修改或重构的应用程序代码 ，可以不写测试代码。

### 不同类型测试代码的编写顺序

1. 通常首先编写控制器测试(功能测试)和模型测试(单元测试)代码；
2. 然后编写集成测试代码。

### “红、绿、重构”循环

即先编写会导致测试失败的测试代码(运行`rails test`时显示为红色)，然后编写或修改应用程序代码使测试能够通过(运行`rails test`时显示为绿色)，接下来再重构。测试驱动开发的过程就是“红、绿、重构”循环的过程。

注：在编程一段时间后，应用程序代码通常会变得丑陋、臃肿或同现大量重复代码，这时就需要及时进行重构。

使用`minitest-reporters`gem实现“红、绿”效果：

    subl Gemfile

        group :test do
          gem 'minitest-reporters'
          ...
        end

    subl test/test_helper.rb

        ...
        require 'minitest/reporters'
        Minitest::Reporters.use!

### 向后追踪消音器的使用

用于过滤测试错误提示中的向后追踪信息，以避免错误提示过长。

    subl Gemfile

        group :test do
          ...
          gem 'mini_backtrace'
          ...
        end

    subl config/initializers/backtrace_silencers.rb

        # Be sure to restart your server when you modify this file.
        # You can add backtrace silencers for libraries that you're using but don't wish to see in your backtraces.
        Rails.backtrace_cleaner.add_silencer { |line| line =~ /rvm/ }

    rails s

通过上述配置，包含`rvm`的向后追踪信息都会被过滤掉。

### 使用Guard实现自动化测试

Guard监测文件系统的变化(根据`Guardfile`的配置)，一旦有变化就运行测试。

注：以下代码未测试过。信息来源为“Ruby on Rails Tutorial by Michael Hartl”。

    subl Gemfile

        group :test do
          ...
          gem 'guard'
          gem 'guard-minitest'
        end

    guard init

    subl Guardfile

        # Defines the matching rules for Guard.
        guard :minitest, spring: true, all_on_start: false do
          watch(%r{^test/(.*)/?(.*)_test\.rb$})
          watch('test/test_helper.rb') { 'test' }
          watch('config/routes.rb')    { integration_tests }
          watch(%r{^app/models/(.*?)\.rb$}) do |matches|
            "test/models/#{matches[1]}_test.rb"
          end
          watch(%r{^app/controllers/(.*?)_controller\.rb$}) do |matches|
            resource_tests(matches[1])
          end
          watch(%r{^app/views/([^/]*?)/.*\.html\.erb$}) do |matches|
            ["test/controllers/#{matches[1]}_controller_test.rb"] +
            integration_tests(matches[1])
          end
          watch(%r{^app/helpers/(.*?)_helper\.rb$}) do |matches|
            integration_tests(matches[1])
          end
          watch('app/views/layouts/application.html.erb') do
            'test/integration/site_layout_test.rb'
          end
          watch('app/helpers/sessions_helper.rb') do
            integration_tests << 'test/helpers/sessions_helper_test.rb'
          end
          watch('app/controllers/sessions_controller.rb') do
            ['test/controllers/sessions_controller_test.rb',
             'test/integration/users_login_test.rb']
          end
          watch('app/controllers/account_activations_controller.rb') do
            'test/integration/users_signup_test.rb'
          end
          watch(%r{app/views/users/*}) do
            resource_tests('users') +
            ['test/integration/microposts_interface_test.rb']
          end
        end

        # Returns the integration tests corresponding to the given resource.
        def integration_tests(resource = :all)
          if resource == :all
            Dir["test/integration/*"]
          else
            Dir["test/integration/#{resource}_*.rb"]
          end
        end

        # Returns the controller tests corresponding to the given resource.
        def controller_test(resource)
          "test/controllers/#{resource}_controller_test.rb"
        end

        # Returns all tests for the given resource.
        def resource_tests(resource)
          integration_tests(resource) << controller_test(resource)
        end

    subl .gitignore

        # Ignore Spring files.
        /spring/*.pid

    guard

按回车运行所有测试，按`Ctrl + D`退出Guard。

### 数据库配置

Rails应用程序和数据库关系紧密，测试也一样。因此首先要配置好数据库，并创建测试数据。

Rails应用程序默认有开发、测试、开发三种环境。三种环境下的数据库都在`config/database.yml`中配置。

### 目录结构

测试代码的目录结构：

    ls -F test

        controllers/    helpers/        mailers/        test_helper.rb
        fixtures/       integration/    models/

`test/test_helper.rb`保存了测试的默认配置。通过所有测试代码都包含的`require 'test_helper'`生效。

`test/models/`目录下是单元测试代码(针对Model)，`test/controllers/`目录下是功能测试代码(针对Controller)，`test/integration/`目录下是集成测试代码。

### 测试夹具(fixtures)

参考资料：[Fixture API文档](http://api.rubyonrails.org/classes/ActiveRecord/FixtureSet.html)

`test/fixtures/`目录下是Fixture文件。Fixture是组织测试数据的一种方式，当提到Fixture时指的就是样例数据。Fixture用YAML语言书写，有了Fixture，在测试运行之前我们就有了预定义的数据。在Fixture中，一个文件对应一个Model。

模型校验对测试夹具无效，因此需要注意测试夹具数据是否有效。可以在单元测试中使用测试夹具数据。

Fixture示例代码：

    # test/fixturers/users.html
    tom:
      name: Tom
      character: cat
      age: 3

    jerry:
      name: Jerry
      charactoer: mouse
      age: 2

关联Model的示例代码(`belongs_to`和`has_many`)：

    # In fixtures/categories.yml
    about:
      name: About

    # In fixtures/articles.yml
    one:
      title: Welcome to Rails!
      body: Hello world!
      category: about

对于关联Model，要通过`name`而不是`id`来引用，`id`作为主键应该由Rails在运行时自动生成，以保证一致性。

在Fixture中使用ERB的示例代码(生成1000个用户名和邮件地址)：

    <% 1000.times do |n| %>
    user_<%= n %>:
      username: <%= "user#{n}" %>
      email: <%= "user#{n}@example.com" %>
    <% end %>

在测试代码中使用Fixture的示例代码：

    # this will return the User object for the fixture named david
    users(:david)

    # this will return the property for david called id
    users(:david).id

    # one can also access methods available on the User class
    email(david.girlfriend.email, david.location_tonight)

### 为测试配置环境变量

    # test/controllers/welcome_controller_test.rb
    class WelcomeControllerTest < ActionDispatch::IntegrationTest
      def setup
        @base_tile = 'SEO Optimized Website'
      end
      ...
    end

### 单元测试

注：针对Model的单元测试。默认使用内置的minitest。

单元测试的示例代码-示例代码一：

    rails g scaffold article title:string body:text

        ...
        create  app/models/article.rb
        create  test/models/article_test.rb
        create  test/fixtures/articles.yml
        ...

    subl test/models/article_test.rb

        require 'test_helper'

        class ArticleTest < ActiveSupport::TestCase
          # test "the truth" do
          #   assert true
          # end
        end

`ActiveSupport::TestCase`的父类是`Minitest::Test`，提供了以`test_`开头的方法，用于编写测试。当提到一个测试时，指的就是一个以`test_`开头的方法。`test_password`和`test_valid_password`都是合法的测试名。一个测试用例可以包含多个测试。

`assert`和`assert_not`的功能正好相反，就像`if`和`unless`修饰符那样。

单元测试的示例代码-示例代码二：

    # railg g model User name:string email:string
    # test/models/user_test.rb
    require 'test_helper'
    class UserTest < ActiveSupport::TestCase
      def setup
        @user = User.new(name: 'chinakr', email: 'chinakr@gmail.com')
      end
      test 'should be valid' do
        assert @user.valid?
      end
    end

上面的单元测试中，首先创建了User模型的一条记录，然后测试这条记录是否是合法的。然后可以通过`rails test:models`运行单元测试。

单元测试的示例代码-记录不能重复：

    # railg g model User name:string email:string
    # test/models/user_test.rb
    require 'test_helper'
    class UserTest < ActiveSupport::TestCase
      def setup
        @user = User.new(name: 'chinakr', email: 'chinakr@gmail.com')
      end
      test 'email should be unique' do
        dup_user = @user.dup
        @user.save
        assert_not dup_user.valid?
      end
    end

下面两种定义测试的方法是等价的：

方法一：

    def test_the_truth
      assert true
    end

方法二：

    test "the truth" do
      assert true
    end

运行测试：

    rails test test/models/article_test.rb

或

    rails test test/models/article_test.rb test_the_truth

测试运行的结果，包括了测试数量、断言数量、失败数量、错误数量。其中`F`表示失败，即断言不成立，`E`表示错误，即代码错误。

参考资料：[15 TDD steps to create a Rails application](http://andrzejonsoftware.blogspot.com/2007/05/15-tdd-steps-to-create-rails.html)：在Rails开发中应用TDD(测试驱动开发)方法。

理论上，单元测试应覆盖所有可能出错的地方。实践上，对于Model中的每一个校验和每一个方法，都至少应该编写一个测试。

### 断言

参考资料：[RubyGuides > A Guide to Testing Rails Applications > Available Assertions](http://guides.rubyonrails.org/testing.html#available-assertions)

示例代码：

判断页面标题：

    assert_select 'title', 'The Page Title'

即要求存在`<title>The Page Title</title>`标签。

断言的作用是确保程序按照设计正确运行。Minitest提供了多种类型的断言：

* `assert( test, [msg] )`：确保测试为真。
    + `assert_not( test, [msg] )`：确保测试为假。
* `assert_equal( expected, actual, [msg] )`：确保`expected == actual`为真。
    + `assert_not_equal( expected, actual, [msg] )`：确保`expected != actual`为真。
* `assert_same( expected, actual, [msg] )`：确保`expected.equal?(actual)`为真。
    + `assert_not_same( expected, actual, [msg] )`：确保`expected.equal?(actual)`为假。
* `assert_nil( obj, [msg] )`：确保`obj.nil?`为真。
    + `assert_not_nil( obj, [msg] )`：确保`obj.nil?`为假。
* `assert_empty( obj, [msg] )`：确保`obj.empty?`为真。
    + `assert_not_empty( obj, [msg] )`：确保`obj.empty?`为假。
* `assert_match( regexp, string, [msg] )`：确保字符串和正则表达式匹配。
    + `assert_no_match( regexp, string, [msg] )`：确保字符串和正则表达式不匹配。
* `assert_includes( collection, obj, [msg] )`：确保`obj`(对象)在`collection`(对象的集合)中。
    + `assert_not_includes( collection, obj, [msg] )`：确保`obj`不在`collection`中。
* `assert_in_delta( expecting, actual, [delta], [msg] )`：确保数值`expected`和`actual`的误差在`delta`之内。
    + `assert_not_in_delta( expecting, actual, [delta], [msg] )`：确保数值`expected`和`actual`的误差不在`delta`之内。
* `assert_throws( symbol, [msg] ) { block }`：确保`block`(块)返回`symbol`(符号)。(没太理解)
* `assert_raises( exception1, exception2, ... ) { block }`：确保`block`抛出列出的异常的某一个。
* `assert_nothing_raised( exception1, exception2, ... ) { block }`：确保`block`不抛出列出的异常。
* `assert_instance_of( class, obj, [msg] )`：确保`obj`是`class`的实例。
    + `assert_not_instance_of( class, obj, [msg] )`确保`obj`不是`class`的实例。
* `assert_kind_of( class, obj, [msg] )`：确保`obj`是`class`或其子类的实例(遗传)。
    + `assert_not_kind_of( class, obj, [msg] )`：确保`obj`不是`class`或其子类的实例。
* `assert_respond_to( obj, symbol, [msg] )`：确保`obj`会响应`symbol`。
    + `assert_not_respond_to( obj, symbol, [msg] )`：确保`obj`不会响应`symbol`。
* `assert_operator( obj1, operator, [obj2], [msg] )`：确保`obj1.operator(obj2)`为真。
    + `assert_not_operator( obj1, operator, [obj2], [msg] )`：确保`obj1.operator(obj2)`为假。
* `assert_predicate ( obj, predicate, [msg] )`：确保`obj.predicate`为真，如`assert_predicate str, :empty?`。
    + `assert_not_predicate ( obj, predicate, [msg] )`：确保`obj.predicate`为假，如`assert_predicate str, :empty?`。
* `assert_send( array, [msg] )`：确保对象`array[0]`的方法`array[1]`以参数`array[2]`运行的结果为真。
* `flunk( [msg] )`：确保失败。通常用于标记未编写完成的测试。

参考资料：

* [Minitest API文档](http://docs.seattlerb.org/minitest/)
    + [Minitest::Assertions](http://docs.seattlerb.org/minitest/Minitest/Assertions.html)

Rails测试框架是模块化的，我们可以编写自己的断言。Rails就自定义了一些断言：

* `assert_difference(expressions, difference = 1, message = nil) {...}`：(没太看懂)
* `assert_no_difference(expressions, message = nil, &block)`：确保块运行前后表达式值不变。
* `assert_recognizes(expected_options, path, extras={}, message=nil)`
* `assert_generates(expected_path, options, defaults={}, extras = {}, message=nil)`
* `assert_response(type, message = nil)`
* `assert_redirected_to(options = {}, message=nil)`
* `assert_template(expected = nil, message=nil)`

因为使用场景比较复杂，需要一些例子来理解上述断言的使用方法。

### 功能测试

注：针对Controller的功能测试。

功能测试的目标对象是一个Controller的众多Action。Controller处理Web请求，返回渲染后的View，这一过程的各个环节就早要测试的内容。

`rails g controller ...`命令会生成功能测试代码。这些测试会覆盖控制器的每个动作。

功能测试示例代码：

    # test/controllers/articles_controller_test.rb
    class ArticlesControllerTest < ActionController::TestCase
      test "should get index" do
        get :index
        assert_response :success
        assert_not_nil assigns(:articles)
      end
    end

`get`用法示例：

    get(:show, {'id' => "12"}, {'user_id' => 5})

其中`'id' => "12"`是给出的URL参数，`'user_id' => 5`是对session的设置。

    get(:view, {'id' => '12'}, nil, {'message' => 'booya!'})

其中`'id' => "12"`是给出的URL参数，未设置session，`'message' => 'booya!'`是设置提示信息。

功能测试示例代码：

    test "should create article" do
      assert_difference('Article.count') do
        post :create, article: {title: 'Some title'}
      end

      assert_redirected_to article_path(assigns(:article))
    end

功能测试支持HTTP协议提供的6种请求类型：`get`、`post`、`patch`、`put`、`head`、`delete`。

在发出上述6种请求之一之后，就可以使用4种Hash对象：`assigns`、`cookies`、`flash`、`session`。其中`assigns`是Action中保存的、可以在View中使用的实例变量。示例代码：

    flash["gordon"]
    flash[:gordon]
    session["shmession"]
    session[:shmession]
    cookies["are_good_for_u"]
    cookies[:are_good_for_u]

    # Because you can't use assigns[:something] for historical reasons:
    assigns["something"]
    assigns(:something)

在功能测试中可以使用实例变量`@controller`、`@requrest`、`@response`。

设置HTTP header的示例代码：

    # setting a HTTP Header
    @request.headers["Accept"] = "text/plain, text/html"
    get :index # simulate the request with custom header

设置CGI变量的示例代码：

    # setting a CGI variable
    @request.headers["HTTP_REFERER"] = "http://example.com/home"
    post :create # simulate the request with custom env variable

测试模板和布局：

测试视图：

### 集成测试

在集成测试中可以使用的helper

集成测试示例代码：

    rails g integration_test site_layout

        Running via Spring preloader in process 34567
              invoke  test_unit
              create    test/integration/site_layout_test.rb

    subl test/integration/site_layout_test.rb

        require 'test_helper'
        class SiteLayoutTest < ActionDispatch::IntegrationTest
          # test "the truth" do
          #   assert true
          # end
          test 'layout links' do
            get root_path
            assert_template 'static_pages/home'
            assert_select 'a[href=?]', root_path, count: 2
            assert_select 'a[href=?]', help_path
          end
        end

    rails test:integration

`assert_select`用法示例：

| 代码                                          | 匹配的HTML                       |
|-----------------------------------------------|----------------------------------|
| `assert_select "div"`                         | `<div>foobar</div>`              |
| `assert_select "div", "foobar"`               | `<div>foobar</div>`              |
| `assert_select "div.nav"`                     | `<div class="nav">foobar</div>`  |
| `assert_select "div#profile"`                 | `<div id="profile">foobar</div>` |
| `assert_select "div[name=yo]"`                | `<div name="yo">hey</div>`       |
| `assert_select "a[href=?]", ’/’, count: 1`    | `<a href="/">foo</a>`            |
| `assert_select "a[href=?]", ’/’, text: "foo"` | `<a href="/">foo</a>`            |

示例代码-注册信息不合法时不会创建新用户，合法时会创建新用户：

    rails g integration_test signup

    # test/integration/signup_test.rb
    require 'test_helper'
    class SignupTest < ActionDispatch::IntegrationTest
      test 'invalid signup info' do
        get signup_path
        assert_no_difference 'User.count' do
          post users_path, user: {name: '', email: 'www@example', password: 'password', password_confirmation: 'wrongpassword'}
          assert_template 'users/new'
        end
      end
      test 'valid signup info' do
        get signup_path
        assert_difference 'User.count', 1 do
          post_via_redirect users_path, user: {name: 'example', email: 'www@example.com', password: 'password', password_confirmation: 'password'}
        end
        assert_template 'users/show'
      end
    end

    rails test:integration

其中`assert_no_difference 'User.count' do ... end`认为块运行后表达式`User.count`的值不变，`assert_difference 'User.count', 1 do ... end`认为块运行后表达式`User.count`的值变化是`1`。`get signup_path`以GET方式访问页面，`post users_path, user: {...}`以POST方案提交表单，`post_via_redirect users_path, user: {}`以POST方式提交表单并跳转，`assert_template 'users/new'`认为最后渲染的页面是`users/show`。


### 测试路由

示例代码：

    class ArticleRoutesTest < ActionController::TestCase
      test "should route to article" do
        assert_routing '/articles/1', { controller: "articles", action: "show", id: "1" }
      end

      test "should route to create article" do
        assert_routing({ method: 'post', path: '/articles' }, { controller: "articles", action: "create" })
      end
    end

### 测试helper

### 在命令行运行测试

* `rails test`：运行所有测试。
* `rails test:controllers`：运行`test/controllers/`下的测试。
* `rails test:functionals`：运行`test/controllers/`、`test/mailers/`、`test/functional`下的测试。
* `rails test:helper`：运行`test/helpers/`下的测试。
* `rails test:integration`：运行`test/integration/`下的测试。
* `rails test:jobs`：运行`test/jobs/`下的测试。
* `rails test:mailers`：运行`test/mailers/`下的测试。
* `rails test:models`：运行`test/models/`下的测试。
* `rails test:units`：运行`test/models/`、`test/helpers/`、`test/unit/`下的测试。
* `rails test:db`：运行所有测试并重置数据库。

### 调试Rails应用程序

参考资料：

* [Debugging Rails Applications](http://guides.rubyonrails.org/debugging_rails_applications.html "Google关键字：rails log")
* [Rails 调试和记录日志方法总结](http://rubyer.me/blog/352/ "Google关键字：rails log")


## Rails对Ruby的扩展

注：这些语言特性可以在`rails c`控制台中测试。

检测字符串是否为空白：

    '   '.blank?    # true

控制器的类继承树：

    c = StaticPagesController.new
    c.class    # => StaticPagesController
    c.class.superclass    # => ApplicationController
    c.class.superclass.superclass    # => ActionController::Base
    c.class.superclass.superclass.superclass    # => ActionController::Metal
    c.class.superclass.superclass.superclass.superclass    # => AbstractController::Base
    c.class.superclass.superclass.superclass.superclass.superclass    # => Object
    c.class.superclass.superclass.superclass.superclass.superclass.superclass    # => BasicObject

## 实用技巧

### 设置时区

参考资料：[How to set Rails config.time_zone to GMT +6?](http://stackoverflow.com/questions/25306167/how-to-set-rails-config-time-zone-to-gmt-6)


    rails time:zones:all OFFSET=+8

        * UTC +08:00 *
        Beijing
        Chongqing
        Hong Kong
        Irkutsk
        Kuala Lumpur
        Perth
        Singapore
        Taipei
        Ulaanbaatar

    subl config/application.rb

        config.time_zone = 'Beijing'


注：设置后重新运行`rails s`，即可通过`Time.now.to_datetime`获得当前时区的日期时间。

### 要求表单字段不为空

参考资料：[Active Record Validations](http://guides.rubyonrails.org/active_record_validations.html)

subl app/models/order.rb

### 下拉列表的默认提示信息

参考资料：[select_tag](http://apidock.com/rails/ActionView/Helpers/FormTagHelper/select_tag)


    <%= select_tag 'order[product_id]', options_for_select(['请选择课程'] + @product_options || []) %>

### 自动选中文本框

默认选中添加词的文本框：

参考资料：[how to focus a form input field when page loaded](http://stackoverflow.com/questions/5243539/how-to-focus-a-form-input-field-when-page-loaded "Google关键字：rails jquery input focus")

示例代码：

    <%= f.text_field :content, autofocus: true %>

### 文本框输入自动补全

参考资料：

* [rails search autocomplete](https://www.youtube.com/watch?v=iMz8HmrQ350 "Google关键字：rails search autocomplete")
* [Creating Autocomplete Dropdowns with the Datalist Element](http://blog.teamtreehouse.com/creating-autocomplete-dropdowns-datalist-element "Google关键字：foundation autocomplete input")
* [Autocomplete Ruby on Rails form_for using HTML5 Datalist](http://stackoverflow.com/questions/25163982/autocomplete-ruby-on-rails-form-for-using-html5-datalist "Google关键字：rails autocomplete input datalist")
* [Creating Autocomplete datalist Controls](http://www.sitepoint.com/creating-autocomplete-datalist-controls/ "Google关键字：datalist autocomplete ajax rails")
* [jQuery AJAX HTML5 Datalist Autocomplete Example](http://www.sitepoint.com/jquery-ajax-html5-datalist-autocomplete/ "Google关键字：datalist autocomplete ajax coffeescript")


## 手工实现用户认证功能(Authentication)

功能设计：

* 用户注册
* 用户登录
* 用户详细页
* 重新设置用户密码
* 用户退出

数据表设计-`users`数据表：

| 字段  | 类型    |
|-------|---------|
| id    | integer |
| name  | string  |
| email | string  |

gem相关代码：

    subl Gemfile

        ...
        gem 'bcrypt', '3.1.11'

    bundle

URL路由相关代码：

    subl config/routest.rb

        get 'signup' => 'users#new'
        resources :users

视图相关代码：

    subl app/views/layouts/application.html.erb

        <!DOCTYPE html>
        <html>
          <head>
            <title><%= full_title yield(:title) %></title>
            <%= csrf_meta_tags %>

            <%= stylesheet_link_tag    'application', media: 'all', 'data-turbolinks-track': 'reload' %>
            <%= javascript_include_tag 'application', 'data-turbolinks-track': 'reload' %>
            <!--[if lt IE 9]>
              <script src="//cdnjs.cloudflare.com/ajax/libs/html5shiv/r29/html5.min.js">
              </script>
            <![endif]-->
          </head>
          <body>
            <div class="container">
              <%= render 'layouts/header' %>
            </div>
            <div class="container">
              <div class="row">
                <div class="col-sm-12">
                  <%= render 'layouts/flash' %>
                  <%= yield %>
                </div>
              </div>
              <div class="row">
                <div class="col-sm-12">
                  <p><%= debug(params) if Rails.env.development? %></p>
                </div>
              </div>
            </div>
          </body>
        </html>

    subl app/views/layouts/_header.html.erb

        <nav class="navbar navbar-inverse">
          <%= link_to 'Sample App', root_path, id: 'logo', class: 'navbar-brand' %>
          <ul class="nav navbar-nav navbar-right">
            <li class="nav-item">
              <%= link_to 'Home', root_path, class: 'nav-link' %>
            </li>
            <li class="nav-item">
              <%= link_to 'Help', help_path, class: 'nav-link' %>
            </li>
            <li class="nav-item">
              <%= link_to 'Log in', signup_path, class: 'nav-link' %>
            </li>
          </ul>
        </nav>

    subl app/views/layouts/_flash.html.erb

        <% flash.each do |message_type, message| %>
          <div class="alert alert-<%= message_type %>"><%= message %></div>
        <% end %>

    subl app/views/shared/_error_messages.html.erb

        <% if @user.errors.any? %>
          <div class="error-explanation">
            <div class="alert alert-danger" role="alert">
              The form contains <%= pluralize(@user.errors.count, 'error') %>
            </div>
            <ul>
            <% @user.errors.full_messages.each do |msg| %>
              <li><%= msg %></li>
            <% end %>
            </ul>
          </div>
        <% end %>

    subl app/views/users/new.html.erb

        <% provide :title, 'Sign up' %>
        <h1>Sign up</h1>
        <div class="row">
          <div class="col-sm-6 col-sm-offset-3">
            <%= form_for(@user) do |f| %>
              <%= render 'shared/error_messages' %>
              <fieldset class="form-group">
                <%= f.label :name %>
                <%= f.text_field :name, class: 'form-control' %>
              </fieldset>
              <fieldset class="form-group">
                <%= f.label :email %>
                <%= f.email_field :email, class: 'form-control' %>
              </fieldset>
              <fieldset class="form-group">
                <%= f.label :password %>
                <%= f.password_field :password, class: 'form-control' %>
              </fieldset>
              <fieldset class="form-group">
                <%= f.label :password_confirmation, 'Confirmation' %>
                <%= f.password_field :password_confirmation, class: 'form-control' %>
              </fieldset>
              <%= f.submit 'Create account', class: 'btn btn-primary' %>
            <% end %>
          </div>
        </div>

    subl app/ivew/users/show.html.erb

        <% provide :title, @user.name %>
        <div class="row">
          <aside class="col-sm-4">
            <section class="user_info">
              <h1>
                <%= gravatar_for @user %>
                <%= @user.name %>
              </h1>
            </section>
          </aside>
        </div>

模型相关代码：

    rails g model User name:string email:string password_digest:string
    rails db:migrate

注：在生成控制器时使用`Users`，在生成模型时使用`User`。生成的数据表是`users`，对模型类的引用是`User`。

    subl app/models/user.rb

        class User < ApplicationRecord
          before_save {email.downcase!}
          validates :name, presence: true
          validates :email, presence: true, length: {maximum: 140}, format: {with: /\A[\w+\-.]+@[a-z\d\-.]+\.[a-z]+\z/i}, uniqueness: {case_sensitive: false}
          has_secure_password
          validates :password, presence: true, length: {minimum: 6}
        end

控制器相关代码：

    rails g controller Users new create

测试相关代码：

    subl test/models/user_test.rb

        require 'test_helper'
        class UserTest < ActiveSupport::TestCase
          def setup
            @user = User.create(name: 'chinakr', email: 'chinakr@gmail.com', password: 'helloworld', password_confirmation: 'helloworld')
          end
          test 'should be valid' do
            assert @user.valid?
          end
          test 'name should not be blank' do
            @user.name = ''
            assert_not @user.valid?
          end
          test 'email should not be too long' do
            @user.email = 'a' * 255 + '@example.com'
            assert_not @user.valid?
          end
          test 'email should be unique' do
            dup_user = @user.dup
            dup_user.email = dup_user.email.upcase
            @user.save
            assert_not dup_user.valid?
          end
          test 'password should not be blank' do
            @user.password = @user.password_confirmation = ' ' * 6
            assert_not @user.valid?
          end
          test 'password should have more than 6 characters' do
            @user.password = @user.password_confirmation = 'a' * 5
            assert_not @user.valid?
          end
          test 'email should be saved as lower-case' do
            mixed_case_email = 'WWW@example.Com'
            @user.email = mixed_case_email
            @user.save
            assert_equal mixed_case_email.downcase, @user.reload.email
          end
        end

    rails test:models

    rails g integration_test signup

    subl test/integration/signup_test.rb

        require 'test_helper'
        class SignupTest < ActionDispatch::IntegrationTest
          test 'invalid signup info' do
            get signup_path
            assert_no_difference 'User.count' do
              post users_path, user: {name: '', email: 'www@example', password: 'password', password_confirmation: 'wrongpassword'}
              assert_template 'users/new'
            end
          end
          test 'valid signup info' do
            get signup_path
            assert_difference 'User.count', 1 do
              post_via_redirect users_path, user: {name: 'example', email: 'www@example.com', password: 'password', password_confirmation: 'password'}
            end
            assert_template 'users/show'
          end
        end

    rails test:integration

在控制台进行语法测试代码：

    rails c

        user = User.new(name: 'chinakr', email: 'chinakr@gmail.com')
        user.valid?    # => true
        user.save

        user = User.find(1)
        user.name    # => "chinakr"
        user.email    # => "chinakr@gmail.com"
        user.updated_at


## 实现邮件提醒功能

参考资料：

  * [Action Mailer Basics](http://guides.rubyonrails.org/action_mailer_basics.html)
  * [ActionMailer::Base < AbstractController::Base](http://api.rubyonrails.org/classes/ActionMailer/Base.html)

配置ActionMailer：


    subl config/environments/development.rb
    subl config/environments/production.rb

          # Mailer settings
          config.action_mailer.delivery_method = :smtp
          config.action_mailer.smtp_settings = {
            address:              'smtp.exmail.qq.com',
            port:                 465,
            domain:               'exmail.qq.com',
            user_name:            'bm@mail.haijia.org',
            password:             'z1HfMk4VwDX7',
            authentication:       'login',
            ssl:                  true,
          }


注：只有上传到远程服务器后，发送的邮件才能被收到。不要浪费时间在本地白折腾了！

创建mailer模型：


    rails g mailer UserMailer

        Running via Spring preloader in process 34576
              create  app/mailers/user_mailer.rb
              invoke  erb
              create    app/views/user_mailer
              invoke  test_unit
              create    test/mailers/user_mailer_test.rb
              create    test/mailers/previews/user_mailer_preview.rb

    subl app/mailers/application_mailer.rb

        class ApplicationMailer < ActionMailer::Base
          default from: 'bm@mail.haijia.org'
          layout 'mailer'
        end

    subl app/mailers/user_mailer.rb

        class UserMailer < ApplicationMailer
          def new_order_email(order)
            # both name and mobile should be valid
            if order.name.length == 0 or order.mobile.length <= 8
              return
            end
            email = 'houyx@mail.haijia.org'
            content_type = 'text/html'
            subject = "在线报名：#{order.name}，#{order.mobile}"
            @order = order
            mail(to: email, content_type: content_type, subject: subject) do |format|
              format.html
            end
          end
        end


创建邮件模板：


    subl app/views/user_mailer/new_order_email.text.erb

        <ul>
          <li>姓名：<%= @order.name %></li>
          <li>手机：<%= @order.mobile %></li>
          <li>课程：<%= @order.product.name + '，' + @order.product.price.to_s + '元' %></li>
          <li>备注：<%= @order.note %></li>
        </ul>


在控制器中发送邮件：


    subl app/controllers/orders_controller.rb

        UserMailer.new_order_email(@order).deliver_now


## 用devise实现用户认证

### 参考资料

  * [devise项目主页](https://github.com/plataformatec/devise)
  * [devise Wiki](https://github.com/plataformatec/devise/wiki)
  * [使用者認證](https://ihower.tw/rails4/auth.html)
  * [alias_method_chain fix for Devise with Rails 5 API?](http://stackoverflow.com/questions/33072535/alias-method-chain-fix-for-devise-with-rails-5-api)

### 使用方法


    subl Gemfile

        # Background authentication
        gem 'devise'


注：对于Rails 5应使用


        # Background authentication
        gem "devise", '~> 4.0.0.rc1'

    bundle

    rails g devise:install

        Running via Spring preloader in process 25032
              create  config/initializers/devise.rb
              create  config/locales/devise.en.yml
        ===============================================================================

        Some setup you must do manually if you haven't yet:

          1. Ensure you have defined default url options in your environments files. Here
             is an example of default_url_options appropriate for a development environment
             in config/environments/development.rb:

               config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

             In production, :host should be set to the actual host of your application.

          2. Ensure you have defined root_url to *something* in your config/routes.rb.
             For example:

               root to: "home#index"

          3. Ensure you have flash messages in app/views/layouts/application.html.erb.
             For example:

               <p class="notice"><%= notice %></p>
               <p class="alert"><%= alert %></p>

          4. If you are deploying on Heroku with Rails 3.2 only, you may want to set:

               config.assets.initialize_on_precompile = false

             On config/application.rb forcing your application to not access the DB
             or load models when precompiling your assets.

          5. You can copy Devise views (for customization) to your app by running:

               rails g devise:views

        ===============================================================================

    subl config/environments/development.rb

        # default url required by devise
        config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

    subl config/environments/production.rb

        # default url required by devise
        config.action_mailer.default_url_options = { host: 'bm.haijia.net.cn', port: 80 }

    subl config/routes.rb

        root to: 'orders#new'

    subl app/views/layouts/application.html.erb

        <p class="notice"><%= notice %></p>
        <p class="alert"><%= alert %></p>

    rails g devise user

        Running via Spring preloader in process 25219
              invoke  active_record
              create    db/migrate/20160323040632_devise_create_users.rb
              create    app/models/user.rb
              invoke    test_unit
              create      test/models/user_test.rb
              create      test/fixtures/users.yml
              insert    app/models/user.rb
               route  devise_for :users

    rails db:migrate

    subl app/controllers/products_controller.rb

        before_action :authenticate_user!

    subl app/controllers/centers_controller.rb

        before_action :authenticate_user!

    subl app/controllers/orders_controller.rb

        before_action :authenticate_user!, only: [:show, :edit, :update, :destroy]

    subl app/views/layouts/application.html.erb

    mkdir app/views/application/

    subl app/views/application/_nav.html.erb

        <ul class="menu align-right">
          <li><%= link_to '退出', destroy_user_session_path, :method => :delete %></li>
          <li><%= link_to current_user.email, edit_registration_path(:user) %></li>
          <li><%= link_to '报名中心', centers_path %></li>
          <li><%= link_to '课程', products_path %></li>
          <li><%= link_to '订单', orders_path %></li>
        </ul>

    subl app/views/layouts/application.html.erb

        <% if current_user %>
          <%= render 'nav' %>
        <% end %>


配置完成后需要重新运行`rails s`。

### 添加admin属性

参考资料：

  * [How To: Add an Admin Role](https://github.com/plataformatec/devise/wiki/How-To:-Add-an-Admin-role)：Option 2: Adding an admin attribute
  * [Access devise current_user variable in rails controller](http://stackoverflow.com/questions/19147729/access-devise-current-user-variable-in-rails-controller)：判断是否为admin
  * [Devise before_filter authenticate_admin?](http://stackoverflow.com/questions/7411577/devise-before-filter-authenticate-admin)：仅允许admin访问
  * [Rails 4: before_filter vs. before_action](http://stackoverflow.com/questions/16519828/rails-4-before-filter-vs-before-action)：As we can see in ActionController::Base, before_action is just a new syntax for before_filter. However all before_filters are deprecated in Rails 5.0 and will be removed in Rails 5.1

添加admin属性的方法：


    rails g migration add_admin_to_users admin:boolean

        Running via Spring preloader in process 39281
              invoke  active_record
              create    db/migrate/20160323105143_add_admin_to_users.rb

    subl db/migrate/20160323105143_add_admin_to_users.rb

        class AddAdminToUsers < ActiveRecord::Migration[5.0]
          def change
            add_column :users, :admin, :boolean, default: false
          end
        end

    rails db:migrate

        == 20160323105143 AddAdminToUsers: migrating ==================================
        -- add_column(:users, :admin, :boolean, {:default=>false})
           -> 0.0078s
        == 20160323105143 AddAdminToUsers: migrated (0.0078s) =========================

    rails g controller admin activate deactivate

        Running via Spring preloader in process 39977
              create  app/controllers/admin_controller.rb
               route  get 'admin/deactivate'
               route  get 'admin/activate'
              invoke  erb
              create    app/views/admin
              create    app/views/admin/activate.html.erb
              create    app/views/admin/deactivate.html.erb
              invoke  test_unit
              create    test/controllers/admin_controller_test.rb
              invoke  helper
              create    app/helpers/admin_helper.rb
              invoke    test_unit
              invoke  assets
              invoke    coffee
              create      app/assets/javascripts/admin.coffee
              invoke    scss
              create      app/assets/stylesheets/admin.scss

    subl app/controllers/admin_controller.rb

        class AdminController < ApplicationController
          before_action :authenticate_user!

          def activate
            if current_user.try(:admin?)
              redirect_to orders_url, notice: 'You are already admin.'
            else
              current_user.update_attribute :admin, true
              redirect_to orders_url, notice: 'You are now admin.'
            end
          end

          def deactivate
            if current_user.try(:admin?)
              current_user.update_attribute :admin, false
              redirect_to orders_url, notice: 'You are no longer admin.'
            else
              redirect_to orders_url, notice: 'You are not admin.'
            end
          end
        end

    firefox http://localhost:3000/admin/activate
    firefox http://localhost:3000/admin/activate
    firefox http://localhost:3000/admin/deactivate
    firefox http://localhost:3000/admin/deactivate


在命令行查询当前用户：


    rails console
    User.all


在命令行删除指定用户：

参考资料：[Deleting a User record from rails console](http://stackoverflow.com/questions/21845735/deleting-a-user-record-from-rails-console)


    rails console
    user = User.where(email: 'chinakr@gmail.com')
    user.delete_all


在命令行添加用户：

参考资料：[How to create the first (Admin) user (CanCan and Devise)?](http://stackoverflow.com/questions/5149773/how-to-create-the-first-admin-user-cancan-and-devise)


    rails console
    user = User.create(email: 'www@example.com', password: 'helloworld')


禁示通过Web注册用户：

参考资料：[Rails: Add a before_action to a Devise generated admin controller?](http://stackoverflow.com/questions/23171297/rails-add-a-before-action-to-a-devise-generated-admin-controller)


    subl app/models/user.rb

        class User < ApplicationRecord
          # Include default devise modules. Others available are:
          # :confirmable, :lockable, :timeoutable and :omniauthable
          # :registerable
          devise :database_authenticatable, :recoverable,
                 :rememberable, :trackable, :validatable
        end

    subl app/views/application/_nav.html.erb

        <li><%= link_to current_user.email, '#' %></li>


注：因为禁用了Web注册，Web下修改密码也失效了，`edit_registration_path(:user)`也就不能用了。


## 使用Cancan实现用户授权

注：Devise for authentication, Cancan for authorisation。

略。


## Rails应用的部署

注：以下为手动部署的过程。自动化部署请参考`Capistrano笔记`。

### 部置相关知识点

* 本地和远程服务器的关系
* Git和Mina的关系
* Mina和Puma的关系
* Puma和nginx的关系

### 首次部署

参考资料：

  * [How To Deploy a Rails App with Puma and Nginx on Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-rails-app-with-puma-and-nginx-on-ubuntu-14-04)：主要参考资料，除数据库和rbenv部分外基本都照做了。
  * [Deploying a Rails App on Ubuntu 14.04 with Capistrano, Nginx, and Puma](https://www.digitalocean.com/community/tutorials/deploying-a-rails-app-on-ubuntu-14-04-with-capistrano-nginx-and-puma)
    * [A Basic MySQL Tutorial](https://www.digitalocean.com/community/tutorials/a-basic-mysql-tutorial)
    * [How To Use MySQL with Your Ruby on Rails Application on Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-use-mysql-with-your-ruby-on-rails-application-on-ubuntu-14-04)
  * [Deploy Ruby On Rails on Ubuntu 14.04 Trusty Tahr](https://gorails.com/deploy/ubuntu/14.04)

关键字：rvm, ruby, gem, rails, bundler, nginx, puma, mysql

    sudo adduser deploy
    sudo adduser deploy sudo
    su deploy

在本地：

    brew install ssh-copy-id
    ssh-copy-id deploy@bm.haijia.net.cn

本地操作结束。

    sudo aptitude update; sudo aptitude upgrade -y
    sudo aptitude install curl

参考资料：[Installed Ruby 1.9.3 with RVM but command line doesn't show ruby -v](http://stackoverflow.com/questions/9056008/installed-ruby-1-9-3-with-rvm-but-command-line-doesnt-show-ruby-v/9056395#9056395)

    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
    \curl -L https://get.rvm.io | bash -s stable

退出并重新登录。

参考资料：[RubyGems 镜像 - 淘宝网](https://ruby.taobao.org/ "国内使用必不可少，rvm、gem和bundle都需要设置")

    rvm install 2.3.0
    rvm use 2.3.0 --default
    ruby -v
    rvm gemset create rails5
    rvm use 2.3.0@rails5 --default
    rvm gemset list

参考资料：[Installing Nokogiri > Ubuntu / Debian](http://www.nokogiri.org/tutorials/installing_nokogiri.html#ubuntu___debian)

    sudo aptitude install build-essential patch
    gem install rails -v 5.0.0.beta3 --no-rdoc --no-ri --verbose
    rails -v

    mkdir -p ~/bm.haijia.net.cn/

在本地：

    cd ~/workspace/ruby/rails/
    tar czvf signup_2016-03-23_01.tar.gz signup/
    scp signup_2016-03-23_01.tar.gz deploy@bm.haijia.net.cn:/home/deploy/bm.haijia.net.cn/

本地操作结束。

    cd ~/bm.haijia.net.cn/
    tar zxvf signup_2016-03-23_01.tar.gz
    cd signup/

参考资料：

  * [使用阿里云镜像服务器](http://theo.im/blog/2014/05/20/use-aliyun-mirror-to-boost-up-download-speed/)
  * [RubyGems 镜像 - 淘宝网](https://ruby.taobao.org/)

继续操作：

    # gem source -r https://rubygems.org/
    # gem source -a http://mirrors.aliyun.com/rubygems/
    # gem source -a https://rubygems.org/
    # gem sources -l
    # gem update
    # sed -i 's!https://rubygems.org!http://mirrors.aliyun.com/rubygems/!' Gemfile
    bundle

注：使用阿里云的gem镜像会遇到`Could not find rake-11.1.1 in any of the sources`的问题，因此哪怕网速慢一点也只能使用官方gem源了。(注：这个问题已解决，可以使用了。2016-04-18)

参考资料：[There was an error while trying to load the gem 'uglifier'. (Bundler::GemRequireError)](http://stackoverflow.com/questions/34420554/there-was-an-error-while-trying-to-load-the-gem-uglifier-bundlergemrequire)

    sudo aptitude install nodejs
    rails s
    sudo aptitude install lynx

参考资料：wget笔记 > 中文显示乱码的问题

    locale -a
    sudo locale-gen zh_CN.UTF-8
    lynx localhost:3000

    cd ~/bm.haijia.net.cn/signup/

    vim config/puma.rb

        # Change to match your CPU core count
        workers 4

        # Min and Max threads per worker
        threads 1, 6

        app_dir = File.expand_path("../..", __FILE__)
        shared_dir = "#{app_dir}/shared"

        # Default to production
        rails_env = ENV['RAILS_ENV'] || "production"
        environment rails_env

        # Set up socket location
        bind "unix://#{shared_dir}/sockets/puma.sock"

        # Logging
        stdout_redirect "#{shared_dir}/log/puma.stdout.log", "#{shared_dir}/log/puma.stderr.log", true

        # Set master PID and state locations
        pidfile "#{shared_dir}/pids/puma.pid"
        state_path "#{shared_dir}/pids/puma.state"
        activate_control_app

        on_worker_boot do
          require "active_record"
          ActiveRecord::Base.connection.disconnect! rescue ActiveRecord::ConnectionNotEstablished
          ActiveRecord::Base.establish_connection(YAML.load_file("#{app_dir}/config/database.yml")[rails_env])
        end

    mkdir -p shared/pids shared/sockets shared/log

    cd
    wget https://raw.githubusercontent.com/puma/puma/master/tools/jungle/upstart/puma-manager.conf
    wget https://raw.githubusercontent.com/puma/puma/master/tools/jungle/upstart/puma.conf

    vim puma.conf

        setuid deploy
        setgid deploy

    sudo cp puma.conf puma-manager.conf /etc/init
    rm puma.conf puma-manager.conf

    sudo vim /etc/puma.conf

        /home/deploy/bm.haijia.net.cn/signup

    cd /etc/nginx/sites-available/

    sudo vim bm.haijia.net.cn

        upstream app {
            # Path to Puma SOCK file, as defined previously
            server unix:///home/deploy/bm.haijia.net.cn/signup/shared/sockets/puma.sock fail_timeout=0;
        }

        server {
            listen 80;
            server_name bm.haijia.net.cn;

            root /home/deploy/bm.haijia.net.cn/signup/public;

            try_files $uri/index.html $uri @app;

            location @app {
                proxy_pass http://app;
                proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
                proxy_set_header Host $http_host;
                proxy_redirect off;
            }

            error_page 500 502 503 504 /500.html;
            client_max_body_size 4G;
            keepalive_timeout 10;
        }

    cd ../sites-enabled/
    sudo ln -s ../sites-available/bm.haijia.net.cn .
    sudo nginx -t
    sudo service nginx restart

参考资料：[How to solve error “Missing `secret_key_base` for 'production' environment” on Heroku](http://stackoverflow.com/questions/23180650/how-to-solve-error-missing-secret-key-base-for-production-environment-on-h)

    sudo start puma-manager
    lynx http://bm.haijia.net.cn/
    less shared/log/puma.stderr.log
    sudo less /var/log/nginx/error.log
    less log/production.log

注：nginx、puma、rails三关都过了，应用才能正常运行。

    RAILS_ENV=production rails secret

        GENERATED_CODE

    vim ~/.bash_profile

        export SECRET_KEY_BASE=GENERATED_CODE

    source ~/.bash_profile
    echo $SECRET_KEY_BASE

    sudo vim /etc/init/puma.conf

        export SECRET_KEY_BASE=GENERATED_CODE

以上两处对`SECRET_KEY_BASE`的设置均未起作用，于是

    vim config/secrets.yml

        production:
          secret_key_base: GENERATED_CODE

    sudo start puma-manager
    RAILS_ENV=production rails db:migrate
    RAILS_ENV=production rails db:seed
    RAILS_ENV=production rails assets:precompile

参考资料：[Why does stylesheet_link_tag not link to /assets in production?](http://stackoverflow.com/questions/8824734/why-does-stylesheet-link-tag-not-link-to-assets-in-production)

    vim config/application.rb

        config.assets.digest = true

    sudo restart puma-manager
    lynx http://bm.haijia.net.cn/

    RAILS_ENV=production rails console

        User.all.delete_all
        User.create(email: 'chinakr@gmail.com', password: 'PASSWORD')


注：对生产环境进行操作时千万别忘了`RAILS_ENV=production`！

### 手动更新代码

更新部分代码：

    scp -r app/ deploy@bm.haijia.net.cn:/home/deploy/bm.haijia.net.cn/signup/
    scp -r config/ deploy@bm.haijia.net.cn:/home/deploy/bm.haijia.net.cn/signup/

更新全部代码：

    scp -r * deploy@bm.haijia.net.cn:/home/deploy/bm.haijia.net.cn/signup/

### 在一台服务器上部署多个Rails应用程序

参考资料：

* [Question about multiple Rails apps on one server, and integrating with Apache](https://www.reddit.com/r/rails/comments/27y0if/question_about_multiple_rails_apps_on_one_server/ "Google关键字：multiple rails app on one server")：参考价值不大。

第二个Rails应用程序的部署过程：

    subl /etc/hosts

        123.56.193.84 hk.haijia.net.cn

    # use deploy:deploy for deployment which is required by puma
    ssh deploy@hk.haijia.net.cn
    mkdir -p ~/hk.haijia.net.cn/journal/

    # 本地操作
    cd ~/workspace/ruby/rails/
    tar czvf journal_2016-04-18_01.tar.gz journal/
    scp journal_2016-04-18_01.tar.gz deploy@hk.haijia.net.cn:/home/deploy/hk.haijia.net.cn/
    ssh deploy@hk.haijia.net.cn

    cd ~/hk.haijia.net.cn/
    tar zxvf journal_2016-04-18_01.tar.gz
    cd journal/
    bundle config mirror.https://rubygems.org https://ruby.taobao.org
    bundle

    mv config/puma.rb config/puma.rb.old
    vim config/puma.rb

        # Change to match your CPU core count
        workers 4

        # Min and Max threads per worker
        threads 1, 6

        app_dir = File.expand_path("../..", __FILE__)
        shared_dir = "#{app_dir}/shared"

        # Default to production
        rails_env = ENV['RAILS_ENV'] || "production"
        environment rails_env

        # Set up socket location
        bind "unix://#{shared_dir}/sockets/puma.sock"

        # Logging
        stdout_redirect "#{shared_dir}/log/puma.stdout.log", "#{shared_dir}/log/puma.stderr.log", true

        # Set master PID and state locations
        pidfile "#{shared_dir}/pids/puma.pid"
        state_path "#{shared_dir}/pids/puma.state"
        activate_control_app

        on_worker_boot do
          require "active_record"
          ActiveRecord::Base.connection.disconnect! rescue ActiveRecord::ConnectionNotEstablished
          ActiveRecord::Base.establish_connection(YAML.load_file("#{app_dir}/config/database.yml")[rails_env])
        end

    mkdir -p shared/pids shared/sockets shared/log

    RAILS_ENV=production rails secret

        GENERATED_CODE

    vim config/secrets.yml

        production:
          secret_key_base: GENERATED_CODE

    RAILS_ENV=production rails db:reset
    RAILS_ENV=production rails assets:precompile

    vim config/application.rb

        config.assets.digest = true

    sudo vim /etc/puma.conf

        /home/deploy/hk.haijia.net.cn/journal

    cd /etc/nginx/sites-available/

    sudo vim hk.haijia.net.cn

        # name journal should be unique for each site and will be used for several times
        upstream journal {
            # Path to Puma SOCK file, as defined previously
            server unix:///home/deploy/hk.haijia.net.cn/journal/shared/sockets/puma.sock fail_timeout=0;
        }

        server {
            listen 80;
            server_name hk.haijia.net.cn;

            root /home/deploy/hk.haijia.net.cn/journal/public;

            try_files $uri/index.html $uri @journal;

            location @journal {
                proxy_pass http://journal;
                proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
                proxy_set_header Host $http_host;
                proxy_redirect off;
            }

            error_page 500 502 503 504 /500.html;
            client_max_body_size 4G;
            keepalive_timeout 10;
        }

    cd ../sites-enabled/
    sudo ln -s ../sites-available/hk.haijia.net.cn .
    sudo nginx -t
    sudo service nginx restart
    sudo restart puma-manager

    # 本地操作
    firefox http://hk.haijia.net.cn/

部署成功！

### 启用SSL(https)

1.修改生产环境配置文件：

    subl config/environments/production.rb

        config.force_ssl = true

2.购买SSL认证服务。

3.为Web服务器配置SSL。

当把应用程序部署在Heroku上时，步骤2、3可以省略。


### Rails应用程序的自动化部署

参考：[用nginx+Puma+Mina部署Rails应用程序](rails-deploy-nginx-puma-mina.md)

### 把Rails应用程序部署到Heroku

参考资料：

* [Heroku官网](https://www.heroku.com/)
    + [Getting Started with Rails 4.x on Heroku](https://devcenter.heroku.com/articles/getting-started-with-rails4)

把Rails应用程序部署到Heroku十分简单，部署需要使用Git。如果流量不大，使用Heroku通常都是免费的。

Heroku使用PostgreSQL数据库：

    subl Gemfile

        group :development, :test do
          gem 'sqlite3'
        end

        group :test do
          gem 'minitest-reporters'
          gem 'mini_backtrace'
          gem 'guard'
          gem 'guard-minitest'
        end

        group :production do
          gem 'pg'
          gem 'rails_12factor'
        end

    bundle --without production

    git commit -a -m 'Update Gemfile.lock for Heroku.'

其中`pg`gem提供PostgreSQL数据库支持；`rails_12factor`gem提供asset支持(也就是可以访问CSS、JS、图片等静态文件)；`--without production`选项使`bundle`不会把生产环境的gem安装到本地(如`pg`和`rails_12factor`)。

注：如果缺少了`gem 'guard'`这一行，在运行`rails test`时就遇到`LoadError: cannot load such file -- guard`错误。可参考[Minitest Issues Ruby on Rails](http://stackoverflow.com/questions/28685584/minitest-issues-ruby-on-rails)。

如果系统中已经安装了Heroku命令行客户端：

    heroku version

        heroku-toolbelt/3.43.3 (x86_64-linux) ruby/2.3.0
        heroku-cli/5.2.20-9d094b0 (linux-amd64) go1.6.2
        You have no installed plugins.

添加SSH密钥到Heroku：

    heroku login

        Enter your Heroku credentials.
        Email: chinakr@gmail.com
        Password (typing will be hidden):
        Logged in as chinakr@gmail.com

    heroku keys:add

        Heroku CLI submits usage information back to Heroku. If you would like to disable this, set `skip_analytics: true` in /home/ubuntu/.heroku/config.json
        Found an SSH public key at /home/ubuntu/.ssh/id_rsa.pub
        ? Would you like to upload it to Heroku? Yes
        Uploading /home/ubuntu/.ssh/id_rsa.pub SSH key... done

在Heroku上为Rails应用程序创建空间：

    heroku create

        Creating app... done, ⬢ powerful-brook-32947
        https://powerful-brook-32947.herokuapp.com/ | https://git.heroku.com/powerful-brook-32947.git

    firefox https://powerful-brook-32947.herokuapp.com/

把Rails应用程序部署到Heroku：

    git push heroku master

    firefox https://powerful-brook-32947.herokuapp.com/

注：

1. 在本地可以使用`heroku open`打开Heroku上的Rails应用程序。
2. 之后可以用`git push heroku`完成代码推送。

在Heroku上应用数据库迁移(migrations)：

    heroku run rails db:migrate

为应用程序指定二级域名：

    irb

        2.3.1 :001 > ('a'..'z').to_a.shuffle[0..7].join
         => "bztonxmy"

    heroku rename bztonxmy

        Renaming powerful-brook-32947 to bztonxmy... done
        https://bztonxmy.herokuapp.com/ | https://git.heroku.com/bztonxmy.git
        Git remote heroku updated
         ▸    Don't forget to update git remotes for all other local checkouts of the app.

    firefox https://bztonxmy.herokuapp.com/

其他可用的Heroku命令：

    heroku --help

        Usage: heroku COMMAND [--app APP] [command-specific-options]

        Primary help topics, type "heroku help TOPIC" for more details:

          addons    #  manage add-on resources
          apps      #  manage apps (create, destroy)
          auth      #  authentication (login, logout)
          config    #  manage app config vars
          domains   #  manage domains
          logs      #  display logs for an app
          ps        #  manage dynos (dynos, workers)
          releases  #  manage app releases
          run       #  run one-off commands (console, rake)

        Additional topics:

          access         #  CLI to manage access in Heroku Applications
          buildpacks     #  manage the buildpack for an app
          certs          #  manage ssl endpoints for an app
          drains         #  display drains for an app
          features       #  manage optional features
          fork           #  clone an existing app
          git            #  manage local git repository for app
          help           #  list commands and display help
          keys           #  manage authentication keys
          labs           #  manage optional features
          local          #  run heroku app locally
          login          #  login with your Heroku credentials.
          maintenance    #  manage maintenance mode for an app
          members        #  manage membership in organization accounts
          notifications  #  display notifications
          orgs           #  manage organization accounts
          pg             #
          pgbackups      #  manage backups of heroku postgresql databases
          pipelines      #  manage collections of apps in pipelines
          plugins        #  manage plugins to the heroku gem
          redis          #  manage heroku redis instances
          regions        #  list available regions
          spaces         #  manage heroku private spaces
          stack          #  manage the stack for an app
          status         #  status of the Heroku platform
          update         #  update the heroku client
          version        #  display version

查看生产环境日志(用于错误调试)：

    heroku logs

在Heroku上运行控制台：

    heroku run rails c

在Heroku上的沙箱中运行控制台：

    heroku run rails c --sandbox

值得进一步解决的两个问题：

    git push heroku

        remote: ###### WARNING:
        remote:        You have not declared a Ruby version in your Gemfile.
        remote:        To set your Ruby version add this line to your Gemfile:
        remote:        ruby '2.2.4'
        remote:        # See https://devcenter.heroku.com/articles/ruby-versions for more information.
        remote:
        remote: ###### WARNING:
        remote:        No Procfile detected, using the default web server.
        remote:        We recommend explicitly declaring how to boot your server process via a Procfile.
        remote:        https://devcenter.heroku.com/articles/ruby-default-web-server

参考资料：

* [Ruby on Rails Tutorial > Chanpter 7: Sign up > 7.5.2 Production webserver](https://www.railstutorial.org/book/sign_up#sec-production_webserver)
* [Ruby on Rails Tutorial > Chanpter 7: Sign up > 7.5.3 Ruby version number](https://www.railstutorial.org/book/sign_up#sec-ruby_version_number)


## 项目实例

### RubyChina社区

  * [对所有已登录的用户开放 rack-mini-profiler 统计结果](https://ruby-china.org/topics/28858)
    * Ruby China 正在用那些我们常见到，又时常纠结的热门三方组件:
      * Devise：账号体系
      * CanCan：权限管理
      * will_paginate：分页
      * Carrierwave：文件上传辅助
      * Doorkeeper：OAuth 服务端
      * OmniAuth：OAuth 客户端
      * SimpleForm：表单辅助
      * Mongoid
    * 5 年来，Ruby China 一直在持续升级这些三方库，目前它们都基本已经到了最新的版本，也是证明 Rails，Gem 保持升级到新版本是可行的。
    * Rails 不慢，ActiveRecord 也不慢！Ruby China 的场景可以证明这个事情！

## Rails开发中需要注意的其他问题

### Git版本控制系统的使用

参考资料：[让 Git 全局性的忽略 .DS_Store](http://www.07net01.com/2015/03/804033.html)

> Mac 中每个目录都会有个文件叫.DS_Store, 用于存储当前文件夹的一些 Meta 信息。每次提交代码时，我都要在代码仓库的 .gitignore 中声明，忽略这类文件。有方法可以全局性的忽略某种类型的文件吗？ 按照以下两步就可实现：
>
>   1. 创建 ~/.gitignore_global 文件，把需要全局忽略的文件类型塞到这个文件里。
>   2. 在 ~/.gitconfig 中引入 .gitignore_global。 搞定了！在所有的文件夹下 .DS_Store .swp .zip 等文件类型会被 Git 自动忽略。


    subl ~/.gitignore_global

    # .gitignore_global
    ####################################
    ######## OS generated files ########
    ####################################
    .DS_Store
    .DS_Store?
    *.swp
    ._*
    .Spotlight-V100
    .Trashes
    Icon?
    ehthumbs.db
    Thumbs.db
    ####################################
    ############# packages #############
    ####################################
    *.7z
    *.dmg
    *.gz
    *.iso
    *.jar
    *.rar
    *.tar
    *.zip

    subl ~/.gitconfig

    [user]
        name = xiaoronglv
        email = xxxxx@gmail.com
    [push]
        default = matching
    [core]
        excludesfile = /Users/xxx/.gitignore_global


## 待解决的问题

### 本地


    Warning: PATH set to RVM ruby but GEM_HOME and/or GEM_PATH not set, see:
        https://github.com/wayneeseguin/rvm/issues/3212


## Cloud9的使用

参考资料：

[Cloud9官网](https://c9.io)：基于Web的集成开发环境，在一个页面中整合了导航、编辑器和终端，简洁易用，功能强大。通workspace和Git管理应用程序代码，和BitBucket、Heroku配合使用可以获得更加完美的体验。

Cloud9使用方法：

* 在编辑器中通过`Cmd + S`快捷键保存当前修改，`Cmd + D`删除当前行。
* 在Chrome中使用Cloud9时，记得为该网域关闭AdBlock Plus，否则语法高亮等功能会失效。
* 在终端中通过`puma s -b $IP -p $PORT`启动测试用Web服务器，在Share菜单中允许从外部访问测试用Web服务器并获得访问所需的URL地址。
* 在Dashboard中新建workspace，每个workspace相当于一个独立的开发用VPS，具有独立的`~/workspace/`目录。
* 在一个`~/workspace/`目录下可以通过`rails new appname`创建多个Rails应用程序，在某个应用程序目录下运行`puma s ...`然后可以从外部访问这个应用程序的测试服务器。
* 经测试，Cloud 9完美支持ruby 2.3.1和rails 5.0.0.rc1。

查看环境变量：

    echo $IP    # => 0.0.0.0
    echo $PORT    # => 8080

在开发环境下启动Web服务器：

    rails c -b $IP -p $PORT

注：如果在Cloud9上启动了Web服务器并且在Share中打开了外部访问，但是从外部访问不正常时，可以尝试重启Workspace。

