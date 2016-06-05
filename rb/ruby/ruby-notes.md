# Ruby笔记


## Ruby简介

### 参考资料

* 网站
    + [Ruby官网](https://www.ruby-lang.org/en/)：最新版本`2.3.1`，2016年4月26日发布。
* Web电子书
    + [Learn Ruby The Hard Way](http://learnrubythehardway.org/book/)
* 多看电子书：
    + Ruby基础教程(第4版)，[日]高桥征义、后藤裕藏，[日]松本行弘 审校，何文斯 译，人民邮电出版社(图灵程序设计丛书)
* PDF电子书
    + Programming Ruby 1.9&2.0

题外话-写得好的教程：

* PHP Manual
* Core Python Programming (Python核心编辑)
* Go语言编程 (许式伟)
* Ruby基础教程 ([日]高桥征义、后藤裕藏)
* Rails实战圣经
* 深入浅出CoffeeScript

注：可以作为写教程的教程。

### 中英文对照

| 英文                | 中文       | 不同翻译方法 |
|---------------------|------------|--------------|
| numeric             | 数值       |-             |
| string              | 字符串     |-             |
| symbol              | 符号       |-             |
| regular expression  | 正则表达式 |-             |
| container           | 容器       |-             |
| array               | 数组       |-             |
| hash                | 散列表     | 散列、哈希表 |
| exception           | 异常       |-             |
| variable            | 变量       |-             |
| local variable      | 局部变量   |-             |
| global variable     | 全局变量   |-             |
| instance variable   | 实例变量   |-             |
| class variable      | 类变量     |-             |
| pseudo variable     | 伪变量     |-             |
| constant            | 常量       |-             |
| method              | 方法       |-             |
| object              | 对象       |-             |
| class               | 类         |-             |
| instance            | 实例       |-             |
| map                 | 映射       |-             |
| file                | 文件       |-             |
| library             | 库         |-             |
| multiple assignment | 多重赋值   | 并行赋值     |
| namespace           | 命名空间   | 名字空间     |

### 关于Ruby

matz：人受创造之驱动，我清楚自己非常喜欢创造。(人生之价值和乐趣所在)

matz：通过阅读源代码来获悉语言的准确行为。

matz：Ruby让编程更容易，更有趣。

Dave Thomas：Ruby让你能够集中精力解决手头上的问题。

### 知识体系

参考资料：[PHP Manual](http://php.net/manual/en/index.php)

* 工具
    + irb
    + Rake
* 库
    + 57个标准类和模块的1300个方法 (Ruby标准库有9000多个方法)
    + RubyGems
* 文档
    + RDoc(标准库的文档——近万个方法，源代码中的文档，ri)
* 所有方法 vs 常用方法
* 内建的类、模块，标准库
    + 类、模块的方法
    + 类、对象(类的实例)
* 类
    + 数据类型都是类
    + 查询对象所属的类
    + 判断对象是否属于某个类
    + 根据继承关系判断对象是否是某个类(类、父类、祖先类)
    + 类的继承关系
    + 定义类
    + 实例变量
    + 实例方法
    + 存取器
    + 公共方法、私有方法、受保护方法
    + self变量
    + 类常量
    + 类变量
    + 类方法
    + 从外部为类添加方法(打开类)
    + 类的继承
* 类型
* 表达式
* 语句
* 测试
    + 单元测试

### 一句话知识点

**变量**：

变量赋值造成对象别名，其中一个改变都改变。通过freeze方法可以冻结对象，避免改变(一改变就出错)。

**字符串**：

字符串中存在转义字符(\xxx)或内插表达式(#{xxx})时应使用双引号，其他情况可优先使用单引号。

对于全局变量$xxx，内插表达式#{$xxx}应简写为#xxx。

对于实例变量@xxx，内插表达式#{@xxx}应简写为#xxx。

**正则表达式**：

/xxx/是正则表达式。=~做正则匹配，sub方法替换一次，gsub方法替换所有。

**对象、类、模块、方法**：

类定义中的构造(初使化)方法initialize

inspect方法输出对象ID和对象的实例变量。

<定义子类(父类)。

Ruby是单继承语言，每个类只有一个父类。通过包含mixin可以实现多继承的效果，而不会引入多继承的缺点。

attr_reader :xxx, ... 等价于 def xxx @xxx end

attr_writer :xxx, ... 等价于 def xxx=(params) @xxx = params end

我们可以打开标准类或自定义类来为类添加新的方法。

出现在方法定义代码块内最后一行的return xxx等价于xxx，都为方法提供了返回值。应使用后面这种方式。

类变量对类和类的实例都是私有的，要从外部访问只能通过方法。

类方法不需要实例即可直接调用。定义方法： def ClassName.method_name ... end 或 def self.method_name ... end 或 class << self def method_name ... end end

私有方法只能在当前对象中调用。定义私有方法： private :method

保护方法可以在当前类的所有对象中调用。定义保护方法： protected :method

方法名可以以?、!、=结尾。

arr[start, count] arr[start..end] # 包含结束位置 arr[start...end] # 不包含结束位置

{…}或do…end被称为块。前者用于单行，后者用于多行。

“方法名+块”实现调用关联，在方法定义中可以用yield调用块。块调用支持参数| xxx, xxx, ... |，通过yield(xxx)调用。

用*args声明可变参数。

**流程控制**：

通过块可以实现迭代器。迭代器的使用，以面向对象的方式实现了循环，语法更简洁自然。

each、find、collect是常用的迭代器。

**输入输出**：

puts输出参数并换行，print输出参数不换行，printf格式化输出。

**其他**：

链式语句


## irb控制台

启动控制台：

    irb

退出控制台：

    exit

或`Ctrl + D`。


## Ruby脚本文件

设置文件编码：

    #encoding: GBK

除了`GBK`，还可以指定编码为`GB2312`或`UTF-8`。

执行脚本程序：

    ruby hello.rb
    ruby -w hello.rb    # 显示警告信息(默认不显示？)

也可以在执行脚本程序时指定编码：

    ruby -E GBK hello.rb

命令行参数：

    # hello.rb
    puts "First argument: #{ARGV[0]}"
    puts "Second argument: #{ARGV[1]}"
    puts "Third argument: #{ARGV[2]}"
    puts "There are #{ARGV.length} arguments in total."

    ruby hello.rb 1 2 3

    输出结果：

        First argument: 1
        Second argument: 2
        Third argument: 3
        There are 3 arguments in total.

执行系统命令：

    `ls`
    %x{ ls }

中断执行，退出脚本程序：

    abort    # alias for `Kernel.exit(failse)`
    exit    # alias for `Kernel.exit(true)` and raise `SystemExit` exception

参考资料：[Stop execution of Ruby script](http://stackoverflow.com/questions/4432506/stop-execution-of-ruby-script "Google关键字：ruby exit script")


## 基本语法

### 注释

单行注释以`#`开头。

多行注释：

    =begin
    ...
    =end


## 数据类型

### 布尔值

`false`和`nil`为假，`true`和其他值均为真。

注：nil是表示没有任何东西的对象。

0也为真：

    if 0
      puts 'true'
    end

    输出结果：

        true

### 数值

整数和浮点数：

    100
    3.14
    -1

输出固定宽度的数值：

    "%04d" % 1    # => "0001"
    "%04d" % 10    # => "0010"
    "% 4d" % 1    # => "   1"
    "% 4d" % 10    # => "  10"

运算(加、减、乘、除和混合运算)：

    1 + 1    # => 2
    1 - 1    # => 0
    3 * 3    # => 9
    3 / 3    # => 1
    1 + 2 * 3    # => 7

指数：

    1e2    # => 100.0
    1e-2    # => 0.01

数学函数：

    Math.sqrt 9    # => 3

把字符串转换为整数：

    '123'.to_i    # => 123
    '3.14'.to_i    # => 3

### 字符串

使用单引号的字符串不转义，使用双引号的字符串会转义：

    'hello world\n'    # => "hello world\n"
    %q/hello world\n/    # => "hello world\n"
    "hello world\n"    # => "hello world" with newline
    %Q/hello world\n/    # => "hello world\n"
    person = 'world'
    %Q/hello #{person}/    # => "hello world"

注：`%Q/.../`支持字符串插值，但不支持`\n`转义字符，这一点需要注意。分界符`/.../`也可以换成`！...!`、`{...}`等。

使用双引号的字符串插值：

    'hello world'    # => "hello world"
    'hello #{world}'    # => "hello #{world}"
    "hello #{world}"    # => eg. "hello China"

多行字符串：

参考资料：[Ruby 多行字符串 heredoc 详解](https://ruby-china.org/topics/25983)

    puts <<EOF
    this is the first line
    this is the second line
    EOF

    puts <<-EOF
      this is the first line
      this is the second line
    EOF

    puts <<-EOF.gsub(/^\s+/, '')
      this is the first line
      this is the second line
    EOF

注：`<<-EOF ... EOF`的用法，每行字符串开头的空格都将保留，通过`.gsub(/^\s+/, '')`可以达到去除空格的效果。

字符串迭代：

    'abc'.each_char do |c|
      puts c
    end

    输出结果：

        a
        b
        c

字符串长度：

参考资料：[Ruby：字符集和编码学习总结](http://www.cnblogs.com/happyframework/p/3275367.html "百度关键字：ruby 字符串 bytesize")

    '我们'.length    # => 2
    '我们'.bytesize    # => 6
    '我们'.encode('gb18030').bytesize    # => 4

字符串包含：

参考资料：[How to check whether a string contains a substring in Ruby?](http://stackoverflow.com/questions/8258517/how-to-check-whether-a-string-contains-a-substring-in-ruby "Google关键字：ruby string contains")

    'abc'.include? 'bc'    # => true
    'abc'.include? 'd'    # => false

### 符号

符号和字符串类似，区别在于符号用作散列表的键时性能比字符串更好。符号和字符串可以互相转换。

符号：

    :tom

把字符串转换为符号：

    'tom'.to_sym    # => :tom

把符号转换为字符串：

    :tom.to_s    # => "tom"

### 正则表达式

参考资料：

* [Ruby Regular Expressions](http://www.tutorialspoint.com/ruby/ruby_regular_expressions.htm)

正则表达式：

    /abc/    # 在字符串任意位置进行匹配
    /abc/i    # 匹配时忽略大小写
    /^abc/    # 从字符串开头位置开始匹配
    /abc$/    # 从字符串结尾位置开始匹配
    /^$/    # 匹配空行

正则表达式的更多表示方法：

    %r{abc}    # => /abc/
    Regexp.new('abc')    # => /abc/

正则表达式匹配(简称”正则匹配“)：

    /abc/ =~ 'abcdefg'    # => 0
    /bcd/ =~ 'abcdefg'    # => 1
    /Bcd/ =~ 'abcdefg'    # => nil
    /Bcd/i =~ 'abcdefg'    # => 1
    /Bcd/ =~ 'ABCDEFG'    # => nil
    /Bcd/i =~ 'ABCDEFG'    # => 1

查询：

    /^# (.*)$/.match("# This is the title\nblahblahblah")[1]

字符串替换：

    'abcccdefg'.gsub /c{3}/, 'c'    # => "abcdefg"
    'abcccdefg'.gsub /(c{3})/, '**\1**'    # => "ab**ccc**defg"；注意：`'**\1**'`不能使用双引号


## 容器

### 数组

数组：

    []    # empty array
    ['a', 'b', 'c']    # string array
    [1, 2, 3]    # digit array
    ['a', 'b', 'c', 1, 2, 3]    # mixed array

访问数组元素：

    chars = ['a', 'b', 'c']
    chars[0]    # => "a"
    chars[1]    # => "b"
    chars[-1]    # => "c"

修改数组元素：

    digits = [1, 2, 3]
    digits[0] = 2
    digits    # => [2, 2, 3]

为数组添加元素：

    [1, 2, 3]  << 4    # => [1, 2, 3, 4]
    [1, 2, 3].push 4    # => [1, 2, 3, 4]

数组的长度：

    digits = [1, 2, 3]
    digits.size    # => 3

快速生成数组：

    (1..3).to_a    # => [1, 2, 3]
    (1...3).to_a    # => [1, 2]

遍历数组：

    [1, 2, 3].each do |i|
      puts i
    end

### 散列表

散列表：

    {}    # empty hash
    {:one => 1, :two => 2, :three => 3}
    {one: 1, two: 2, three: 3}    # simpler form of above hash

访问散列表的值：

    digits = {one: 1, two: 2, three: 3}
    digits[:one]    # => 1

修改散列表的值：

    orders = {one: 'Tom', two: 'Jerry', three: 'Mickey'}
    orders[:one] = 'Eric'
    orders    # => {:one=>"Eric", :two=>"Jerry", :three=>"Mickey"}

遍历散列表：

     digits = {one: 1, two: 2, three: 3}
     digits.each do |k, v|
       puts "#{k}: #{v}"
     end

     输出结果：

        one: 1
        two: 2
        three: 3


## 变量

局部变量以小写英文字母或`_`开头：

    name
    _name

首次给局部变量赋值时会同时初始化该局部变量。引用未初始化的局部变量会抛出异常。

全局变量以`$`开头：

    $name

实例变量以`@`开头：

    @name

类变量以`@@`开头：

    @@name

伪变量是Ruby预先定义的代表某个特定值的特殊变量，无法通过赋值改变伪变量的值：

    nil
    true
    false
    self

变量赋值：

    name = 'Tom'
    age = 18

多重赋值：

    a, b = 1, 2
    a, b = b, a    # 多重赋值可用于交换变量的值
    a    # => 2
    b    # => 1

    a, b = [1, 2]    # 多重赋值可用于访问数组元素
    a    # => 1
    b    # => 2

    a, b = [1, [2, 3]]
    a    # => 1
    b    # => [2, 3]

    a, [b, c] = [1, [2, 3]]
    a    # => 1
    b    # => 2
    c    # => 3

    a, b, c = 1, 2    # 多余的左值会被赋值为nil
    a    # => 1
    b    # => 2
    c    # => nil

    a, b = 1, 2, 3    # 多余的右值会被忽略
    a    # => 1
    b    # => 2

    a, b, *c = 1, 2, 3, 4, 5    # 变量前加`*`将会把对应位置的值和未分配的值作为数组赋值给该变量
    a    # => 1
    b    # => 2
    c    # => [3, 4, 5]

短变量名的习惯用法：

    [x, y, z]    # 坐标
    [i, j, k]    # 循环计数


## 常量

常量以大写英文字母开头。常量的行为和变量类似，区别是给已初始化的常量赋值会显示警告信息(但不会抛出异常)。

常量示例：

    Owner
    ARGV
    RUBY_VERSION


## 保留字

使用保留字作为变量或常量名称会提示语法错误。

Ruby保留字(41个)：

    __LINE__
    __ENCODING__
    __FILE__
    BEGIN
    END
    alias
    and
    begin
    break
    case
    class
    def
    defined?
    do
    else
    elsif
    end
    ensure
    false
    for
    if
    in
    module
    next
    nil
    not
    or
    redo
    rescue
    retry
    return
    self
    super
    then
    true
    undef
    unless
    until
    when
    while
    yield


## 命名风格

变量名、方法名使用下划线风格：

    first_person
    find_the_largest

常量名、类名、模块名使用驼峰风格：

    SelectedOnes


## 表达式


## 运算符

注：算术运算符参见”数据类型 > 数值“，赋值运算符参见”变量 > 变量赋值“。

### 运算优先级

运算符优先级从高到低：

    []
    +(一元运算符)    !    ~
    **
    -(一元运算符)
    *    /    %
    +    -
    <<    >>
    &
    |    ^
    >    >=    <    <=
    <=>    ==    ===    !=    =~    !~
    &&
    ||
    ? :(条件运算符)
    ..    ...
    =    +=    -=    *=    /=    %=
    not
    and or


### 比较运算符

    a > b
    a < b
    a >= b
    a <= b
    a == b
    a === b    # 左值是数值或字符串时，等价于`==`；左值是正则表达式时，等价于`=~`
    a != b

### 逻辑运算符

    a && b    # 与
    a || b    # 或
    !a    # 非
    a and b
    a or b
    not a

注：`and`、`or`、`not`和`&&`、`||`、`!`的作用相同，但优先级较低。

### 条件运算符

    a, b = 1, 2
    bigger = (a > b) ? a : b
    bigger    # => 2


## 流程控制

### 条件

作为条件的表达式经常用到比较运算符和逻辑运算符，作为条件的表达式返回布尔值。

if语句：

    if a > b
      puts 'a is larger than b.'
    end

    if a > b
      puts 'a is larger than b.'
    else
      puts 'a is not larger than b.'
    end

    if a > 10
      puts 'Larger than 10.'
    elsif a > 5
      puts 'Larger than 5.'
    else
      puts 'Smaller than 5.'
    end

注：省略了`then`。

if修饰符：

    puts 'a is larger than b.' if a > b

unless语句：

    unless a <= b
      puts 'a is larger than b.'
    end

    unless a <= b
      puts 'a is larger than b.'
    else
      puts 'a is not larger than b.'
    end

注：unless语句和if语句的作用相同，区别在于unless语句是条件为假时进行处理，if语句是条件为真时进行处理。

unless修饰符：

    puts 'a is larger than b.' unless a <= b

case语句：

    case digit
    when 1
      puts 'one'
    when 2
      puts 'two'
    when 3
      puts 'three'
    else
      puts 'unknown'
    end

    # case语句支持正则匹配
    case info
    when /Tom/
      puts 'It is Tom!'
    when /Jerry/
      puts 'It is Jerry!'
    else
      puts 'Who is it?'
    end

注：case语句使用`===`进行匹配，因此支持正则匹配。

### 循环

for语句：

    for i in 1..3
      puts i
    end

    输出结果：

        1
        2
        3

注：省略了`do`。

times方法：

    3.times do
      puts 'hello'
    end

    输出结果：

        hello
        hello
        hello

    3.times do |i|
      puts i
    end

    输出结果：

        0
        1
        2

    3.times { print 'a' }    # => aaa

while语句：

    i = 3
    while i > 0
      puts i
      i = i - 1
    end

    输出结果：

        3
        2
        1

注：省略了`do`。

until语句：

    i = 1
    until i > 3
      puts i
      i = i + 1
    end

    输出结果：

        1
        2
        3

注：省略了`do`。`until a`实际上等价于`while !a`。

loop方法：

    i = 1
    loop do
      puts i
      i = i + 1
      break if i > 3
    end

注：`do`不能省略(因为没有条件表达式)。

除了`break`命令，还可以使用`next`和`redo`命令。`break`是中止循环，`next`是进入下一次循环，`redo`是重复本次循环。三个命令都会忽略本次循环中之后的代码。

改变计数变量的值：

    i = i + 1
    i += 1
    i = i - 1
    i -= 1

不支持`i++`和`i--`的写法。

### 迭代

each方法：

    [1, 2, 3].each do |i|
      puts i
    end

    输出结果：

        1
        2
        3

     digits = {one: 1, two: 2, three: 3}
     digits.each do |k, v|
       puts "#{k}: #{v}"
     end

     输出结果：

        one: 1
        two: 2
        three: 3

注：`[1, 2, 3].each do |i|`相当于`for i in [1, 2, 3]`。

map方法：

    (1..3).to_a.map { |id| id*2 }    # => [2, 4, 6]

`each_with_index`方法：

    nums.each_with_index do |num, index|
      chapters[num.to_s] = titles[index]
    end

find方法：

collect方法：

### 异常




### 列表解析

参考资料：

* [Building A Ruby List Comprehension](https://blog.engineyard.com/2014/ruby-list-comprehension "Google关键字：ruby list comprehension")
* [List comprehension in Ruby](http://stackoverflow.com/questions/310426/list-comprehension-in-ruby "Google关键字：ruby list comprehension")

示例代码：

    [2 * x for x in xrange(1, 100)]
    [{x: 1}, {x: 2}, {x: 3}].collect{|e| e[:x] }    # => [1, 2, 3]
    keywords = Word.select(:content).where('content like ?', "#{prefix}%").collect{ |w| {content: w.content} }    # => [{"content":"学习实践活动"},{"content":"学习"},{"content":"实践"}]


## 输入输出

print方法不会在行尾输出换行，puts方法会在行尾输出换行：

    print 'Hello world!'    # => "Hello world!"
    puts 'Hello world!'    # => "Hello world!" with newline

在irb中还可以使用p方法：

    print 100    # => 100
    print '100'    # => 100
    p 100    # => 100
    p '100'    # => "100"

使用less浏览输出的长内容：

参考资料：[How to use Unix pager programs like `less` from Ruby?](http://stackoverflow.com/questions/9636377/how-to-use-unix-pager-programs-like-less-from-ruby "Google关键字：ruby popen less")

    IO.popen("less", "w") do |f|
      f.puts very_long_string
    end


## 文件操作

### 写入文件

一次性写入所有内容：

    def to_file(filename='addressbook.html', content)
        File.open(filename, 'w') do |f|
            f.puts content
        end
    end

### 读取文件内容

一次性读取文件全部内容-方式一：

    f = File.read('/path/to/filename')
    text = f.read
    print text
    f.close

一次性读取文件全部内容-方式二：

    text = File.new('/path/to/filename').read
    print text

逐行读取文件全部内容：

    f = File.open('/path/to/filename')
    f.each_line do |line|
      print line
    end
    f.close

### 列出当前目录下的所有Markdown文件

    Dir.glob('./input/*.md')    # => ["./input/1.md", "./input/2.md", "./input/3.md"]

### 组装路径

    File.join('./input', '*.md')    # => "./input/*.md"

### 获得文件名

带扩展名的文件名：

    File.basename('./input/1.md')    => "1.md"

不带扩展名的文件名：

    File.basename('./input/1.md', '.*')    => "1"

### 检测文件是否存在

    FileTest.exist?('/path/to/file')

### 复制、删除、移动文件

    require 'fileutils'
    FileUtils.cp('/path/to/oldfile', '/path/to/newfile')
    FileUtils.rm('/path/to/file')
    FileUtils.mv('/path/to/oldfile', '/path/to/newfile')

### 引用库(文件)

引用自定义库：

    # name.rb
    def name
      'Tom'
    end

    # hello.rb
    require './name'
    puts "Hello #{name}!"

    ruby hello.rb

    输出结果：

        Hello Tom!

引用第三方库：

    # pretty_print.rb
    require 'pp'
    digits = {one: 1, two: 2, three: 3}
    pp digits

    ruby pretty_print.rb

    输出结果：

        {:one=>1, :two=>2, :three=>3}


## 日期时间

今天的日期(如`2014-12-12`)：

    require 'date'
    Date.today.to_s    # => 2014-12-12

计算日期间隔：

    require 'date'
    beginning = Date.parse('2013-08-19')
    ending = Date.parse('2014-07-10')
    days = (ending - beginning).to_i    # => 30

格式化DateTime：

参考资料：[关于Ruby格式化时间DateTime](http://hlee.iteye.com/blog/1032645)

    <%= order.datetime.strftime('%Y-%m-%d %H:%M') %>


## 方法

在Ruby中，对象的所有操作都被封装成方法。调用对象的方法就是向对象发送消息(方法名、调用参数)、查找方法、执行方法的过程。

查看对象的可用方法：

    'abc'.methods    # => [:include?, :unicode_normalize, :to_c, :%, :unicode_normalize!, :unicode_normalized?, :*, :+, :count, :partition, :unpack, :encode, :encode!, :next, :casecmp, :insert, :bytesize, :match, :succ!, :next!, :upto, :index, :rindex, :replace, :clear, :chr, :+@, :-@, :setbyte, :getbyte, :<=>, :<<, :scrub, :scrub!, :byteslice, :==, :===, :dump, :=~, :downcase, :[], :[]=, :upcase, :downcase!, :capitalize, :swapcase, :upcase!, :oct, :empty?, :eql?, :hex, :chars, :split, :capitalize!, :swapcase!, :concat, :codepoints, :reverse, :lines, :bytes, :prepend, :scan, :ord, :reverse!, :center, :sub, :freeze, :inspect, :intern, :end_with?, :gsub, :chop, :crypt, :gsub!, :start_with?, :rstrip, :sub!, :ljust, :length, :size, :strip!, :succ, :rstrip!, :chomp, :strip, :rjust, :lstrip!, :tr!, :chomp!, :squeeze, :lstrip, :tr_s!, :to_str, :to_sym, :chop!, :each_byte, :each_char, :each_codepoint, :to_s, :to_i, :tr_s, :delete, :encoding, :force_encoding, :sum, :delete!, :squeeze!, :tr, :to_f, :valid_encoding?, :slice, :slice!, :rpartition, :each_line, :b, :to_r, :ascii_only?, :hash, :to_json, :to_json_raw, :to_json_raw_object, :<, :>, :<=, :>=, :between?, :instance_of?, :public_send, :instance_variable_get, :instance_variable_set, :instance_variable_defined?, :remove_instance_variable, :private_methods, :kind_of?, :instance_variables, :tap, :is_a?, :extend, :define_singleton_method, :to_enum, :enum_for, :!~, :respond_to?, :display, :send, :object_id, :method, :public_method, :singleton_method, :nil?, :class, :singleton_class, :clone, :dup, :itself, :taint, :tainted?, :untaint, :untrust, :trust, :untrusted?, :methods, :protected_methods, :frozen?, :public_methods, :singleton_methods, :!, :!=, :__send__, :equal?, :instance_eval, :instance_exec, :__id__]

定义方法-不带参数：

    def hello
      puts 'Hello world!'
    end
    hello

    输出结果：

        Hello world!

定义方法-带参数：

    def hello(name)
      puts "Hello #{name}!"
    end
    hello 'Tom'

    输出结果：

        Hello Tom!

使用`return xxx`的方式指定方法的返回值，`return`语句可以省略，此时方法中最后一个表达式的值就会成为方法的返回值。

调用方法时，`()`可以省略，因此`hello('Tom')`可以简写为`hello 'Tom'`，`add(1, 2)`可以简写为`add 1, 2`，即方法名和参数之间用空格隔开，参数之间用逗号隔开。

带块的方法调用，可参考times方法、loop方法、each方法等，如`3.times { |i| print "#{i} " }`输出`1 2 3 `。

看起来像运算符的方法调用：

    a + b    # `+`是a的方法，b是方法调用的参数
    /abc/ =~ 'abcdefg'    # `=~`是`/abc/`的方法，`'abcdefg'`是方法调用的参数
    digits = [1, 2, 3]    # `=`是`digits`的方法，`[1, 2, 3]`是方法调用的参数
    digits[0]    # `[]`是`digists`的方法，`0`是方法调用的参数
    digits[0] = 4    # `[]=`是`digits`的方法，`0`和`4`是方法调用的参数

这意味着可以重新定义这些看似运算符的方法的行为。

关于方法名的约定：

* 返回布尔值的方法，其方法名都要以`?`结尾。

根据接收者种类的不同，方法可分为函数式方法、实例方法、类方法。

函数式方法是没有接收者的方法，或者更准确地说是接收者可以省略的方法：

    puts 123
    sleep 10

实例方法是最常用的方法：

    '3.14'.to_i    # => 3
    ['a', 'b', 'c'].index('b')    # =》 1
    Time.now.to_s    # => "2016-05-08 14:59:41 +0800"

类方法的接收者是类：

    Array.new    # => []
    File.open '/path/to/file'
    Time.now    # => 2016-05-08 15:00:57 +0800

约定俗成的方法表示法：

    类名#方法名    # 仅用于教程
    类名.方法名
    类名::方法名

定义带块的方法-不带参数：

    def hello
      yield
    end
    hello do
      puts 'Hello world!'
    end

    输出结果：

        Hello world!

定义带块的方法-带参数：

    def hello
      yield 'Tom'
    end
    hello do |person|
      puts "Hello #{person}!"
    end

    输出结果：

        Hello Tom!

定义方法-带不确定个数的参数：

    def hello(*args)
      args.each do |arg|
        puts "Hello #{arg}!"
      end
    end
    hello 'Tom', 'Jerry'

    输出结果：

        Hello Tom!
        Hello Jerry!

定义方法-至少带一个参数：

    def hello(arg, *args)
      puts "Hello #{arg}!"
      args.each do |arg|
        puts "Hello #{arg}!"
      end
    end
    hello 'world', 'Tom', 'Jerry'

    输出结果：

        Hello world!
        Hello Tom!
        Hello Jerry!

定义方法-首尾至少各带一个参数：

    def hello(arg1, *args, arg2)
      puts "Hello #{arg1}!"
      args.each do |arg|
        puts "Hello #{arg}!"
      end
      puts "Hello #{arg2}!"
    end
    hello 'world', 'Tom', 'Jerry', 'earth'

    输出结果：

        Hello world!
        Hello Tom!
        Hello Jerry!
        Hello earth!

定义方法-关键字参数：

    def hello(first: 'Tom', second: 'Jerry')
      puts "Hello #{first} and #{second}!"
    end
    hello
    hello first: 'Jim', second: 'Tim'
    hello second: 'Tim'
    persons = {first: 'Joe', second: 'John'}
    hello persons

    输出结果：

        Hello Tom and Jerry!
        Hello Jim and Tim!
        Hello Tom and Tim!
        Hello Joe and John!


## Proc对象

通过Proc对象，可以把块当作对象。

示例代码：

    hello = Proc.new do |name|
      puts "Hello #{name}!"
    end
    hello.call 'Tom'    # Hello Tom!

在定义方法时，最后一个参数可以写成`&参数名`的形式，这样以带块的方式调用方法时就会把块赋值给这个参数，从而得到一个Proc对象。

示例代码：

    def hello(from, &to)
      from.each &to
    end
    from = ['Tom', 'Jerry', 'Candy']
    hello from do |p|
      puts "#{p} says: Hello world!"
    end

    输出结果：

        Tom says: Hello world!
        Jerry says: Hello world!
        Candy says: Hello world!


## 对象

Ruby是真正的面向对象的语言，所有东西都是对象，所有操作都是对象方法的调用。数值、字符串、符号、数组、散列表、正则表达式、文件、日期时间、异常都是对象。

对象ID：

    'abc'.object_id    # => 70133011854900

判断对象ID是否相同(是否是同一个对象)：

    one = 1
    digit = one
    one.equal? digit    # => true
    one.equal? 1    # => true

判断对象的值是否相等：

    one = 1
    another_one = 1.0
    one == another_one    # => true
    one.eql? another_one    # => false

对于数值的比较，`eql?`方法比`==`方法更严格。

把对象转换为字符串：

    String.inspect    # => "String"
    'abc'.inspect    # => "\"abc\""
    123.inspect    # => "123"

    String.to_s    # => "String"
    'abc'.to_s    # => "abc"
    123.to_s    # => "123"

`to_s`方法通常用于输出运行结果，`inspect`方法通常用于确认程序状态、查询对象内部信息。


## 类

类就是对象的种类。对象拥有什么特性是由类决定的。如果一个对象属于某个类，就可称它为`xx类的对象`或`xx类的实例`。在上下文允许的情况下，“类的实例”通常简称为“实例”。

类名和常量名一样，以大写字母开头。

在Ruby中一切都是对象，类是Class类的对象：

    String.class    # => Class
    Class.class    # => Class

Ruby提供的数据类型实际上都是类：

    digits = Array.new
    digits    # => []
    name = String.new
    name    # => ""

查询对象所属的类：

    123.class    # => Fixnum
    'abc'.class    # => String
    [1, 2, 3].class    # Array

判断对象是否属于某个类：

    'abc'.instance_of? String    # => true
    123.instance_of? String    # => false

根据继承关系判断对象是否属于某个类(类、父类、祖先类)：

    'abc'.is_a? String    # => true
    'abc'.is_a? Object    # => true
    'abc'.is_a? Numeric    # => false
    123.is_a? String    # => false

注：`instance_of?`和`is_a?`方法是在Object类中定义的，因此所有对象都可以使用这两个方法。

类的继承关系：

* BasicObject
    + Object
        - Array
        - String
        - Hash
        - Regexp
        - IO
            * File
        - Dir
        - Numeric
            * Integer
                + Fixnum
                + Bignum
            * Float
            * Complex
            * Rational
        - Exception
        - Time

定义类：

    class Hello
      def initialize(name='Tom')
        @name = name
      end
      def hello
        puts "Hello #{@name}!"
      end
    end
    tom = Hello.new
    tom.hello    # Hello Tom!
    jerry = Hello.new 'Jerry'
    jerry.hello    # Hello Jerry

使用new方法生成类的对象时，会调用initialize方法，new方法的参数会原封不动地传递给initialize方法。（因此在调用类方法时，initialize方法并没有机会运行，这一点需要注意)

实例变量：

实例变量是在类中定义的以`@`开头的变量，在同一个实例的不同方法中都可以使用(相当于这个实例范围内的“全局变量”)。不同实例的相同实例变量之间没有关系，值可以不同。相比之下，局部变量只能在方法内使用。

存取器：

    class Hello
      def initialize(name='Tom')
        @name = name
      end
      def hello
        puts "Hello #{@name}!"
      end
      def name
        @name
      end
      def name=(value)
        @name = value
      end
    end

其中`name`方法的定义可以简写为`attr_reader :name`，`name=(value)`方法的定义可以简写为`attr_writer :name`，两者可以一并简写为`attr_accessor :name`。因此上述代码可以简写为：

    class Hello
      attr_accessor :name
      def initialize(name='Tom')
        @name = name
      end
      def hello
        puts "Hello #{@name}!"
      end
    end

公共方法、私有方法、受保护方法：

* 公共方法总是可以访问。公共方法是方法的默认身份，`public`关键字可以省略。
    + initialize方法是例外，默认为私有方法。
* 私有方法只能在实例内部访问。不能为私有方法指定接收者，其接收者只能是默认的self，这就是不能从实例外部访问私有方法的原因。私有方法使用`private`关键字。
* 受保护方法可以在同一个类及其子类中作为实例方法调用。受保护方法使用`public`关键字。

示例代码-受保护方法：

    class Hello
      attr_accessor :name
      protected :name=    # 定义受保护方法
      def initialize(name='Tom')
        @name = name
      end
      def hello
        puts "Hello #{name}!"
      end
      def alias(obj)
        @name = obj.name    # 调用受保护方法
      end
    end
    tom = Hello.new
    jerry = Hello.new 'Jerry'
    tom.hello    # Hello Tom!
    tom.alias(jerry)
    tom.hello    # Hello Jerry!

self变量：

self变量用于在实例方法中引用方法的接收者。self通常可以省略，换句话说，self是方法的默认接收者。当存在和方法同名的局部变量时，self不能省略。

示例代码：

    class Hello
      attr_accessor :name
      def initialize(name='Tom')
        @name = name
      end
      def hello
        puts "Hello #{name}!"    # 一般情况下self可以省略
      end
      def greet
        name = 'Jerry'
        puts "Hello #{self.name}!"    # 存在同名局部变量时，self不能省略
      end
    end
    tom = Hello.new
    tom.hello    # Hello Tom!
    tom.greet    # Hello Tom!

类常量：

    class Hello
      Version = '1.0'
    end
    Hello::Version    # => "1.0"

类变量：

类变量是在类中定义的以`@@`开头的变量，在该类的所有实例中都可以使用。类变量不支持存取器，要从外部访问必须手动定义读写类方法。

示例代码：

    class Hello
      @@count = 0
      def initialize(name='Tom')
        @name = name
      end
      def hello
        puts "Hello #{@name}!"
        @@count += 1
      end
      def self.count
        @@count
      end
      def self.count=(value)
        @@count = value
      end
    end
    tom = Hello.new
    jerry = Hello.new 'Jerry'
    Hello.count    # => 0
    tom.hello
    jerry.hello
    Hello.count    # => 2
    Hello.count = 0
    Hello.count    # => 0

类方法：

类方法是接收者是类的方法，类方法操作的是类而不是实例。调用类方法时，需指定作为指收者的类。

定义类方法-方法一：

    class << Hello
      def hello(name)
        puts "Hello #{name}!"
      end
    end
    Hello.hello 'Tom'    # Hello Tom!

这种定义类方法的写法称为单例类定义，所定义的类方法称为单例方法。

定义类方法-方法二：

    class Hello
      class << self
        def hello(name)
          puts "Hello #{name}!"
        end
      end
    end
    Hello.hello 'Tom'    # Hello Tom!

在class上下文中使用self时，引用的是类本身，因此上面的`class << self`和方法一中的`class << Hello`效果是一样的。

定义类方法-方法三：

    class Hello
      def Hello.hello(name)
        puts "Hello #{name}!"
      end
    end
    Hello.hello 'Tom'    # Hello Tom!

定义类方法-方法四：

    class Hello
      def self.hello(name)
        puts "Hello #{name}!"
      end
    end
    Hello.hello 'Tom'    # Hello Tom!

从外部为类添加方法(打开类)：

    class Numeric
      def double
        self * 2
      end
    end
    1.double    # => 2

类的继承：

    class Title < String
      def html
        "<title>#{self}</title>"
      end
    end
    title = Title.new 'Hello world!'
    title.length    # => 12
    title.html    # => "<title>Hello world!</title>"

有了继承就可以在父类中定义相同的功能，在子类中定义独有的功能。
Object类是默认父类，如果在定义类时未指定父类，那么这个类的父类就是Object。

查询类的父类：

    class Hello < String
    end
    Hello.superclass    # => String

查询类的继承关系列表：

    class Hello < String
    end
    Hello.ancestors    # => [Hello, Object, Kernel, BasicObject]

Kernel模块是Ruby的一个核心模块，Ruby程序运行时所需的通用函数都封装在这个模块中，例如`p`方法、`raise`方法。

`alias`方法和`undef`方法待补充。


## 模块

模块和类的不同之处在于模块不能拥有实例，模块不能被继承。

模块常用作命名空间，用于封装常量、方法和类：

    module Chinakr
      Email = 'chinakr@gmail.com'
      class Hello
        def greet
          puts 'Hello world!'
        end
      end
      def hello
        puts "Hello, I'm chinakr!"
      end
      module_function :hello
    end
    Chinakr::Email    # => "chinakr@gmail.com"
    Chinakr.hello    # Hello, I'm chinakr!
    hello = Chinakr::Hello.new
    hello.greet    # Hello world!

    include Chinakr
    Email    # => "chinakr@gmail.com"
    hello()    # Hello, I'm chinakr!
    hello = Hello.new
    hello.greet    # Hello world!

引用模块中常量的语法是`ModuleName::ConstantName`，引用模块中方法的语法是`ModuleName::method_name`，引用模块中类的语法是`ModuleName::ClassName`。
`module_function`关键字用于定义模块函数，模块函数可以通过`ModuleName.module_function_name`直接调用。
`include`关键字用于把模块中的常量、方法和类合并到当前命名空间，以简化调用语法。

利用模块扩展类的实例方法(Mixin)：

    module Hello
      def hello
        puts "Hello #{@name}!"
      end
    end
    class HelloTom
      include Hello
      def initialize
        @name = 'Tom'
      end
    end
    class HelloJerry
      include Hello
      def initialize
        @name = 'Jerry'
      end
    end
    tom = HelloTom.new
    tom.hello    # Hello Tom!
    jerry = HelloJerry.new
    jerry.hello    # Hello Jerry!

`include`关键字用于混入指定模块中的方法(实际上也是合并命名空间)。

Ruby只许一个类拥有一个父类，这种继承模型被称为单一继承模型。单一继承模型使遍历继承关系树变得简单高效。单一继承模型通过Mixin使多个类可以共享相同的功能。

查询类是否包含某个模块：

    module Hello
    end
    class HelloTom
      include Hello
    end
    HelloTom.include? Hello    # => true

调用方法时查找接收者的顺序：

1. 查看对象的类中是否定义了该方法；
2. 查看对象的类包含的模块中是否定义的该方法。
    + 从最后含的那个模块查起。

绕过类直接扩展对象的功能：

    module Hello
      def hello
        puts "Hello #{self}!"
      end
    end
    tom = 'Tom'
    tom.extend Hello
    tom.hello    # Hello Tom!

利用模块扩展类的类方法(Mixin)：

    module Hello
      def hello
        puts 'Hello world!'
      end
    end
    class Tom
      extend Hello
    end
    Tom.hello    # Hello world!


## 异常

异常处理-最简单的情况：

    begin
      # some code that may cause exception
    rescue
      # exception handling
    end

异常处理-获得异常对象：

    begin
      # some code that may cause exception
    rescue => e    # e references exception object
      # exception handling
    end

异常处理-不管是否出现异常都执行指定代码：

    begin
      # some code that may cause exception
    rescue
      # exception handling
    ensure
      # the code that will always execute
    end

可以在rescue中使用`retry`，这样会重新执行bengin中的代码。

rescue修饰符：

    m = Integer('123') rescue 0    # => 123
    n = Integer('abc') rescue 0    # => 0
    n = Integer('abc')    # ArgumentError: invalid value for Integer(): "abc"

指定需要捕捉的异常：

    begin
      # do something
    rescue ExceptionClass1
      # do something
    rescue ExceptionClass2 => e
      # do something
    rescue ExceptionClass3, ExceptionClass4
      # do something
    rescue
      # do something
    end

异常类的继承关系：

* Exception
    + SystemExit
    + NoMemoryError
    + SignalException
    + ScriptError
        - LoadError
        - SyntacError
        - NotImplementationError
    + StandardError
        - RuntimeError
        - SecurityError
        - NameError
            * NoMethodError
        - IOError
            * EOFError
        - SystemCallError
            * Errno::EPERM
            * Errno::ENOENT
            * ...

抛出异常：

    raise message
    raise ExceptionClass
    raise ExceptionClass, message
    raise    # 在rescue中会再次抛出最后一次异常，在rescue外会抛出`RuntimeError`


## 单元测试

参考资料：

  * [Learn Ruby The Hard Way > Exercise 47: Automated Testing](http://learnrubythehardway.org/book/ex47.html)

工作流程：

  1. 编写自动化测试代码；
  2. 编写最少的功能代码，以通过测试；
  3. 在添加、修改功能或重构代码时重复步骤1—2。

以上流程也称为TDD(测试驱动开发)。

测试指南：

  * 测试文件放在`tests/`目录下，以`test_BLAH.rb`命名。这样`rake test`就能找到这些文件。
  * 为每个模块分别编写测试文件。
  * 测试用例要尽可能简短。
  * 必要时应创建帮助函数，以避免在测试用例中出现重复代码。这样有例于代码维护，减少出错的可能性。
  * 必要时应大胆地删除不再有用的测试代码。

示例代码：

`lib/ex47/game.rb`的源代码(实现功能的代码)：


    class Room

      def initialize(name, description)
        @name = name
        @description = description
        @paths = {}
      end

      # these make it easy for you to access the variables
      attr_reader :name
      attr_reader :paths
      attr_reader :description

      def go(direction)
        return @paths[direction]
      end

      def add_paths(paths)
        @paths.update(paths)
      end

    end

`tests/test_ex47.rb`的源代码(实现测试的代码)：


    require "ex47/game.rb"
    require "test/unit"

    class TestGame < Test::Unit::TestCase

        def test_room()
            gold = Room.new("GoldRoom",
                        """This room has gold in it you can grab. There's a
                    door to the north.""")
            assert_equal("GoldRoom", gold.name)
            assert_equal({}, gold.paths)
        end

        def test_room_paths()
            center = Room.new("Center", "Test room in the center.")
            north = Room.new("North", "Test room in the north.")
            south = Room.new("South", "Test room in the south.")

            center.add_paths({'north'=> north, 'south'=> south})
            assert_equal(north, center.go('north'))
            assert_equal(south, center.go('south'))

        end

        def test_map()
            start = Room.new("Start", "You can go west and down a hole.")
            west = Room.new("Trees", "There are trees here, you can go east.")
            down = Room.new("Dungeon", "It's dark down here, you can go up.")

            start.add_paths({'west'=> west, 'down'=> down})
            west.add_paths({'east'=> start})
            down.add_paths({'up'=> start})

            assert_equal(west, start.go('west'))
            assert_equal(start, start.go('west').go('east'))
            assert_equal(start, start.go('down').go('up'))
        end
    end

运行测试：


    rake test

    ...
    Finished in 0.000398 seconds.
    3 tests, 7 assertions, 0 failures, 0 errors


## 常用的标准库

### 使用ERB模板

参考资料：

  * [An Introduction to ERB Templating](http://www.stuartellis.eu/articles/erb/)

模板标签：

    Hello, <%= @name %>.
    Today is <%= Time.now.strftime('%A') %>.

    <% for @item in @shopping_list %>
      <%= @item %>
    <% end %>

    <%# This is just a comment %>

Rails扩展的模板标签(通过`-`来避免产生新行)：

    <% for @item in @items -%>
      <%= @item %>
    <% end -%>

使用模板-方式一：

    require 'erb'

    weekday = Time.now.strftime('%A')
    simple_template = "Today is <%= weekday %>."

    renderer = ERB.new(simple_template)
    puts output = renderer.result()

使用模板-方式二：

    class ShoppingList
      attr_accessor :items, :template

      def render()
        renderer.result(binding)
      end
    end

使用模板-方式三：

    class ShoppingList
      attr_accessor :items

      def initialize(items)
        @items = items
      end

      # Expose private binding() method.
      def get_binding
        binding()
      end

    end

    list = ShoppingList.new(items)
    renderer = ERB.new(template)
    puts output = renderer.result(list.get_binding)

用法小结：

    require 'erb'
    renderer = ERB.new(template_text)
    output = renderer.result()

### 使用Yaml

参考资料：

  * [Yaml Cookbook](http://yaml.org/YAML_for_ruby.html)
  * [How do I parse a YAML file?](http://stackoverflow.com/questions/3877004/how-do-i-parse-a-yaml-file)

示例代码：

`some.yml`的源代码：

    ---
    javascripts:
    - fo_global:
      - lazyload-min
      - holla-min

`parse_yml.rb`的源代码：rair

    require 'yaml'
    thing = YAML.load_file('some.yml')
    puts thing.inspect    # {"javascripts"=>[{"fo_global"=>["lazyload-min", "holla-min"]}]}

## 常用的第三方Gem

### 把Markdown文本转换为HTML(kramdown)

参考资料：

  * [为什么选择kramdown](http://stackoverflow.com/questions/373002/better-ruby-markdown-interpreter)
  * [kramdown项目主页](https://github.com/gettalong/kramdown)

基本用法：

    # Gemfile
    gem 'kramdown'

    # main src file
    require 'kramdown'
    markdown_text = 'This is a **markdown** file.'
    html = Kramdown::Document.new(markdown_text).to_html    # => "<p>This is a <strong>markdown</strong> file.</p>\n"

### 从文本创建图片

参考资料：

  * [How to create a PNG file with text on it?](http://stackoverflow.com/questions/15864443/how-to-create-a-png-file-with-text-on-it)
  * [Rails / Ruby - What gem can create a image with text?](http://stackoverflow.com/questions/10303434/rails-ruby-what-gem-can-create-a-image-with-text)：示例代码。
    * [Rmagick unable to read font](http://stackoverflow.com/questions/28043993/rmagick-unable-to-read-font)：解决找不到字体的问题。
    * [Rails上使用RMagick经验之谈](http://www.it610.com/article/1048584.htm)：如何设置字体，解决中文字符乱码问题。
    * [Chinese in Mac OS X 10.5 Leopard](http://www.yale.edu/chinesemac/pages/osx5.html)：Mac OS X上的中文字体位于`/System/Library/Fonts/`目录下。
    * ImageMagick: Color Names：可选颜色的名称。
    * 更多参考资料：
      * [RMagick的基本使用](http://www.cnblogs.com/lizunicon/p/3675096.html)
      * [Rails上使用RMagick经验之谈](http://www.it610.com/article/1048584.htm)

示例代码：

    brew install gs

    subl Gemfile
    require `rmagick`

    bundle

    subl test_gen_png.rb

    require 'RMagick'
    width = 1200    # picture size
    height = 1600
    fontsize = 42
    string = '坚持和发展中国特色社会主义学习实践活动第三批学习资料'
    margin_top = 450
    canvas = Magick::Image.new(width, height) {self.background_color = 'SkyBlue'}
    gc = Magick::Draw.new
    gc.font('/System/Library/Fonts/PingFang.ttc')
    gc.pointsize(fontsize)
    indent = (width - string.length * fontsize) / 2
    gc.text(indent, margin_top, string)
    gc.draw(canvas)
    canvas.write('tst.png')    # `tst.jpg` is OK too

    ruby test_gen_png.rb; open tst.png

### 调试Ruby程序

参考资料：

* [Using the Ruby Logger](http://hawkins.io/2013/08/using-the-ruby-logger/ "Google关键字：ruby logger")
* [Ruby中打印日志：Logger的使用](http://blog.sina.com.cn/s/blog_573a052b0100qyp4.html "Google关键字：ruby logger")

示例代码：

    require 'logger'
    production_log = File.new '/path/to/production.log', w
    logger = Logger.new production_log
    logger.info 'something'
    logger.warn 'something'
    logger.error 'something'
    logger.fatal 'something'


## 实用技巧

### 判断是否为中英文字符

参考资料：

* `CoffeeScript笔记 > 判断中文字符长度`
* [Getting an ASCII character code in Ruby using `?` (question mark) fails](http://stackoverflow.com/questions/1270209/getting-an-ascii-character-code-in-ruby-using-question-mark-fails "Google关键字：ruby char code")
* [str.each in Ruby isn't working](http://stackoverflow.com/questions/2104319/str-each-in-ruby-isnt-working "Google关键字：ruby string each")
* [How to match Chinese word in Ruby？](http://stackoverflow.com/questions/26033137/how-to-match-chinese-word-in-ruby "Google关键字：ruby char is chinese 2.1")：主要参考资料。
* [How to determine if a character is a Chinese character](http://stackoverflow.com/questions/2727804/how-to-determine-if-a-character-is-a-chinese-character "Google关键字：ruby char is chinese")

示例代码：

    # 匹配中文字符的
    /\p{Han}/ =~ '我们'    # => 0
    /\p{Han}/ =~ 'abc'    # => nil
    /\p{Han}/ =~ '123'    # => nil

    # 匹配英文字母和数字
    /\w+/ =~ '我们'    # => nil
    /\w+/ =~ 'abc'    # => 0
    /\w+/ =~ '123'    # => 0

    # 匹配英文字母
    /[a-zA-Z]+/ =~ '我们'    # => nil
    /[a-zA-Z]+/ =~ 'abc'    # => 0
    /[a-zA-Z]+/ =~ '123'    # => nil

### 把HTML代码转换为纯文本

参考资料：

* [HTML to Plain Text with Ruby?](http://stackoverflow.com/questions/2505104/html-to-plain-text-with-ruby "Google关键字：ruby html to text")

示例代码：

    require 'nokogiri'
    puts Nokogiri::HTML(my_html).text
