# phpcareer
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/1463244-4ea2cb09f63e19d1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
# 一、开发环境

学习一门语言，首先要搞定的就是环境的配置
想要比较开心的开发php，你就需要搞定这几个
* PHP
* Apache
* MySQL
具体的环境配置自行百度
这里给出几种集成环境的选择
* phpstudy
* WAMPSERVER
* appserv
以上几种都是在windows下的集成环境
在linux下的环境配置如果有需要的可以联系我，在这里就不讲了
# 二、编辑器
推荐几款编辑器
1. notepad++
2. sublime text
3. Atom
4. editplus
根据个人喜好选择，重点是下面的
# 三、php简介

php是世界上最好的语言（yes or no?）

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/1463244-1dc330ec5e879c7e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
那么，php到底是不是世界上最好的语言呢，其实不是的。
>三个程序员坐在格子间里编程。
一个程序员一言不发，他用的是python.
一个程序员写一会儿就按一下编译，然后就玩会儿手机。他用的是C++。
一个程序员坐在那里浏览网页，不时飞快的键入一些字符。
经理看到，怒道：你怎么不干活，尽在上网。
回答：我在查实现这个功能需要用什么函数。
他用的是PHP.

php语言的劣势：

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/1463244-7b19aabe1655fe6d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

http://m.oschina.net/question/1579_49262
（想要深入了解php特性的可以看一下这篇文章）
基于以上特点，我们基本可以得出一个结论：php不是所谓的最优语言。

但我们为什么要学习php呢？

>1、开源性和免费性。由于PHP的解释器的源代码是公开的，所以安全系数较高的网站可以自己更改PHP的解释程序。另外，PHP运行环境的使用也是免费的。

>2、跨平台性强。由于PHP的解释器是开源的，所以能够在所有的操作系统平台上非常稳定地运行，这使它成为常用的服务器语言。

>3、快捷性。PHP是一种非常容易学习和使用的一门语言，它的语法特点类似于C语言，但又没有C语言复杂的地址操作，而且又加入了面向对象的概念，再加上它具有简洁的语法规则，使得它操作编辑非常简单，实用性很强。

>4、面向过程和面向对象并用。在PHP语言的使用中，可以分别使用面向过程和面向对象，而且可以将PHP面向过程和面向对象两者一起混用，这是其他很多编程语言是做不到的。

>5、运行高效性。由于PHP运行在相应的平台解释器上，消耗系统资源比较少，运行的环境简单，所以效率就很高。

>6、数据库连接的广泛性。PHP可以与很多主流的数据库建立起连接，如MySQL、ODBC、Oracle、AdabasD、S等，PHP是利用编译的不同函数与这些数据库建立起连接的，PHPLIB就是常用的为一般事务提供的基库。

# 四、php代码规范
>格式

PHP 脚本可放置于文档中的任何位置， 以<?php 开头，以 ?>结束
`<?php
// 这里是PHP 代码
?>`
实例
```
<!DOCTYPE html> 
  <html>
   <body>
     <h1>看看下面PHP的结果是什么</h1>
     <?php echo "hello, world"; ?>
   </body>
 </html>```

>大小写敏感与否

* 用户定义的函数、类和关键字
在 PHP 中，所有用户定义的函数、类和关键字（例如 if、else、echo 等等）都对大小写不敏感。在下面的例子中，所有这三天 echo 语句都是合法的（等价）：
```
<!DOCTYPE html>
     <html>
    <body>
      <?php
        ECHO "Hello World!<br>";
        echo "Hello World!<br>";
        EcHo "Hello World!<br>";
      ?>
    </body>
</html>
```
* PHP 变量：
变量以 $ 符号开头，其后是变量的名称
变量名称必须以字母或下划线开头，变量名称不能以数字开头，变量名称只能包含字母数字字符和下划线（A-z、0-9 以及 _）变量名称*对大小写敏感* （$y 与 $Y 是两个不同的变量）
实例：
```
<!doctype html>
   <html>
     <body>
      <?php 
        $x=6;
        $y=7; 
        $z=$x+$y;
        echo $z;
       ?>
      </body>
   </html>```
#五、php基本语法

>数据类型

在PHP中，支持8种原始类型，其中包括四种标量类型、两种复合类型和两种特殊类型。
* String（字符串）, Integer（整型）, Float（浮点型）, Boolean（布尔型）,
* Array（数组）, Object（对象）, 
* NULL（空值）,resource（资源）

