# 基础&进阶篇
## 1.什么是java
java 是一门面向对象的高级编程语言，不仅吸收了C++的各种优点，比如继承了C++语言面向对象的技术核心。
还摒弃了C++里难以理解的#多继承，指针等概念，同时也增加了#垃圾回收机制，释放掉不被使用的内存空间，解决了管理内存空间的烦恼
因此java语言具有功能强大和简单易用两个特征。java语言作为#静态面向对象编程语言的代表，极好的实现了面向对象理论，允许程序员以
优雅的思维方式进行复杂编程。

## 2.Java的特点有哪些
java语言是一种#分布式的面向对象语言，具有面向对象，平台无关性，简单性，解释执行，多线程，安全性等很多特点。
1.面向对象
Java是一种面向对象的语言，它对对象中的类，对象，继承，多态，封装，接口，包等均有很好的支持。
为了简单起见，java只支持类之间的单继承，但是可以使用#接口来实现多继承，使用java语言开发程序，
需要采用面向对象的思想设计程序和编写代码

2. 平台无关性
3. 简单性
Java语言的语法与C语言和C++语言很相近，使得很多程序员学起来很容易。对java来说，它舍弃了很多C++中难以理解的特性
如#操作符的重载和多继承
4.解释执行
java程序在java平台运行时会被编译成#字节码文件，然后可以在有java环境的操作系统上运行。
在运行文件时，Java的解释器对这些字节码进行解释执行，执行过程中需要加入的类在连接阶段被载入到运行环境中
5. 多线程
java语言是多线程的，这也是Java语言的一大特性，它必须由#thread类和它的子类来创建。
Java支持多个线程同时执行，并提供多线程之间的同步机制，任何一个线程都有自己的run（）方法，要执行的方法就写在run（）方法体内
6.分布式
Java语言支持internet应用的开发，在java的#基本应用编程接口中就有一个网络应用编程接口，它提供了网络应用编程的类库，
包括URL，URLConnection，Socket等，java的#RIM机制也是开发分布式应用的重要手段。
7. 健壮性
java的强类型机制，异常处理，垃圾回收机制都是java健壮性的重要保证，对指针的丢弃是java的一大进步。
另外，java的异常机制也是健壮性的一大体现
8.高性能
java的高性能主要是相对其他高级脚本语言来说的，随着JIT(just in time， 即时编译器) 的发展，java的运行速度也越来越高
9.安全性
java通常被用在网络环境中，为此，java提供了一个安全机制以防止恶意代码攻击。除了Java语言具有许多安全特性之外，Java还对通过网络下载的类增加一个安全防范机制，分配不同的命名空间以防替代本地的同名类，并包含安全管理机制

## 3. JDK和JRE和JVM的区别
1.JDK（java SE Development Kit）,Java标准的开发包，提供了编译、运行Java程序所需要的各种工具
和资源，包括了Java编译器、Java运行时环境、以及常用的Java类库等。

2. JRE
JRE（Java Runtime Environment），Java运行时环境，用于解释执行Java的字节码文件。普通用户只
需要安装JRE来运行Java程序即可，而作为一名程序员必须安装JDK，来编译、调试程序。

