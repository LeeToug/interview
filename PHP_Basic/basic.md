1.PHP中的数据类型有哪些？
    4个标量：字符串，整型，浮点型，布尔型
    2个复合型：数组，对象
    2个特殊型：资源，NULL
2.PHP中的数组常用的方法？至少5个
    in_array():判断是否在数组中
    array_unique():数组去重
    array_merge():数组合并
    array_keys():获取数组中所有下标
    array_values():返回数组的所有值
    array_push():将一个或多个元素插入数组的末尾（入栈）
    array_pop():删除数组的最后一个元素（出栈）
    count():返回数组中元素的数目
    sort():数组升序排序
    rsort():数组降序排序
    array_sum():返回数组中值的和
3.session与cookie的区别？
    Session是在服务端保存的一个数据结构，用来跟踪用户 的状态，这个数据可以保存在集群、数据库、文件中
    Cookie是客户端保存用户信息的一种机制，用来记录用户的一些信息，也是实现Session的 一种方式。
4.超级全局变量你知道几个？（9个）
    $GLOABLE:储存全局作用域中的变量
    $_SERVER:获取服务器相关信息
    $_REQUESR:获取POST和GET请求的参数
    $_POST:获取POST请求的参数
    $_GET:获取GET请求的参数
    $_FILES:获取上传文件的变量
    $_ENV:获取服务器环境变量的数组
    $_COOKIE:浏览器cookie的相关操作
    $_SESSION:服务端session的操作
5.魔术变量你知道几个？(记住5个以上即可)
    __FUNCTION__：返回该函数被定义时的名字
    __METHOD__:返回该方法被定义时的名字
    __DIR__:文件所在的目录
    __FILE__:文件的完整路径和文件名
    __LINE__:文件中的当前行号
    __CLASS__:返回该类被定义时的名字
    __NAMESPACE__:当前命名空间的名称（区分大小写）
6.魔术方法你知道几个？(记住5个以上即可)
    __construct():构造函数。实例化对象时被调用，当__construct和以类名为函数名的函数同时存在时，__construct将被调用，另一个不被调用
    __destruct():析构函数。当删除一个对象或对象操作终止时被调用
    __call():对象调用某个方法，若方法存在，则直接调用；若不存在，则会去调用__call函数
    __get(): 读取一个对象的属性时，若属性存在，则直接返回属性值；若不存在，则会调用__get函数
    __set():设置一个对象的属性时，若属性存在，则直接赋值；若不存在，则会调用__set函数
    __toString():打印一个对象的时被调用
    __clone():克隆对象时被调用
    __sleep():serialize(序列化)之前被调用。若对象比较大，想删减一点东东再序列化，可考虑一下此函数
    __unset():unset一个对象的属性时被调用
    __isset(): 检测一个对象的属性是否存在时被调用
    __autoload(): 实例化一个对象时，如果对应的类不存在，则该方法被调用
    __wakeup():unserialize(反序列化)时被调用，做些对象的初始化工作
7.HTTP常见状态码？各是什么含义？
    301（永久移动）
    302（临时移动）
    305（使用代理）
    400（错误请求）服务器不理解请求的语法。
    401（未授权）请求要求身份验证。对于登录后请求的网页，服务器可能返回此响应。
    403（禁止）
    404（未找到）
    408（请求超时）
    500（服务器内部错误）
    502（错误网关）
    503 （服务不可用）
8.include,require,include_once,require_once有什么区别？
    include函数：会将指定的文件读入并且执行里面的程序；
    require函数：会将目标文件的内容读入，并且把自己本身代换成这些读入的内容；
    include_once 函数：在脚本执行期间包含并运行指定文件。此行为和 include 语句类似，唯一区别是如果该文件中已经被包含过，则不会再次包含。如同此语句名字暗示的那样，只会包含一次；
    require_once 函数：和 require 语句完全相同，唯一区别是 PHP 会检查该文件是否已经被包含过，如果是则不会再次包含。
    include与require除了在处理引入文件的方式不同外，最大的区别就是：include在引入不存文件时产生一个警告且脚本还会继续执行，而require则会导致一个致命性错误且脚本停止执行
9.error_reporting的作用？有哪些级别？
    设置 PHP 的报错级别并返回当前级别
     error_reporting(0):关闭错误报告
     error_reporting(E_ERROR | E_WARNING | E_PARSE):报告 runtime 错误
     error_reporting(E_ALL):报告所有错误
     ini_set("error_reporting", E_ALL):等同 error_reporting(E_ALL);
     error_reporting(E_ALL & ~E_NOTICE):报告 E_NOTICE 之外的所有错误
10.echo、print_r、print、var_dump区别？
    echo：语句结构；
    print：是函数，有返回值
    print_r：能打印数组，对象
    var_dump:能打印对象数组，并且带数据类型
11.如何把一个GB2312格式的字符串转换成UTF-8格式？
    iconv()函数
12.简述 private、 protected、 public修饰符的访问权限
    private : 私有成员, 在类的内部才可以访问。
    protected : 保护成员，该类内部和继承类中可以访问。
    public : 公共成员，完全公开，没有访问限制。
13.$this和self、parent这三个关键词分别代表什么？在哪些场合下使用？
    $this  当前对象
    self   当前类
    parent 当前类的父类
14.isset() 和 empty() 区别？
    isset判断变量是否存在，可以传入多个变量，若其中一个变量不存在则返回假；empty判断变量是否为空为假，只可传一个变量，如果为空为假则返回真
15.MVC分别指哪三层，有什么优点？
    MVC三层分别指：业务模型、视图、控制器，由控制器层调用模型处理数据，然后将数据映射到视图层进行显示，优点是：①可以实现代码的重用性，避免产生代码冗余；②M和V的实现代码分离，从而使同一个程序可以使用不同的表现形式
    
    