*  String
字符串是由一系列字符组成，在PHP中，字符和字节一样，也就是说，一共有256种不同字符的可能性。字符串型可以用三种方法定义：单引号形式、双引号形式和Heredoc结构形式。
  * 当字符串中包含引号的时候，有三种解决方案：
    1. 在单引号中嵌入双引号
    2. 在双引号中嵌入单引号
    3. 使用转义符“\”
  * 当引号中包含『$』符号时，该怎么办？
    1. 当双引号中包含变量时，变量会与双引号中的内容连接在一起；
    2. 当单引号中包含变量时，变量会被当做字符串输出。
  * 当字符串很长时怎么办?
  我们可以使用Heredoc结构形式的方法来解决该问题，首先使用定界符表示字符串（<<<），接着在“<<<“之后提供一个标识符GOD，然后是字符串，最后以提供的这个标识符结束字符串。如下：
```
<?php 
$string1 = <<<GOD
我有一只小毛驴，我从来也不骑。
有一天我心血来潮，骑着去赶集。
我手里拿着小皮鞭，我心里正得意。
不知怎么哗啦啦啦啦，我摔了一身泥.
GOD;
echo $string1;
?>
```
在赋值符号后，输入定界符“<<<”,接着是标识符，你可以用你的女神作为标识符“GOD”，如第2行，也可以使用你喜欢的狗 狗，“DOG”作为标识符，但是，结尾处的标识符也必须是一样的。此外，在结尾的一行，如第7行，一定要另起一行，并且此行除了“GOD”，并以“；”号 结束之外，不能有任何其他字符，前后都不能有，包括空格，否则会出现错误的



```
<?php 
$x = "Hello world!";
echo $x;
echo "<br>"; 
$x = 'Hello world!';
echo $x;
?>
```
* Integer
  * 整数必须至少有一个数字 (0-9)
  * 整数不能包含逗号或空格
  * 整数是没有小数点的
  * 整数可以是正数或负数
  * 整型可以用三种格式来指定：十进制， 十六进制（ 以 0x 为前缀）或八进制（前缀为 0）
```
<?php 
$x = 5985;
var_dump($x);
echo "<br>"; 
$x = -345; // 负数 
var_dump($x);
echo "<br>"; 
$x = 0x8C; // 十六进制数
var_dump($x);
echo "<br>";
$x = 047; // 八进制数
var_dump($x);
?>
```
* Array
```
<?php
 $cars=array("Volvo","BMW","Toyota");
var_dump($cars);
?>
```
* Object
对象数据类型也可以用于存储数据。
在 PHP 中，对象必须声明。
首先，你必须使用class关键字声明类对象。类是可以包含属性和方法的结构。
然后我们在类中定义数据类型，然后在实例化的类中使用数据类型：
```
<?php
class Car
{
  var $color;
  function Car($color="green") {
    $this->color = $color;
  }
  function what_color() {
    return $this->color;
  }
}
?>
```

* 第一种特殊类型---资源 resource

资源（resource）：资源是由专门的函数来建立和使用的，例如打开文件、数据连接、图形画布。我们可以对资源进行操作（创建、使用和释放）。任何资 源，在不需要的时候应该被及时释放。如果我们忘记了释放资源，系统自动启用垃圾回收机制，在页面执行完毕后回收资源，以避免内存被消耗殆尽。
```
<?php 
//首先采用“fopen”函数打开文件，得到返回值的就是资源类型。
$file_handle = fopen("/data/webroot/resource/php.f.txt","r");
if ($file_handle){
//接着采用while循环（后面语言结构语句中的循环结构会详细介绍）一行行地读取文件，然后输出每行的文字
while (!feof($file_handle)) { //判断是否到最后一行
    $line = fgets($file_handle); //读取一行文本
       echo $line; //输出一行文本
      echo "<br />"; //换行
}
}
fclose($file_handle);//关闭文件
?>

```
* 第二种特殊类型---空类型（NULL）
NULL（NULL）：NULL是空类型，对大小写不敏感，NULL类型只有一个取值，表示一个变量没有值，当被赋值为NULL，或者尚未被赋值，或者被unset()，这三种情况下变量被认为为NULL。


>php常量

PHP中的常量分为系统常量和自定义常量。
* 系统常量
PHP已经定义好的常量，我们可以直接拿来使用，常见的系统常量有：
	* FILE :php程序文件名。它可以帮助我们获取当前文件在服务器的物理位置。
	* LINE :PHP程序文件行数。它可以告诉我们，当前代码在第几行。
	* PHP_VERSION:当前解析器的版本号。它可以告诉我们当前PHP解析器的版本号，我们可以提前知道我们的PHP代码是否可被该PHP解析器解析。
	* PHP_OS：执行当前PHP版本的操作系统名称。它可以告诉我们服务器所用的操作系统名称，我们可以根据该操作系统优化我们的代码。
