为什么String存储在字符串常量池中？

解析

所有的字符串字面量都被存储在一个称为字符串常量池（String Constant Pool：SCP）的单独内存区域中。并且 String 的不可变性使得字符串常量池成为可能。

问：为什么 Java 需要一个单独的字符串常量池来存储字符串？为什么字符串不像其它对象那样存储在堆内存中？

引：通常，在一个 Java 业务应用程序会创建并处理成千上万个字符串对象（实际开发中几乎没有不使用 String 的程序），这些字符串对象中有许多具有相同的值或者是中间操作字符而非最终结果。如果我们将所有这些字符串对象存储在堆内存中，仅仅是存储这些字符串对象就需要占用大量的堆内存。当回收不再使用的字符串对象时也会导致垃圾收集器频繁地运行，这将大大降低应用程序的性能。

答：为了避免 JVM 首先创建大量的字符串对象，然后再进行垃圾回收。 JVM 将所有字符串字面量存储在称为字符串常量池的单独内存区域中，并重用该高速缓存池中的对象。

升华：当我们创建字符串字面量时，JVM 就会首先查看 SCP 中是否已经存在该字符串字面量，如果存在，则新的引用变量指向 SCP 中的同一个字符串字面量，这个过程称为 String Interning。

String 对象的创建

1. 创建字符串字面量，例如：String str = "zhangsan"。默认情况下，所有字符串字面量都会经过 String Interning 放入到 SCP 中。

2. 使用构造函数创建字符串对象：如果我们使用构造函数创建 String 对象，例如 String str = new String("zhangsan")。该对象是在堆内存中创建的，而不是在 SCP 中创建的。这就是为什么不将使用构造函数创建 String 对象视为最佳实践的原因。 我们可以通过用构造函数创建的 String 对象来调用它的 intern() 方法来手动要求对象指向 SCP 而不是堆内存。

String 的不可变性使得字符串常量池成为可能

String a = "Naresh";
String b = "Naresh";
String c = "Naresh";
对于上述代码，仅在 SCP 中创建了一个值为 Naresh 的字符串对象，并且所有的引用变量a、b、c 都指向同一对象。 此时我们进行如下更改：

a.replace("a"，"");
我们知道在 Java 中上述更改的结果为：引用变量 a 的值为 Nresh，而引用变量 b、c 的值为 Naresh。但是，不是说引用变量 a、b、c 都指向同一个 String 对象吗？因此如果我们对引用变量 a 进行更改，那么引用变量 b、c 应该也跟着改变啊。这正是因为 String 的不可变性。

由于 String 对象的不变性，字符串对象 Naresh 永远不会改变。当我们对引用变量 a 进行更改时，JVM 不会对字符串对象 Naresh 进行任何更改，而是创建一个的 String 对象把它分配给引用变量 a，再在这个新的 String 对象中进行更改。

因此，由于 String 的不可变性，才使得 字符串常量池成为可能。如果 String 是可变的，则缓存字符串对象并重新使用它们是不可能的，因为任何引用变量都会改变 String 对象的值并破坏其它引用该对象的引用变量。

 作者：JsutForFun https://www.bilibili.com/read/cv10202424 出处：bilibili