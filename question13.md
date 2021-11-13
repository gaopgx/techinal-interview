java内部类有什么作用？

作者：二境志
链接：https://www.zhihu.com/question/26954130/answer/708467570
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

非常感谢大家的意见，我已经在原来对内部类基本讲解的基础上，增加了内部类的一些使用场景，帮助大家对于内部类可以解决什么样的问题有一个简单的概念。或许能给一些初学者帮助，更深入的学习也是需要自己去琢磨，去查阅，去学习，加油！内部类(一) 概述把类定义在另一个类的内部，该类就被称为内部类。举例：把类Inner定义在类Outer中，类Inner就被称为内部类。  class Outer {
      class Inner {
      }
  }(二) 内部类的访问规则​	A:可以直接访问外部类的成员，包括私有​	B:外部类要想访问内部类成员，必须创建对象(三) 内部类的分类​	A：成员内部类​	B：局部内部类​	C：静态内部类​	D：匿名内部类(1) 成员内部类成员内部类——就是位于外部类成员位置的类特点：可以使用外部类中所有的成员变量和成员方法（包括private的）A：格式：  class Outer {
      private int age = 20;
      //成员位置
      class Inner {
          public void show() {
              System.out.println(age);
          }
      }
  }
  ​
  class Test {
      public static void main(String[] ages) {
          //成员内部类是非静态的演示
          Outer.Inner oi = new Outer().new Inner();
          oi.show();
      }
  }B：创建对象时：  //成员内部类不是静态的：
  外部类名.内部类名 对象名 = new 外部类名.new 内部类名();
  ​
  //成员内部类是静态的：
  外部类名.内部类名 对象名 = new 外部类名.内部类名();    C：成员内部类常见修饰符：A：private如果我们的内部类不想轻易被任何人访问，可以选择使用private修饰内部类，这样我们就无法通过创建对象的方法来访问，想要访问只需要在外部类中定义一个public修饰的方法，间接调用。这样做的好处就是，我们可以在这个public方法中增加一些判断语句，起到数据安全的作用。  class Outer {
      private class Inner {
          public void show() {
              System.out.println(“密码备份文件”);
          }
      }
      
      public void method() {
          if(你是管理员){
              Inner i = new Inner();
              i.show();
          }else {
              System.out.println(“你没有权限访问”);
          }
      }
  }下面我们给出一个更加规范的写法  class Outer {
      private class Inner {
          public void show() {
              System.out.println(“密码备份文件”);
          }
      }
      //使用getXxx()获取成员内部类，可以增加校验语句（文中省略）
      public Inner getInner() {
          return new Inner();
      }
      
      public static void main(String[] args) {
          Outer outer = new Outer();
          Outer.Inner inner = outer.getInner();
          inner.show();
      }
  }B：static这种被 static 所修饰的内部类，按位置分，属于成员内部类，但也可以称作静态内部类，也常叫做嵌套内部类。具体内容我们在下面详细讲解。D：成员内部类经典题(填空)请在三个println 后括号中填空使得输出25,20,18  class Outer {
      public int age = 18;    
      class Inner {
          public int age = 20;    
          public viod showAge() {
              int age  = 25;
              System.out.println(age);//空1
              System.out.println(this.age);//空2
              System.out.println(Outer.this.age);//空3
          }
      }
  } (2) 局部内部类局部内部类——就是定义在一个方法或者一个作用域里面的类特点：主要是作用域发生了变化，只能在自身所在方法和属性中被使用A 格式：  class Outer {
      public void method(){
          class Inner {
          }
      }
  }B：访问时：  //在局部位置，可以创建内部类对象，通过对象调用和内部类方法
  class Outer {
      private int age = 20;
      public void method() {
          final int age2 = 30;
          class Inner {
              public void show() {
                  System.out.println(age);
                  //从内部类中访问方法内变量age2，需要将变量声明为最终类型。
                  System.out.println(age2);
              }
          }
          
          Inner i = new Inner();
          i.show();
      }
  }C: 为什么局部内部类访问局部变量必须加final修饰呢？因为局部变量是随着方法的调用而调用，使用完毕就消失，而堆内存的数据并不会立即消失。所以，堆内存还是用该变量，而该变量已经没有了。为了让该值还存在，就加final修饰。原因是，当我们使用final修饰变量后，堆内存直接存储的是值，而不是变量名。（即上例 age2 的位置存储着常量30 而不是 age2 这个变量名）(3) 静态内部类我们所知道static是不能用来修饰类的,但是成员内部类可以看做外部类中的一个成员,所以可以用static修饰,这种用static修饰的内部类我们称作静态内部类,也称作嵌套内部类.特点：不能使用外部类的非static成员变量和成员方法解释：非静态内部类编译后会默认的保存一个指向外部类的引用，而静态类却没有。简单理解：即使没有外部类对象，也可以创建静态内部类对象，而外部类的非static成员必须依赖于对象的调用，静态成员则可以直接使用类调用，不必依赖于外部类的对象，所以静态内部类只能访问静态的外部属性和方法。  class Outter {
      int age = 10;
      static age2 = 20;
      public Outter() {        
      }
       
      static class Inner {
          public method() {
              System.out.println(age);//错误
              System.out.println(age2);//正确
          }
      }
  }
  ​
  public class Test {
      public static void main(String[] args)  {
          Outter.Inner inner = new Outter.Inner();
          inner.method();
      }
  }(4) 匿名内部类一个没有名字的类，是内部类的简化写法A 格式：  new 类名或者接口名() {
      重写方法();
  }本质：其实是继承该类或者实现接口的子类匿名对象这也就是下例中，可以直接使用 new Inner() {}.show(); 的原因 == 子类对象.show();  interface Inner {
      public abstract void show();
  }
  ​
  class Outer {
      public void method(){
          new Inner() {
              public void show() {
                  System.out.println("HelloWorld");
              }
          }.show();
      }
  }
  ​
  class Test {
      public static void main(String[] args)  {
          Outer o = new Outer();
          o.method();
      }
  }    如果匿名内部类中有多个方法又该如何调用呢？  Inter i = new Inner() {  //多态，因为new Inner(){}代表的是接口的子类对象
      public void show() {
      System.out.println("HelloWorld");
      }
  };B：匿名内部类在开发中的使用​我们在开发的时候，会看到抽象类，或者接口作为参数。而这个时候，实际需要的是一个子类对象。如果该方法仅仅调用一次，我们就可以使用匿名内部类的格式简化。-----------------------------------------------------------------------------2019-8-17更新补充使用内部类的原因(一) 封装性作为一个类的编写者，我们很显然需要对这个类的使用访问者的访问权限做出一定的限制，我们需要将一些我们不愿意让别人看到的操作隐藏起来，如果我们的内部类不想轻易被任何人访问，可以选择使用private修饰内部类，这样我们就无法通过创建对象的方法来访问，想要访问只需要在外部类中定义一个public修饰的方法，间接调用。  public interface Demo {
      void show();
  }
  
  class Outer {
      private class test implements Demo {
          public void show() {
              System.out.println("密码备份文件");
          }
      }
      
      public Demo getInner() {
          return new test();
      }
      
  }我们来看其测试      public static void main(String[] args) {
          Outer outer = new Outer();
          Demo d = outer.getInner();
          i.show();
      }
  ​
  //运行结果
  密码备份文件这样做的好处之一就是，我们可以在这个public方法中增加一些判断语句，起到数据安全的作用。其次呢，我们的对外可见的只是getInner()这个方法，它返回了一个Demo接口的一个实例，而我们真正的内部类的名称就被隐藏起来了(二) 实现多继承 ※我们之前的学习知道，java是不可以实现多继承的，一次只能继承一个类，我们学习接口的时候，有提到可以用接口来实现多继承的效果，即一个接口有多个实现，但是这里也是有一点弊端的，那就是，一旦实现一个接口就必须实现里面的所有方法，有时候就会出现一些累赘，但是使用内部类可以很好的解决这些问题  public class Demo1 {
      public String name() {
          return "BWH_Steven";
      }
  }
  
  public class Demo2 {
      public String email() {
          return "xxx.@163.com";
      }
  }
  
  public class MyDemo {
  ​
      private class test1 extends Demo1 {
          public String name() {
              return super.name();
          }
      }
  ​
      private class test2 extends Demo2  {
          public String email() {
              return super.email();
          }
      }
  ​
      public String name() {
          return new test1().name();
      }
  ​
      public String email() {
          return new test2().email();
      }
  ​
      public static void main(String args[]) {
          MyDemo md = new MyDemo();
          System.out.println("我的姓名:" + md.name());
          System.out.println("我的邮箱:" + md.email());
      }
  }我们编写了两个待继承的类Demo1和Demo2，在MyDemo类中书写了两个内部类，test1和test2 两者分别继承了Demo1和Demo2类，这样MyDemo中就间接的实现了多继承(三) 用匿名内部类实现回调功能我们用通俗讲解就是说在Java中，通常就是编写一个接口，然后你来实现这个接口，然后把这个接口的一个对象作以参数的形式传到另一个程序方法中， 然后通过接口调用你的方法，匿名内部类就可以很好的展现了这一种回调功能  public interface Demo {
      void demoMethod();
  }
  
  public class MyDemo{
      public test(Demo demo){
          System.out.println("test method");
      }
      
      public static void main(String[] args) {
          MyDemo md = new MyDemo();
          //这里我们使用匿名内部类的方式将接口对象作为参数传递到test方法中去了
          md.test(new Demo){
              public void demoMethod(){
                  System.out.println("具体实现接口")
              }
          }
      }
  }(四) 解决继承及实现接口出现同名方法的问题编写一个接口 Demo  public interface Demo {
      void test();
  }编写一个类 MyDemo  public class MyDemo {
  ​
      public void test() {
          System.out.println("父类的test方法");
      }
      
  }编写一个测试类  public class DemoTest extends MyDemo implements Demo {
      public void test() {
      }
  }这样的话我就有点懵了，这样如何区分这个方法是接口的还是继承的，所以我们使用内部类解决这个问题  public class DemoTest extends MyDemo {
  ​
  ​
      private class inner implements Demo {
          public void test() {
              System.out.println("接口的test方法");
          }
      }
      
      public Demo getIn() {
          return new inner();
      }
      
      
      public static void main(String[] args) {
          //调用接口而来的test()方法
          DemoTest dt = new DemoTest();
          Demo d = dt.getIn();
          d.test();
          
          //调用继承而来的test()方法
          dt.test();
      }
  }
  ​
  //运行结果
  接口的test方法
  父类的test方法