* 常量如何使用？
定义了常量，那么就要使用常量，那么如何获取常量值呢？
获取常量值的有两种方法取值。
  * 第一种是使用常量名直接获取值；例如计算圆周率的面积，如下:
```
<?php
define("PI",3.14);
$r=1;
$area = PI*$r*$r; //计算圆的面积
?>
```
  * 第二种是使用constant()函数。它和直接使用常量名输出的效果是一样的，但函数可以动态的输出不同的常量，在使用上要灵活、方便，其语法格式如下：
mixed constant(string constant_name)
第一个参数constant_name为要获取常量的名称，也可为存储常量名的变量。如果成功则返回常量的值，失败则提示错误信息常量没有被定义。（注：mixed表示函数返回值类型为多种不同的类型，string表示参数类型为字符串类型）
```
<?php 
$p="";
//定义圆周率的两种取值
define("PI1",3.14);
define("PI2",3.142);
//定义值的精度
$height = "中";
//根据精度返回常量名，将常量变成了一个可变的常量
if($height == "中"){
$p = "PI1";
}else if($height == "低"){
$p = "PI2";
}
$r=1;
$area = constant($p)*$r*$r;
echo $area;
?>
```
* 如何判定常量是否被定义
如果常量被重复定义以后，PHP解析器会发出“Constant XXX already defined”的警告，提醒我们该常量已经被定义过。那么，在团队开发，或代码量很大的情况下，我们如何去判定一个常量是否被定义呢？
defined()函数可以帮助我们判断一个常量是否已经定义，其语法格式为：
bool defined(string constants_name)
它只有参数constant_name，指的是要获取常量的名称，若存在则返回布尔类型true，否则返回布尔类型false; 
```
// PHP5以后可以用来定义常量的方法
const  value1 = 10;
echo value1;
echo  "<br>";
// PHP5之前定义常量的方法
define("value2",20);
echo value2;
```
define() 函数 - 有三个参数：首个参数定义常量的名称第二个参数定义常量的值可选的第三个参数规定常量名是否对大小写敏感。默认是 false。

>有关字符串处理的一些函数

```
$str = "Hello PHP";
//strlen() 函数返回字符串的长度，以字符计。
//获取指定字符在字符串中的位置
echo  strpos($str,"P")."<br>";
//截取指定位置的字符串（从第2个字符到最后）
$str1 = substr($str,2);
//截取指定位置的字符串（从第2个字符开始往后截取3位）
$str2 = substr($str,2,2);
//以指定间距分割字符串
$str3 = str_split($str);
$str4 = str_split($str,2);
print_r($str4)."<br>";
//以指定字符分割字符串
$str = "PHP JAVA JS HTML CSS";
$str5 = explode(" ",$str);
print_r($str5)."<br>";

```

> 运算符

* 四则运算符
+ , - , * , / , %
* 赋值运算符
"=" : 把右边表达式的值赋给左边的运算数。它将右边表达式值复制一份，交给左边的运算数。换而言之，首先给左边的运算数申请了一块内存，然后把复制的值放到这个内存中。
"&" : 引用赋值，意味着两个变量都指向同一个数据。它将使两个变量共享一块内存，如果这个内存存储的数据变了，那么两个变量的值都会发生变化。

* 比较运算符

* 逻辑运算符
and 逻辑与
&& 逻辑与
or 逻辑或
|| 逻辑或
xor 逻辑异或
！ 逻辑非

* 字符串连接运算符
连接运算符("."): 它返回将右参数附加到左参数后面所得的字符串。
连接赋值运算符(".="): 它将右边的参数附加到左边的参数后。
* 错误控制运算符
PHP中提供了一个错误控制运算符“@”，对于一些可能会在运行过程中出错的表达式时，我们不希望出错的时候给客户显示错误信息，这样对用户不友好。于是，可以将@放置在一个PHP表达式之前，该表达式可能产生的任何错误信息都被忽略掉；
如果激活了track_error（这个玩意在php.ini中设置）特性，表达式所产生的任何错误信息都被存放在变量$php_errormsg中，此变量在每次出错时都会被覆盖，所以如果想用它的话必须尽早检查。
需要注意的是：错误控制前缀“@”不会屏蔽解析错误的信息，不能把它放在函数或类的定义之前，也不能用于条件结构例如if和foreach等。
```
<?php  
$conn = @mysql_connect("localhost","username","password");
echo "出错了，错误原因是：".$php_errormsg;
?>
```



