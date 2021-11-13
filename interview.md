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