3. JVM
JVM(java virtual mechinal), java虚拟机，是JRE的一部分。它是整个java实现跨平台的核心，负责解释执行字节码文件，是可运行Java字节码文件的虚拟计算机。所有平台上的JVM向编译器提供相同的接口，而编译器只需要面向虚拟机，生成虚拟机能识别的代码，然后由虚拟机来解释执行。
当使用java编译器编译java程序时，生成的是与平台无关的字节码，这些字节码只面向JVM，也就是说JVM是运行java字节码的虚拟机。
为什么要采用字节码
在java中，JVM可以理解的代码就叫做字节码（即.class文件），他不面向任何特定的处理器，只面向虚拟机。java语言通过字节码的方式，在一定程度上解决了#传统解释型语言执行效率低的问题，同时又保留了解释型语言可移植的特点。
所以 Java 程序运行时比较高效，而且，由于字节码并不针对一种特定的机器，因此，Java 程序无
须重新编译便可在多种不同操作系统的计算机上运行。
### java程序从源代码到运行，3步：
![image](https://user-images.githubusercontent.com/6525034/141608397-6bfae8cb-cd60-4120-9b94-b4d422345084.png)
## 4. Oracle JDK和OpenJDK的对比
+ oracleJDK版本将每三年发布一次，而openJDK每三个月发布一次
+ OpenJDK 是一个参考模型并且是完全开源的，而Oracle JDK是OpenJDK的一个实现，并不是完全开源的；
+ Oracle JDK 比 OpenJDK 更稳定。OpenJDK和Oracle JDK的代码几乎相同，但Oracle JDK有更多的
类和一些错误修复。因此，如果您想开发企业/商业软件，我建议您选择Oracle JDK，因为它经过了彻底的测试和稳定。某些情况下，有些人提到在使用OpenJDK 可能会遇到了许多应用程序崩溃的问题，但是，只需切换到Oracle JDK就可以解决问题；
+ 在响应性和JVM性能方面，Oracle JDK与OpenJDK相比提供了更好的性能；
+ Oracle JDK不会为即将发布的版本提供长期支持，用户每次都必须通过更新到最新版本获得支持来获取最新版本；
+ Oracle JDK根据#二进制代码许可协议获得许可，而OpenJDK根据GPL v2许可获得许可。
## java有哪些数据类型
Java中有 8 种基本数据类型，分别为：
6种数字类型：#四个整形两个浮点型：byte，short，int，long，float，double
1种字符类型：char
1种布尔类型： boolean
![image](https://user-images.githubusercontent.com/6525034/141609695-e447b14c-d89b-4623-a7e4-cb067c546230.png)


#byte：
+ byte 数据类型是8位、有符号的，以二进制补码表示的整数；
+ 最小值是 -128（-2^7）；
+ 最大值是 127（2^7-1）；
+ 默认值是 0；
+ byte 类型用在大型数组中节约空间，主要代替整数，因为 byte 变量占用的空间只有 int 类型的四分之一；
+ 例子：byte a = 100，byte b = -50。

short：
+ short 数据类型是 16 位、有符号的以二进制补码表示的整数
+ 最小值是 -32768（-2^15）；
+ 最大值是 32767（2^15 - 1）；
+ Short 数据类型也可以像 byte 那样节省空间。一个short变量是int型变量所占空间的二分之一；
+ 默认值是 0；
+ 例子：short s = 1000，short r = -20000。

#int：
+ int 数据类型是32位、有符号的以二进制补码表示的整数；
+ 最小值是 -2,147,483,648（-2^31）；
+ 最大值是 2,147,483,647（2^31 - 1）；
+ 一般地整型变量默认为 int 类型；
+ 默认值是 0 ；

long：
+ 注意：Java 里使用 long 类型的数据一定要在数值后面加上 L，否则将作为整型解析
+ long 数据类型是 64 位、有符号的以二进制补码表示的整数；
+ 最小值是 -9,223,372,036,854,775,808（-2^63）；
+ 最大值是 9,223,372,036,854,775,807（2^63 -1）；
+ 这种类型主要使用在需要比较大整数的系统上；
+ 默认值是 0L；
+ 例子： long a = 100000L，Long b = -200000L。
+ "L"理论上不分大小写，但是若写成"l"容易与数字"1"混淆，不容易分辩。所以最好大写。

float：
+ float 数据类型是单精度、32位、符合IEEE 754标准的浮点数；
+ float 在储存大型浮点数组的时候可节省内存空间；
+ 默认值是 0.0f；
+ 浮点数不能用来表示精确的值，如货币；
+ 例子：float f1 = 234.5f。
double：
+ double 数据类型是双精度、64 位、符合IEEE 754标准的浮点数；
+ 浮点数的默认类型为double类型；
+ double类型同样不能表示精确的值，如货币；
+ 默认值是 0.0d；
+ 例子：double d1 = 123.4。
char：
+ char类型是一个单一的 16 位 Unicode 字符；
+ 最小值是 \u0000（即为 0）；
+ 最大值是 \uffff（即为 65535）；
+ char 数据类型可以储存任何字符；
+ 例子：char letter = 'A';（单引号）
boolean：
+ boolean数据类型表示一位的信息；
+ 只有两个取值：true 和 false；
+ 这种类型只作为一种标志来记录 true/false 情况；
+ 默认值是 false；
+ 例子：boolean one = true。
#这八种基本类型都有对应的包装类分别为：Byte、Short、Integer、Long、Float、Double、
Character、Boolean

## 6. Java中引用数据类型有哪些，它们与基本数据类型有什么区别？
引用数据类型分3种：类，接口，数组；
简单来说,只要不是基本数据类型.都是引用数据类型。 那他们有什么不同呢？
1、从概念方面来说
1,基本数据类型:变量名指向具体的数值
2,引用数据类型:变量名不是指向具体的数值,而是指向存数据的内存地址,.也及时hash值
2、从内存的构建方面来说(内存中,有堆内存和栈内存两者)
1,基本数据类型:被创建时,在栈内存中会被划分出一定的内存,并将数值存储在该内存中.
2,引用数据类型:被创建时,首先会在栈内存中分配一块空间,然后在堆内存中也会分配一块具体的空间用来
存储数据的具体信息,即hash值,然后由栈中引用指向堆中的对象地址.

举个例子
![image](https://user-images.githubusercontent.com/6525034/141610446-4ef27ccf-6a6f-4177-bed5-933cee0ad40c.png)

由上图可知，基本数据类型中会存在两个相同的1，而引用型类型就不会存在相同的数据。
假如"hello"的引用地址是xxxxx1，声明str变量并其赋值"hello"实际上就是让str变量引用了"hello"的内
存地址，这个内存地址就存储在堆内存中，是不会改变的，当再次声明变量str1也是赋值为"hello"时，
此时就会在堆内存中查询是否有"hello"这个地址，如果堆内存中已经存在这个地址了，就不会再次创建
了，而是让str1变量也指向xxxxx1这个地址，如果没有的话，就会重新创建一个地址给str1变量。
从使用方面来说
1,基本数据类型:判断数据是否相等，用==和!=判断。
2,引用数据类型:判断数据是否相等，用equals()方法,==和!=是比较数值的。而equals()方法是比较内存
地址的。
补充：数据类型选择的原则
+ 如果要表示整数就使用int，表示小数就使用double；
+ 如果要描述日期时间数字或者表示文件（或内存）大小用long；
+ 如果要实现内容传递或者编码转换使用byte；
+ 如果要实现逻辑的控制，可以使用booleam；
+ 如果要使用中文，使用char避免中文乱码；
+ 如果按照保存范围：byte < int < long < double

## 8. Java中的自动装箱与拆箱
从下面的代码中就可以看到装箱和拆箱的过程

![image](https://user-images.githubusercontent.com/6525034/141610634-40371a8b-3c5f-4c85-9bd6-7d954f3ec950.png)
对于Java的自动装箱和拆箱，我们看看源码编译后的class文件，其实装箱调用包装类的valueOf方法，
拆箱调用的是Integer.Value方法，下面就是变编译后的代码：
常见面试一：
这段代码输出什么？
public class Main {
public static void main(String[] args) {
Integer i1 = 100;
Integer i2 = 100;
Integer i3 = 200;
Integer i4 = 200;
System.out.println(i1==i2);
System.out.println(i3==i4);
}
}
答案是:
true
false
为什么会出现这样的结果？输出结果表明i1和i2指向的是同一个对象，而i3和i4指向的是不同的对象。此
时只需一看源码便知究竟，下面这段代码是Integer的valueOf方法的具体实现：

public static Integer valueOf(int i) {
if(i >= -128 && i <= IntegerCache.high)
return IntegerCache.cache[i + 128];
else
return new Integer(i);
}
private static class IntegerCache {
static final int high;
static final Integer cache[];
static {
final int low = -128;
// high value may be configured by property
int h = 127;
if (integerCacheHighPropValue != null) {
// Use Long.decode here to avoid invoking methods that
// require Integer's autoboxing cache to be initialized
int i = Long.decode(integerCacheHighPropValue).intValue();
i = Math.max(i, 127);
// Maximum array size is Integer.MAX_VALUE
h = Math.min(i, Integer.MAX_VALUE - -low);
}
high = h;
cache = new Integer[(high - low) + 1];
int j = low;
for(int k = 0; k < cache.length; k++)
cache[k] = new Integer(j++);
}
private IntegerCache() {}
}
从这2段代码可以看出，在通过valueOf方法创建Integer对象的时候，如果数值在[-128,127]之间，便返
回指向IntegerCache.cache中已经存在的对象的引用；否则创建一个新的Integer对象。
上面的代码中i1和i2的数值为100，因此会直接从cache中取已经存在的对象，所以i1和i2指向的是同一
个对象，而i3和i4则是分别指向不同的对象

常见面试二：

public class Main {
public static void main(String[] args) {
Double i1 = 100.0;
Double i2 = 100.0;
Double i3 = 200.0;
Double i4 = 200.0;
System.out.println(i1==i2);
System.out.println(i3==i4);
}
}
输出结果为：
false
false
原因很简单，在某个范围内的整型数值的个数是有限的，而浮点数却不是。

9. 为什么要有包装类型？
让基本数据类型也具有对象的特征
二者的区别：
1. 声明方式不同：基本类型不使用new关键字，而包装类型需要使用new关键字来在堆中分配存储空
间；
2. 存储方式及位置不同：基本类型是直接将变量值存储在栈中，而包装类型是将对象放在堆中，然后
通过引用来使用；
3. 初始值不同：基本类型的初始值如int为0，boolean为false，而包装类型的初始值为null；
4. 使用方式不同：基本类型直接赋值直接使用就好，而包装类型在集合如Collection、Map时会使用
到。

## 10. a=a+b与a+=b有什么区别吗?

+= 操作符会进行隐式自动类型转换,此处a+=b隐式的将加操作的结果类型强制转换为持有结果的类型,而
a=a+b则不会自动进行类型转换.如：
byte a = 127;
byte b = 127;
b = a + b; // 报编译错误:cannot convert from int to byte
b += a;

以下代码是否有错,有的话怎么改？
short s1= 1;
s1 = s1 + 1;
有错误.short类型在进行运算时会自动提升为int类型,也就是说 s1+1 的运算结果是int类型,而s1是short
类型,此时编译器会报错.
正确写法：

short s1= 1;
s1 += 1;

+= 操作符会对右边的表达式结果强转匹配左边的数据类型,所以没错.

## 11. 能将 int 强制转换为 byte 类型的变量吗？如果该值大于 byte 类型的范围，将会出现什么现象？

我们可以做强制转换，但是 Java 中 int 是 32 位的，而 byte 是 8 位的，所以，如果强制转化，int 类型
的高 24 位将会被丢弃，因为byte 类型的范围是从 -128 到 127

## 12. Java程序是如何执行的
我们日常的工作中都使用开发工具（IntelliJ IDEA 或 Eclipse 等）可以很方便的调试程序，或者是通过打
包工具把项目打包成# jar 包或者 war 包，放入 Tomcat 等 Web 容器中就可以正常运行了，但你有没有想
过 Java 程序内部是如何执行的？其实不论是在开发工具中运行还是在 Tomcat 中运行，Java 程序的执行
流程基本都是相同的，它的执行流程如下：

先把 Java 代码编译成字节码，也就是把 .java 类型的文件编译成 .class 类型的文件。这个过程的大
致执行流程：Java 源代码 -> 词法分析器 -> 语法分析器 -> 语义分析器 -> 字符码生成器 -> 最终生成
字节码，其中任何一个节点执行失败就会造成编译失败；
把 class 文件放置到 Java 虚拟机，这个虚拟机通常指的是 Oracle 官方自带的 Hotspot JVM；
Java 虚拟机使用类加载器（Class Loader）装载 class 文件；
类加载完成之后，会进行字节码效验，字节码效验通过之后 JVM 解释器会把字节码翻译成机器码交
由操作系统执行。但不是所有代码都是解释执行的，JVM 对此做了优化，比如，以 Hotspot 虚拟机
来说，它本身提供了 JIT（Just In Time）也就是我们通常所说的动态编译器，它能够在运行时将热
点代码编译为机器码，这个时候字节码就变成了编译执行。Java 程序执行流程图如下：


![image](https://user-images.githubusercontent.com/6525034/141611496-210b9d52-f7ee-4e60-aa68-39522b1ef83b.png)

## 13. final 在 Java 中有什么作用？

#final作为Java中的关键字可以用于三个地方。用于修饰类、类属性和类方法。
特征：凡是引用final关键字的地方皆不可修改！
(1)修饰类：表示该类不能被继承；
(2)修饰方法：表示方法不能被重写；
(3)修饰变量：表示变量只能一次赋值以后值不能被修改（常量）。

## 14. final有哪些用法?
final也是很多面试喜欢问的地方,但我觉得这个问题很无聊,通常能回答下以下5点就不错了:
被final修饰的类不可以被继承
被final修饰的方法不可以被重写
被final修饰的变量不可以被改变.如果修饰引用,那么表示引用不可变,引用指向的内容可变.
被final修饰的方法,JVM会尝试将其内联,以提高运行效率
被final修饰的常量,在编译阶段会存入常量池中.
除此之外,编译器对final域要遵守的两个重排序规则更好:
在构造函数内对一个final域的写入,与随后把这个被构造对象的引用赋值给一个引用变量,这两个操作之间
不能重排序 初次读一个包含final域的对象的引用,与随后初次读这个final域,这两个操作之间不能#重排序.
## 15. static都有哪些用法?

所有的人都知道static关键字这两个基本的用法:静态变量和静态方法.也就是被static所修饰的变量/方法
都属于类的静态资源,类实例所共享.
除了静态变量和静态方法之外,static也用于静态块,多用于初始化操作:
public calss PreCache{
static{
//执行相关操作
}
}
此外static也多用于修饰内部类,此时称之为静态内部类.
最后一种用法就是静态导包,即 import static .import static是在JDK 1.5之后引入的新特性,可以用来指
定导入某个类中的静态资源,并且不需要使用类名,可以直接使用资源名,比如:
import static java.lang.Math.*;
public class Test{
public static void main(String[] args){
//System.out.println(Math.sin(20));传统做法
System.out.println(sin(20));
}
}

## 16. static和final区别

![image](https://user-images.githubusercontent.com/6525034/141612545-a1f97853-9ff0-416a-90e5-f76d9ae56d97.png)

## 17. 为什么有些java类要实现Serializable接口
为了网络进行传输或者持久化
什么是序列化
将对象的状态信息转换为可以存储或传输的形式的过程
除了实现Serializable接口还有什么序列化方式
Json序列化
FastJson序列化
ProtoBuff序列化

## 18. 什么是java序列化，如何实现java序列化？或者请解释Serializable接口的作用。
我们有时候将一个java对象变成字节流的形式传出去或者从一个字节流中恢复成一个java对象，例如，
要将java对象存储到硬盘或者传送给网络上的其他计算机，这个过程我们可以自己写代码去把一个java
对象变成某个格式的字节流再传输。
但是，jre本身就提供了这种支持，我们可以调用 OutputStream 的 writeObject 方法来做，如果要让
java帮我们做，要被传输的对象必须实现 serializable 接口，这样，javac编译时就会进行特殊处理，
编译的类才可以被 writeObject 方法操作，这就是所谓的序列化。需要被序列化的类必须实现
Serializable 接口，该接口是一个mini接口，其中没有需要实现方法，implements Serializable只是
为了标注该对象是可被序列化的。
例如，在web开发中，如果对象被保存在了Session中，tomcat在重启时要把Session对象序列化到硬
盘，这个对象就必须实现Serializable接口。如果对象要经过分布式系统进行网络传输，被传输的对象就
必须实现Serializable接口。

## 19. 什么是内部类？#内部类的作用
内部类的定义
将一个类定义在另一个类里面或者一个方法里面，这样的类称为内部类。
内部类的作用：
1、成员内部类 成员内部类可以无条件访问外部类的所有成员属性和成员方法（包括private成员和静态
成员）。 当成员内部类拥有和外部类同名的成员变量或者方法时，会发生隐藏现象，即默认情况下访问
的是成员内部类的成员。
2、局部内部类 局部内部类是定义在一个方法或者一个作用域里面的类，它和成员内部类的区别在于局
部内部类的访问仅限于方法内或者该作用域内。
3、匿名内部类 匿名内部类就是没有名字的内部类
4、静态内部类 指被声明为static的内部类，他可以不依赖内部类而实例，而通常的内部类需要实例化外
部类，从而实例化。静态内部类不可以有与外部类有相同的类名。不能访问外部类的普通成员变量，但
是可以访问静态成员变量和静态方法（包括私有类型） 一个 静态内部类去掉static 就是成员内部类，他
可以自由的引用外部类的属性和方法，无论是静态还是非静态。但是不可以有静态属性和方法
## 20. Excption与Error包结构

Java可抛出(Throwable)的结构分为三种类型：被检查的异常(CheckedException)，运行时异常
(RuntimeException)，错误(Error)。
1、运行时异常
定义：RuntimeException及其子类都被称为运行时异常。
特点：Java编译器不会检查它。也就是说，当程序中可能出现这类异常时，倘若既"没有通过throws声明
抛出它"，也"没有用try-catch语句捕获它"，还是会编译通过。例如，除数为零时产生的
ArithmeticException异常，数组越界时产生的IndexOutOfBoundsException异常，fail-fast机制产生的
ConcurrentModificationException异常（java.util包下面的所有的集合类都是快速失败的，“快速失败”
也就是fail-fast，它是Java集合的一种错误检测机制。当多个线程对集合进行结构上的改变的操作时，有
可能会产生fail-fast机制。记住是有可能，而不是一定。例如：假设存在两个线程（线程1、线程2），线
程1通过Iterator在遍历集合A中的元素，在某个时候线程2修改了集合A的结构（是结构上面的修改，而
不是简单的修改集合元素的内容），那么这个时候程序就会抛出 ConcurrentModificationException 异
常，从而产生fail-fast机制，这个错叫并发修改异常。Fail-safe，java.util.concurrent包下面的所有的类
都是安全失败的，在遍历过程中，如果已经遍历的数组上的内容变化了，迭代器不会抛出
ConcurrentModificationException异常。如果未遍历的数组上的内容发生了变化，则有可能反映到迭
代过程中。这就是ConcurrentHashMap迭代器弱一致的表现。ConcurrentHashMap的弱一致性主要是
为了提升效率，是一致性与效率之间的一种权衡。要成为强一致性，就得到处使用锁，甚至是全局锁，
这就与Hashtable和同步的HashMap一样了。）等，都属于运行时异常。
常见的五种运行时异常：
ClassCastException （类转换异常）
IndexOutOfBoundsException （数组越界）
NullPointerException （空指针异常）
ArrayStoreException （数据存储异常，操作数组是类型不一致）
BufferOverflowException
2、被检查异常
定义：Exception类本身，以及Exception的子类中除了"运行时异常"之外的其它子类都属于被检查异
常。
特点 ： Java编译器会检查它。 此类异常，要么通过throws进行声明抛出，要么通过try-catch进行捕获
处理，否则不能通过编译。例如，CloneNotSupportedException就属于被检查异常。
当通过clone()接口去克隆一个对象，而该对象对应的类没有实现Cloneable接口，就会抛出
CloneNotSupportedException异常。被检查异常通常都是可以恢复的。 如：
IOException
FileNotFoundException
SQLException
被检查的异常适用于那些不是因程序引起的错误情况，比如：读取文件时文件不存在引发的
FileNotFoundException 。然而，不被检查的异常通常都是由于糟糕的编程引起的，比如：在对象引
用时没有确保对象非空而引起的 NullPointerException 。


3、错误
定义 : Error类及其子类。
特点 : 和运行时异常一样，编译器也不会对错误进行检查。
当资源不足、约束失败、或是其它程序无法继续运行的条件发生时，就产生错误。程序本身无法修复这
些错误的。例如，VirtualMachineError就属于错误。出现这种错误会导致程序终止运行。
OutOfMemoryError、ThreadDeath。


## 21. try {}里有一个return语句，那么紧跟在这个try后的finally{}里的code会不会被执行，什么时候被执行，在return前还是后?

我们知道finally{}中的语句是一定会执行的，那么这个可能正常脱口而出就是return之前，return之后可
能就出了这个方法了，鬼知道跑哪里去了，但更准确的应该是在return中间执行，请看下面程序代码的
运行结果：

public classTest {
public static void main(String[]args) {
System.out.println(newTest().test());;
}
static int test()
{
intx = 1;
try
{
微信搜索公众号：Java专栏，获取最新面试手册
执行结果如下：
运行结果是1，为什么呢？主函数调用子函数并得到结果的过程，好比主函数准备一个空罐子，当子函数
要返回结果时，先把结果放在罐子里，然后再将程序逻辑返回到主函数。所谓返回，就是子函数说，我
不运行了，你主函数继续运行吧，这没什么结果可言，结果是在说这话之前放进罐子里的。
22. 运行时异常与一般异常有何异同？
异常表示程序运行过程中可能出现的非正常状态，运行时异常表示虚拟机的通常操作中可能遇到的异
常，是一种常见运行错误。java编译器要求方法必须声明抛出可能发生的非运行时异常，但是并不要求
必须声明抛出未被捕获的运行时异常。
23. error和exception有什么区别?
error 表示恢复不是不可能但很困难的情况下的一种严重问题。比如说内存溢出。不可能指望程序能处
理这样的情况。exception表示一种设计或实现问题。也就是说，它表示如果程序运行正常，从不会发生
的情况。
24. 简单说说Java中的异常处理机制的简单原理和应用。
异常是指java程序运行时（非编译）所发生的非正常情况或错误，与现实生活中的事件很相似，现实生
活中的事件可以包含事件发生的时间、地点、人物、情节等信息，可以用一个对象来表示，Java使用面
向对象的方式来处理异常，它把程序中发生的每个异常也都分别封装到一个对象来表示的，该对象中包
含有异常的信息。
 Java对异常进行了分类，不同类型的异常分别用不同的Java类表示，所有异常的根类为
java.lang.Throwable。
Throwable下面又派生了两个子类：
Error和Exception，Error表示应用程序本身无法克服和恢复的一种严重问题，程序只有奔溃了，
例如，说内存溢出和线程死锁等系统问题。
Exception表示程序还能够克服和恢复的问题，其中又分为系统异常和普通异常：
系统异常是软件本身缺陷所导致的问题，也就是软件开发人员考虑不周所导致的问题，软件使用者无法
克服和恢复这种问题，但在这种问题下还可以让软件系统继续运行或者让软件挂掉，例如，数组脚本越
界（ArrayIndexOutOfBoundsException），空指针异常（NullPointerException）、类转换异常
（ClassCastException）；
return x;
}
finally
{
++x;
}
}
}
执行结果如下：
1
运行结果是1，为什么呢？主函数调用子函数并得到结果的过程，好比主函数准备一个空罐子，当子函数
要返回结果时，先把结果放在罐子里，然后再将程序逻辑返回到主函数。所谓返回，就是子函数说，我
不运行了，你主函数继续运行吧，这没什么结果可言，结果是在说这话之前放进罐子里的。

## 22. 运行时异常与一般异常有何异同？

异常表示程序运行过程中可能出现的非正常状态，运行时异常表示虚拟机的通常操作中可能遇到的异
常，是一种常见运行错误。java编译器要求方法必须声明抛出可能发生的非运行时异常，但是并不要求
必须声明抛出未被捕获的运行时异常。

## 23. error和exception有什么区别?
error 表示恢复不是不可能但很困难的情况下的一种严重问题。比如说内存溢出。不可能指望程序能处
理这样的情况。exception表示一种设计或实现问题。也就是说，它表示如果程序运行正常，从不会发生
的情况。

## 24. 简单说说Java中的异常处理机制的简单原理和应用
异常是指java程序运行时（非编译）所发生的非正常情况或错误，与现实生活中的事件很相似，现实生
活中的事件可以包含事件发生的时间、地点、人物、情节等信息，可以用一个对象来表示，Java使用面
向对象的方式来处理异常，它把程序中发生的每个异常也都分别封装到一个对象来表示的，该对象中包
含有异常的信息。
 Java对异常进行了分类，不同类型的异常分别用不同的Java类表示，所有异常的根类为
java.lang.Throwable。
Throwable下面又派生了两个子类：
Error和Exception，Error表示应用程序本身无法克服和恢复的一种严重问题，程序只有奔溃了，
例如，说内存溢出和线程死锁等系统问题。
Exception表示程序还能够克服和恢复的问题，其中又分为系统异常和普通异常：
系统异常是软件本身缺陷所导致的问题，也就是软件开发人员考虑不周所导致的问题，软件使用者无法
克服和恢复这种问题，但在这种问题下还可以让软件系统继续运行或者让软件挂掉，例如，数组脚本越
界（ArrayIndexOutOfBoundsException），空指针异常（NullPointerException）、类转换异常
（ClassCastException）；
普通异常是运行环境的变化或异常所导致的问题，是用户能够克服的问题，例如，网络断线，硬盘空间
不够，发生这样的异常后，程序不应该死掉。
java为系统异常和普通异常提供了不同的解决方案，编译器强制普通异常必须try..catch处理或用throws
声明继续抛给上层调用方法处理，所以普通异常也称为checked异常，而系统异常可以处理也可以不处
理，所以，编译器不强制用try..catch处理或用throws声明，所以系统异常也称为unchecked异常。


## 25. == 和 equals 的区别是什么？

== 对于基本类型来说是值比较，对于引用类型来说是比较的是引用；而 equals 默认情况下是引用比
较，只是很多类重新了 equals 方法，比如 String、Integer 等把它变成了值比较，所以一般情况下
equals 比较的是值是否相等。


## 26. Hashcode的作用

java的集合有两类，一类是List，还有一类是Set。前者有序可重复，后者无序不重复。当我们在set中插
入的时候怎么判断是否已经存在该元素呢，可以通过equals方法。但是如果元素太多，用这样的方法就
会比较慢。
于是有人发明了哈希算法来提高集合中查找元素的效率。 这种方式将集合分成若干个存储区域，每个对
象可以计算出一个哈希码，可以将哈希码分组，每组分别对应某个存储区域，根据一个对象的哈希码就
可以确定该对象应该存储的那个区域。
hashCode方法可以这样理解：它返回的就是根据对象的内存地址换算出的一个值。这样一来，当集合
要添加新的元素时，先调用这个元素的hashCode方法，就一下子能定位到它应该放置的物理位置上。
如果这个位置上没有元素，它就可以直接存储在这个位置上，不用再进行任何比较了；如果这个位置上
已经有元素了，就调用它的equals方法与新元素进行比较，相同的话就不存了，不相同就散列其它的地
址。这样一来实际调用equals方法的次数就大大降低了，几乎只需要一两次。

## 27. 两个对象的 hashCode() 相同， 那么 equals() 也一定为 true吗？
不对，两个对象的 hashCode() 相同，equals() 不一定 true。
代码示例：

String str1 = "keep";
String str2 = "brother";
System. out. println(String. format("str1：%d | str2：%d", str1.
hashCode(),str2. hashCode()));
System. out. println(str1. equals(str2));

执行结果:

str1：1179395 | str2：1179395
false

代码解读：很显然“keep”和“brother”的 hashCode() 相同，然而 equals() 则为 false，因为在散列表
中，hashCode() 相等即两个键值对的哈希值相等，然而哈希值相等，并不一定能得出键值对相等。


## 28. 泛型常用特点

“泛型” 意味着编写的代码可以被不同类型的对象所重用。
“泛型”，顾名思义，“泛指的类型”。我们提供了泛指的概念，但具体执行的时候却可以有具体的规则来约
束，比如我们用的非常多的ArrayList就是个泛型类，ArrayList作为集合可以存放各种元素，如Integer,
String，自定义的各种类型等，但在我们使用的时候通过具体的规则来约束，如我们可以约束集合中只
存放Integer类型的元素，如

List<Integer> iniData = new ArrayList<>()

使用泛型的好处？
以集合来举例，使用泛型的好处是我们不必因为添加元素类型的不同而定义不同类型的集合，如整型集
合类，浮点型集合类，字符串集合类，我们可以定义一个集合来存放整型、浮点型，字符串型数据，而
这并不是最重要的，因为我们只要把底层存储设置了Object即可，添加的数据全部都可向上转型为
Object。 更重要的是我们可以通过规则按照自己的想法控制存储的数据类型。
#为什么不能通过new List（）方式创建对象 在java.util里面List是一个接口，所以不能直接初始化，所以会编译错误
你可以List l =new ArrayList();这样是可以的，因为 ArrayList是实现List接口的
或者List l = new LinkedList(); LinkedList同样实现了List接口 我们一般使用List都是new ArrayList();

## 29. 面向对象的特征

面向对象的编程语言有封装、继承 、抽象、多态等4个主要的特征。
1. 封装： 把描述一个对象的属性和行为的代码封装在一个模块中，也就是一个类中，属性用变量定
义，行为用方法进行定义，方法可以直接访问同一个对象中的属性。
2. 抽象： 把现实生活中的对象抽象为类。分为过程抽象和数据抽象
数据抽象 -->鸟有翅膀,羽毛等(类的属性)
过程抽象 -->鸟会飞,会叫(类的方法)
1. 继承：子类继承父类的特征和行为。子类可以有父类的方法，属性（非private）。子类也可以对父
类进行扩展，也可以重写父类的方法。缺点就是提高代码之间的耦合性。
2. 多态： 多态是指程序中定义的引用变量所指向的具体类型和通过该引用变量发出的方法调用在编程
时并不确定，而是在程序运行期间才确定(比如：向上转型，只有运行才能确定其对象属性)。方法
覆盖和重载体现了多态性。
封装即隐藏对象的属性和实现细节，仅对外提供公共访问方式，保证了模块具有较好的独立性，使得程序维护修改较为容易。继承提高了代码的复用性，多态提高代码的扩展性和可维护性。三者共同达到了一个目的：使得对应用程序的修改带来的影响更加局部化，程序更加健壮，而且易维护、更新和升级。  
  
## 30. Java多态的理解

1. 多态是继封装、继承之后，面向对象的第三大特性。
2. 多态现实意义理解：
现实事物经常会体现出多种形态，如学生，学生是人的一种，则一个具体的同学张三既是学生也是
人，即出现两种形态。
Java作为面向对象的语言，同样可以描述一个事物的多种形态。如Student类继承了Person类，一
个Student的对象便既是Student，又是Person。
1. 多态体现为父类引用变量可以指向子类对象。
2. 前提条件：必须有子父类关系。
注意：在使用多态后的父类引用变量调用方法时，会调用子类重写后的方法。
1. 多态的定义与使用格式
定义格式：父类类型 变量名=new 子类类型();

## 31. 重载和重写的区别 
  
 重写(Override)
从字面上看，重写就是 重新写一遍的意思。其实就是在子类中把父类本身有的方法重新写一遍。子类继
承了父类原有的方法，但有时子类并不想原封不动的继承父类中的某个方法，所以在方法名，参数列
表，返回类型(除过子类中方法的返回值是父类中方法返回值的子类时)都相同的情况下， 对方法体进行
修改或重写，这就是重写。但要注意子类函数的访问修饰权限不能少于父类的。
  
public class Father {
public static void main(String[] args) {
// TODO Auto-generated method stub
Son s = new Son();
s.sayHello();
}
public void sayHello() {
System.out.println("Hello");
}
}
class Son extends Father{
@Override
public void sayHello() {
// TODO Auto-generated method stub
System.out.println("hello by ");
}
}

 重写 总结：
1.发生在父类与子类之间
2.方法名，参数列表，返回类型（除过子类中方法的返回类型是父类中返回类型的子类）必须相同
3.访问修饰符的限制一定要大于被重写方法的访问修饰符（public>protected>default>private)
4.重写方法一定不能抛出新的检查异常或者比被重写方法申明更加宽泛的检查型异常
  
重载（Overload）
在一个类中，同名的方法如果有不同的参数列表（参数类型不同、参数个数不同甚至是参数顺序不同）
则视为重载。同时，重载对返回类型没有要求，可以相同也可以不同，但不能通过返回类型是否相同来
判断重载。

  public class Father {
public static void main(String[] args) {
// TODO Auto-generated method stub
Father s = new Father();
s.sayHello();
s.sayHello("wintershii");
}
public void sayHello() {
System.out.println("Hello");
}
public void sayHello(String name) {
System.out.println("Hello" + " " + name);
}
}
  
重载 总结：
1.重载Overload是一个类中多态性的一种表现
2.重载要求同名方法的参数列表不同(参数类型，参数个数甚至是参数顺序)
3.重载的时候，返回值类型可以相同也可以不相同。无法以返回型别作为重载函数的区分标准
  
# 33. Java创建对象有几种方式？
java中提供了以下四种创建对象的方式:
new创建新对象
通过反射机制
采用clone机制
通过序列化机制

# 34. ConcurrentModificationException异常出现的原因
public class Test {
public static void main(String[] args) {
ArrayList<Integer> list = new ArrayList<Integer>();
list.add(2);
Iterator<Integer> iterator = list.iterator();
while(iterator.hasNext()){
Integer integer = iterator.next();
if(integer==2)
list.remove(integer);
}
}
}
执行上段代码是有问题的，会抛出 ConcurrentModificationException 异常。
原因：调用 list.remove() 方法导致 modCount 和 expectedModCount 的值不一致。
final void checkForComodification() {
if (modCount != expectedModCount)
throw new ConcurrentModificationException();
}
解决办法：在迭代器中如果要删除元素的话，需要调用 Iterator 类的 remove 方法  
 
## 35. HashMap和HashTable、ConcurrentHashMap区别？
相同点:
1. HashMap和Hashtable都实现了Map接口
2. 都可以存储key-value数据
不同点：
1. HashMap可以把null作为key或value，HashTable不可以
2. HashMap线程不安全，效率高。HashTable线程安全，效率低。
3. HashMap的迭代器(Iterator)是fail-fast迭代器，而Hashtable的enumerator迭代器不是fail-fast
的。
什么是fail-fast?
就是最快的时间能把错误抛出而不是让程序执行。

## 36. 如何保证线程安全又效率高？
Java 5提供了ConcurrentHashMap，它是HashTable的替代，比HashTable的扩展性更好。
ConcurrentHashMap将整个Map分为N个segment(类似HashTable)，可以提供相同的线程安全，但是
效率提升N倍，默认N为16。  

## 37. 我们能否让HashMap同步？
HashMap可以通过下面的语句进行同步：
Map m = Collections.synchronizeMap(hashMap);
  
## 38. Java 中 IO 流分为几种？
 按功能来分：输入流（input）、输出流（output）。
按类型来分：字节流和字符流。
字节流和字符流的区别是：字节流按 8 位传输以字节为单位输入输出数据，字符流按 16 位传输以字符
为单位输入输出数据。
 
## 39. BIO、NIO、AIO 有什么区别？
  BIO：Block IO 同步阻塞式 IO，就是我们平常使用的传统 IO，它的特点是模式简单使用方便，并
发处理能力低。
NIO：Non IO 同步非阻塞 IO，是传统 IO 的升级，客户端和服务器端通过 Channel（通道）通
讯，实现了多路复用。
AIO：Asynchronous IO 是 NIO 的升级，也叫 NIO2，实现了异步非堵塞 IO ，异步 IO 的操作基于
事件和回调机制。

## 40. Files的常用方法都有哪些？
 Files. exists()：检测文件路径是否存在。
Files. createFile()：创建文件。
Files. createDirectory()：创建文件夹。
Files. delete()：删除一个文件或目录。
Files. copy()：复制文件。
Files. move()：移动文件。
Files. size()：查看文件个数。
Files. read()：读取文件。
Files. write()：写入文件。
 
## 41. Java反射的作用于原理
  1、定义：
反射机制是在运行时，对于任意一个类，都能够知道这个类的所有属性和方法；对于任意个对象，都能
够调用它的任意一个方法。在java中，只要给定类的名字，就可以通过反射机制来获得类的所有信息。
这种动态获取的信息以及动态调用对象的方法的功能称为Java语言的反射机制。
2、哪里会用到反射机制？
jdbc就是典型的反射
Class.forName('com.mysql.jdbc.Driver.class');//加载MySQL的驱动类
这就是反射。如hibernate，struts等框架使用反射实现的。

## 42. 反射的实现方式
第一步：获取Class对象，有4种方法： 1）Class.forName(“类的路径”)； 2）类名.class 3）对象
名.getClass() 4）基本类型的包装类，可以调用包装类的Type属性来获得该包装类的Class对象

## 43. 实现Java反射的类：
1）Class：表示正在运行的Java应用程序中的类和接口 注意： 所有获取对象的信息都需要Class类来实
现。 2）Field：提供有关类和接口的属性信息，以及对它的动态访问权限。 3）Constructor：提供关于
类的单个构造方法的信息以及它的访问权限 4）Method：提供类或接口中某个方法的信息
  
##44. 反射机制的优缺点：
优点：
1、能够运行时动态获取类的实例，提高灵活性；
2、与动态编译结合
缺点：
1、使用反射性能较低，需要解析字节码，将内存中的对象进行解析。
解决方案：
1、通过setAccessible(true)关闭JDK的安全检查来提升反射速度；
2、多次创建一个类的实例时，有缓存会快很多
3、ReflectASM工具类，通过字节码生成的方式加快反射速度
2、相对不安全，破坏了封装性（因为通过反射可以获得私有方法和属性）

## 45. Java 中 IO 流分为几种?
  
按照流的流向分，可以分为输入流和输出流；
按照操作单元划分，可以划分为字节流和字符流；
按照流的角色划分为节点流和处理流。
Java Io 流共涉及 40 多个类，这些类看上去很杂乱，但实际上很有规则，而且彼此之间存在非常紧密的
联系， Java I0 流的 40 多个类都是从如下 4 个抽象类基类中派生出来的。
InputStream/Reader: 所有的输入流的基类，前者是字节输入流，后者是字符输入流。
OutputStream/Writer: 所有输出流的基类，前者是字节输出流，后者是字符输出流。  
  
![image](https://user-images.githubusercontent.com/6525034/141645376-b15adf21-6084-4e4a-b1a6-1344c26d804e.png)
  
  
  
  
  
  
  
  
  
  
  
  
  
  