> PHP foreach 循环

```
<?php 
$colors = array("red","green","blue","yellow"); 

foreach ($colors as $value) {
  echo "$value <br>";
}
?>
```


关联数组的概念(键值对)
```
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
$age['Peter']="35";
$age['Ben']="37";
$age['Joe']="43";
```
在PHP中foreach循环语句，常用于遍历关联数组，一般有两种使用方式:不取下标、取下标。
* 只取值，不取下标
```
<?php
foreach (数组 as 值){
//执行的任务
}
?>
```
示例:
```
<?php
$students = array(
'2010'=>'令狐冲',
'2011'=>'林平之',
'2012'=>'曲洋',
'2013'=>'任盈盈',
'2014'=>'向问天',
'2015'=>'任我行',
'2016'=>'冲虚',
'2017'=>'方正',
'2018'=>'岳不群',
'2019'=>'宁中则',
);//10个学生的学号和姓名，用数组存储
//使用循环结构遍历数组,获取学号和姓名  
foreach($students as $key)
{ 
echo $key;          
echo "<br />";
}
?>
```
同时取下标和值
```
<?php
foreach (数组 as 下标 => 值){
//执行的任务
}
?>
```
示例:
```
<?php
$students = array(
'2010'=>'令狐冲',
'2011'=>'林平之',
'2012'=>'曲洋',
'2013'=>'任盈盈',
'2014'=>'向问天',
'2015'=>'任我行',
'2016'=>'冲虚',
'2017'=>'方正',
'2018'=>'岳不群',
'2019'=>'宁中则',
);//10个学生的学号和姓名，用数组存储
//使用循环结构遍历数组,获取学号和姓名  
foreach($students as $key => $value)
{ 
echo $value;          //输出（打印）姓名
echo "<br />";
}
?>
```



>PHP global 关键词

global 关键词用于访问函数内的全局变量。
要做到这一点，请在（函数内部）变量前面使用 global 关键词：
```
<?php
$x=5;
$y=10;
function myTest() {
   global $x,$y;
   $y=$x+$y;
} 
myTest(); // 运行函数
echo $y; // 输出变量 $y 的新值
?>```

>PHP echo 和 print 语句

echo 和 print 之间的差异：
echo - 能够输出一个以上的字符串
print - 只能输出一个字符串，并始终返回 1

提示：echo 比 print 稍快，因为它不返回任何值。
```
<?php
echo "<h2>PHP is fun!</h2>";
echo "Hello world!<br>";
echo "I'm about to learn PHP!<br>";
echo "This", " string", " was", " made", " with multiple parameters.";
?>

显示变量
下面的例子展示如何用 echo 命令来显示字符串和变量：
<?php
$txt1="Learn PHP";
$txt2="W3School.com.cn";
$cars=array("Volvo","BMW","SAAB");

echo $txt1;
echo "<br>";
echo "Study PHP at $txt2";
echo "My car is a {$cars[0]}";
?>
```

>几个常用的php库函数



打印某一个变量的类型和值：var_dump()
```
$a = "abc";
var_dump($a);      //string(3) "abc"
print_r("abc");
```
返回一个变量的所有数据
```
$arr = var_export($array);
获取某个变量的类型名称：gettype()
echo gettype($a);      //string
```
判断一个变量是否为某个类型：is_int  is_bool is_string
```
if(is_string($a)){
    echo "\n is string";      //is string
}
```
强制装换：set type($var, $type)或($type)$a
```
(int)$a;
settype($a,int);
```
* PHP 日期和时间
	* PHP Date() 函数
	```
date(format,timestamp)
```
	* 通过 PHP mktime() 创建日期
	```
mktime(hour,minute,second,month,day,year)
```
	 通过 PHP strtotime() 用字符串来创建日期
	```
strtotime(time,now)
strtotime("10:38pm April 15 2015");
```
```
<?php
$d=strtotime("tomorrow");
echo date("Y-m-d h:i:sa", $d) . "<br>";
$d=strtotime("next Saturday");
echo date("Y-m-d h:i:sa", $d) . "<br>";
$d=strtotime("+3 Months");
echo date("Y-m-d h:i:sa", $d) . "<br>";
?>
```

others:

* “memory_get_usage”获取当前PHP消耗的内存

* error_reporting(0); 禁止显示PHP警告提示
