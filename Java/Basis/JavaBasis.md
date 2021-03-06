#### [面向对象和面向过程的区别](#a)
#### [Java 语言有哪些特点](#b)
#### [什么是JDK什么是JRE什么是JVM & 三者之间的联系和区别](#c)
#### [什么是字节码 & 采用字节码的最大好处是什么](#d)
#### [Java和C++的区别](#e)
#### [什么是Java程序的主类 & 应用程序和小程序的主类有何不同](#f)
#### [字符型常量和字符串常量的区别](#g)
#### [构造器Constructor是否可以被override](#h)
#### [重载和重写的区别](#i)
#### [Java面向对象编程三大特性：封装、继承、多态](#j)
#### [String、StringBuffer、StringBuilder区别是什么 & String为什么是不可变的](#k)
#### [自动装箱与拆箱](#l)
#### [在一个静态方法内调用一个非静态成员为什么是非法的](#m)
#### [在Java中定义一个不做事且没有参数的构造方法的作用](#n)
#### [import java和javax有什么区别](#o)
#### [接口和抽象类的区别是什么](#p)
#### [成员变量与局部变量的区别](#q)
#### [创建一个对象用什么运算符 & 对象实体与对象引用有什么区别](#r)
#### [什么是方法的返回值 & 返回值在类的方法里的作用是什么](#s)
#### [一个类的构造方法的作用是什么 & 若一个类没有申明构造方法，该程序能正确执行吗](#t)
#### [构造方法有哪些特性](#u)
#### [静态方法和实例方法的区别](#v)
#### [对象的相等和指向他们的引用相等，有什么区别](#w)
#### [在调用子类构造方法之前会先调用父类没有参数的构造方法，其目的是什么](#x)
#### [==与equals](#y)
#### [hashCode与equals](#z)
#### [为什么Java中只有值传递](#aa)
#### [简述线程、程序、进程的基本概念，以及它们之间的关系](#ab)
#### [线程有哪些基本状态 & 这些基本状态是怎么定义的](#ac)
#### [关于final关键字的一些总结](#ad)
#### [Java中的异常处理（异常类层次结构、Throwable类常用方法、异常处理总结）](#ae)
#### [java序列化中如果有些字段不想进行序列化，怎么办](#af)



## <span id="a">面向对象和面向过程的区别</span>
#### 面向对象
* 其模块单位是类：类是数据类型，对象是类的实例
* 将数据及对数据的操作行为放在一起，作为对象；再通过抽象找出同一类型对象，形成类
* 封装性、抽象性、继承性、多态性

#### 面向过程
* 是一种自顶向下的功能分解法
* 其程序单位是过程或函数
* 可复用性差

## <span id="b">Java 语言有哪些特点</span>
* 简单性
* 面向对象
* 平台无关性
* 可移植性
* 解释性
* 高性能
* 动态性
* 可靠性和安全性
* 多线程
* 分布式处理

## <span id="c">什么是JDK什么是JRE什么是JVM & 三者之间的联系和区别</span>
#### JDK
Java Development Kits <==> Java开发工具包
开发的核心
#### JRE
Java Runtime Environment <==> Java运行环境（运行时类库）
#### JVM
Java Virtual Machine <==> Java虚拟机
跨平台的核心
###### 联系
一层层的嵌套关系：JDK > JRE > JVM
JDK = JRE + JVM + 其它

## <span id="d">什么是字节码 & 采用字节码的最大好处是什么</span>
字节码 Bytecode（.class 文件）：是一种介于Java（用户语言）和机器语言之间的中间语言；是 Java代码部署的最小单元（二进制）

Java编译器将Java源程序编译为JVM字节码；通过Java解释器就可以运行程序

JVM是Java平台无关的基础

Java程序运行环境：
```
Java源程序（.java文件）
=> Java编译器 
=> Java Bytecode（.class文件）
=> Bytecode装载 
=> 字节码校验器 
=> Bytecode解释 
=> 系统执行平台
```
###### 好处
确保了Java的平台无关性；通过JVM保证数据类型的一致性

## <span id="e">Java和C++的区别</span>
Java去掉了C++语言的复杂性和二义性成分，更加安全和可移植，也更简单，文件尺寸小，不需要显式进行内存管理

Java中没有析构函数、指针、运算符重载
> 析构函数：用来释放对象占用的空间
> 特点：名字与类名相同、在前面加上“～”、无参数和返回值、一个类最多只有一个析构函数

> 运算符重载：运算符与类结合，产生新的含义

> 指针：指针 `type *var-name` 是一个变量，其值为另一个变量的地址，即内存位置的直接地址

## <span id="f">什么是Java程序的主类 & 应用程序和小程序的主类有何不同</span>
Java程序有四种基本类型：应用程序application、小应用程序applet、servlet、bean

main方法所在的类叫主类：`public static void main(String args[])`

小程序不能直接运行，必须嵌入在网页中

## <span id="g">字符型常量和字符串常量的区别</span>
#### 字符型常量
用单引号括起来的单个字符
#### 字符串常量
用双引号括起来的多个字符（可以是0个）
> Java中字符串是String类的对象

可以使用 `+` 把两个或更多的字符串常量连接在一起

## <span id="h">构造器Constructor是否可以被override</span>
* 构造器也叫构造方法
* 构造方法一般用于为类新建的对象分配内存空间和进行变量的初始化
* 构造方法只能在创建对象时用new命令调用
* 构造方法必须与其类名相同
* 构造方法没有返回类型，代表没有void
* 可以有参数，可以被重载
* 不能被重写

## <span id="i">重载和重写的区别</span>
#### 重载
* 重载是在一个类里面，方法名字相同，而参数必须不同；返回类型可以相同也可以不同
* 被重载的方法必须改变参数列表(参数个数、类型、顺序不一样)
* 方法能够在同一个类中或者在一个子类中被重载
#### 重写
* 子类对父类允许被访问的方法进行重新编写, 返回值和形参都不能改变
* 访问权限不能比父类中被重写的方法访问权限更低
* 父类的成员方法只能被它的子类重写：`super .父类同名方法(...)`
* 声明为final的方法不能被重写
* 声明为static的方法不能被重写，但是能够被再次声明
* 构造方法不能被重写

## <span id="j">Java面向对象编程三大特性：封装、继承、多态</span>
#### 封装
* 把对象的全部属性和全部操作结合在一起，形成一个不可分割的独立单位
* 尽可能隐蔽对象的全部细节，只保留有限的对外接口
* 提高程序的可复用性和可维护性；保护了私有数据
#### 继承
* 类只支持单继承，接口支持多继承
* 
``` java
[类的修饰符] class 子类名 extends 父类名 {
      成员变量定义;
      成员方法定义;
}
```
* 在创建子类对象时，必须先调用直接父类的构造方法，然后才调用子类本身的构造方法；finalize调用顺序与此相反
* 抽象类必须被继承，抽象方法必须被重写
#### 多态
* 在继承层次结构中，父类可以定义为抽象类或接口，通过在子类中实现父类中的抽象方法，从而实现对象的多态性

## <span id="k">String、StringBuffer、StringBuilder区别是什么 & String为什么是不可变的</span>
#### String类
* 在java.lang包中
* 值在创建后不能被更改
> * 原因：
>     * String类本身是final的，不可被继承
>     * String类内部通过private final char value[]实现，从而保证了引用的不可变和对外的不可见
>     * String内部通过良好的封装，不去改变value数组的值
> * 优势：
>     * 安全性
>     * 效率高
###### 常用方法
* `compareTo(String anotherString)`：按字典顺序比较两个字符串，如果此字符串的字典大小超过字符串参数，则值大于0 ==> `int`
* `concat(String str)`：将指定的字符串连接到该字符串的末尾 ==> `new String`
* `endsWith(String suffix)`：测试此字符串是否以指定的后缀结尾 ==> `boolean`
* `equals(Object anObject)`：将此字符串与指定对象进行比较 ==> `boolean`
* `String.format("hi,%s", "jas")`：返回格式化的字符串 `hi,jas`
* `a.hashCode()`：返回此字符串的哈希码 ==> `int`
* `String.join("-","java","is","cool")`：返回一个新的字符串 `java-is-cool`
* `length()` ==> `int`
* `replace(char oldChar, char newChar)` ==> `new String`
* `split(String regex)` ==> `String[]`
* `trim()`：返回一个字符串，其值为此字符串，并删除任何前导和尾随空格 ==> `new String`
* `charAt(int index)`：返回当前字符串的某一指定位置的字符 ==> `String`
* `toCharArray()`：将String对象转换为字符型数组 ==> `char[]`

#### StringBuffer、StringBuilder类
* 字符串内容可以变化
* 在java.lang包中
###### 常用方法
* `append()`
* `delete(int start, int end)`：删除从start为开始索引到end-1索引之间的字符串
* `insert()`
* `replace()`
* `reverse()`：颠倒StringBuffer对象的内容
* `length()`
* `setCharAt(int index, char ch)`：将指定索引处的字符设置为参数ch中的字符

## <span id="l">自动装箱与拆箱</span>
* 自动装箱就是Java自动将原始类型值转换成对应的对象，比如将int的变量转换成Integer对象，这个过程叫做装箱，反之将Integer对象转换成int类型值，这个过程叫做拆箱
> 原始类型`byte,short,char,int,long,float,double`和boolean对应的封装类为`Byte,Short,Character,Integer,Long,Float,Double,Boolean`
* 自动装箱时编译器调用valueOf将原始类型值转换成对象，同时自动拆箱时，编译器通过调用类似intValue(),doubleValue()这类的方法将对象转换成原始类型值

## <span id="m">在一个静态方法内调用一个非静态成员为什么是非法的</span>
* 类的静态成员（变量和方法）属于类本身，在类加载的时候就会分配内存，可以通过类名直接去访问
* 非静态成员（变量和方法）属于类的对象，所以只有在new类的对象产（创建类的实例）时才会分配内存，然后通过类的对象（实例）去访问

所以在一个类的静态成员中去访问其非静态成员会出错，是因为在类的非静态成员不存在时，类的静态成员就已存在，访问一个内存中不存在的东西就会出错
#### 类的初始化
###### 单例
静态变量、静态初始化块 > 变量、初始化块 > 构造器
###### 继承
父类
```java
class Parent {
    /* 静态变量 */
    public static String p_StaticField = "父类--静态变量";
    /* 变量 */
    public String p_Field = "父类--变量";
    protected int i = 9;
    protected int j = 0;

    /* 静态初始化块 */
    static {
        System.out.println(p_StaticField);
        System.out.println("父类--静态初始化块");
    }

    /* 初始化块 */ {
        System.out.println(p_Field);
        System.out.println("父类--初始化块");
    }

    /* 构造器 */
    public Parent() {
        System.out.println("父类--构造器");
        System.out.println("i=" + i + ", j=" + j);
        j = 20;
    }
}
```
子类
```java
public class SubClass extends Parent {
    /* 静态变量 */
    public static String s_StaticField = "子类--静态变量";
    /* 变量 */
    public String s_Field = "子类--变量";

    /* 静态初始化块 */
    static {
        System.out.println(s_StaticField);
        System.out.println("子类--静态初始化块");
    }

    /* 初始化块 */ {
        System.out.println(s_Field);
        System.out.println("子类--初始化块");
    }

    /* 构造器 */
    public SubClass() {
        System.out.println("子类--构造器");
        System.out.println("i=" + i + ",j=" + j);
    }


    /* 程序入口 */
    public static void main(String[] args) {
        System.out.println("子类main方法");
        new SubClass();
    }
}
```
输出
```
父类--静态变量
父类--静态初始化块
子类--静态变量
子类--静态初始化块
子类main方法
父类--变量
父类--初始化块
父类--构造器
i=9, j=0
子类--变量
子类--初始化块
子类--构造器
i=9,j=20
```

## <span id="n">在Java中定义一个不做事且没有参数的构造方法的作用</span>
构造函数的最大作用就是创建对象时完成初始化，因为当new一个对象并传入参数的时候，会自动调用构造函数并完成参数的初始化：
* 给创建的对象建立一个标识符
* 为对象数据成员开辟内存空间
* 完成对象数据成员的初始化
#### 默认构造函数
当用户没有显式的去定义构造函数时, 编译器会为类生成一个默认的构造函数
#### 主要特点
* 在对象被创建时自动执行
* 构造函数的函数名与类名相同
* 没有返回值类型、也没有返回值
* 构造函数不能被显式调用

## <span id="o">import java和javax有什么区别</span>
实际没有区别，都是Java的API包，java是核心包，javax是扩展包

## <span id="p">接口和抽象类的区别是什么</span>
#### 接口
* 接口由一组常量和一组抽象方法组成，不包含变量和具体实现的方法，除了default方法
* 支持多继承
* 声明：`interface`；实现：`implements`
#### 抽象类
* 抽象类只能作为继承层次中的父类，不能创建抽象类的对象
* 抽象类必须被继承，抽象方法必须被重写
* 声明：`abstract`
###### 区别
| 抽象类 | 接口 | 
| :----: | :----: |
| 抽象类里面的抽象方法必须全部被子类继承 `extends`，如果子类不能全部实现，那么子类必须也是抽象类 | 接口里面的方法也必须全部被子类实现 `implements`，如果子类不能实现那么子类必须是抽象类|
|可以有默认的方法实现 | 接口完全是抽象的，不存在方法的实现 |
| 抽象类可以有构造器 | 接口不能有构造器 |
| 除了不能实例化抽象类之外，它和普通Java类没有任何区别 | 接口是集合，不是类 | 
| 抽象方法可以有public、protected和default这些修饰符 | 接口方法默认修饰符是public，不可以使用其它修饰符 |
| 抽象类速度比接口快 | 接口速度较慢 |

## <span id="q">成员变量与局部变量的区别</span>
| 成员变量 | 局部变量 | 
| :----: | :----: |
|分为类变量（以static修饰）和实例变量（不以static修饰）| 分为形参、方法局部变量和代码块局部变量 |
| 声明在类里面，在方法体（方法，构造方法或代码块）之外 | 声明在方法体（方法，构造方法或代码块）内部，也就是`{}`中 |
| 有默认值，引用类型为null，其他为基本数据类型默认值 | 没有默认值，必须初始化赋值 |
| 在所在类被实例化后，存在堆内存中 | 在所在方法调用时，存在栈内存空间中 |
#### 堆和栈
###### 堆
* 用来存放由`new`创建的对象和数组
* 由Java虚拟机的自动垃圾回收器来管理
###### 栈
* 在函数中定义的一些基本类型的变量和对象的引用变量
* 当超过变量的作用域后，Java会自动释放掉为该变量所分配的内存空间，该内存空间可立即被另作他用

## <span id="r">创建一个对象用什么运算符 & 对象实体与对象引用有什么区别</span>
* 使用一个带有`new`操作符的构造函数，来创建新实例之后初始化类的实例
#### 对象
* 类的实例
* 一个对象可以被多个引用所指向
#### 对象引用
* 通过对象引用可以找到对象
* 一个引用可以指向多个对象

## <span id="s">什么是方法的返回值 & 返回值在类的方法里的作用是什么</span>
#### 返回值
* 规定了方法返回给调用者的结果值类型，可以定义为简单数据类型或类的类型
* 如果返回类型为void，则表示无返回值，不必写return语句；如果写return语句，在return之后必须带返回值
#### 作用
用来使程序流程从方法调用中返回
> 主函数的方法调用必须是静态的

## <span id="t">一个类的构造方法的作用是什么 & 若一个类没有申明构造方法，该程序能正确执行吗</span>
#### 作用
用于为类新建的对象分配内存空间和进行变量的初始化
> 构造方法只能在创建对象时用new命令调用
>     * 构造方法必须与其类名相同
>     * 构造方法没有返回类型（没有void），但可以有参数，并且可以被重载
#### 类中未定义构造方法的情况
编译时系统会提供一个缺省的无参的构造方法，其方法体为空

## <span id="u">构造方法有哪些特性</span>
* 构造器也叫构造方法
* 构造方法一般用于为类新建的对象分配内存空间和进行变量的初始化
* 构造方法只能在创建对象时用new命令调用
* 构造方法必须与其类名相同
* 构造方法没有返回类型，代表没有void
* 可以有参数，可以被重载
* 不能被重写

## <span id="v">静态方法和实例方法的区别</span>
|静态方法|实例方法|
|:----:|:----:|
|外部调用可以通过`类名.方法名`和`对象名.方法名`| 外部调用只能通过`对象名.方法名` |
| 在访问本类的成员时，只允许访问静态成员（即静态成员变量和静态方法），而不允许访问实例成员变量和实例方法 | 可以访问静态和实例成员 |

## <span id="w">对象的相等和指向他们的引用相等，有什么区别</span>
#### 对象的相等
通过`equals()`来判断两个对象是否相等
#### 引用相等
两个不同的引用指向同一对象

## <span id="x">在调用子类构造方法之前会先调用父类没有参数的构造方法，其目的是什么</span>
因为子类继承父类，会继承父类中的数据，所以子类在进行对象初始化时，会先调用父类的构造函数，这就是子类的实例化过程
* 构造方法会在类实例化对象时被自动调用
* 创建子类对象并调用子类构造方法的时候，会先调用父类的构造方法，在子类的构造方法中调用父类的构造方法是用`super()`，如果没有写`super()`，则默认调用父类的无参构造方法
* 如果父类写了有参的构造方法，则必须在子类的构造器中显示的调用父类的构造方法`super(父类构造器参数)`

||类内部|同一个包|子类|任意地方|
|:----:|:----:|:----:|:----:|:----:|
|private| * ||||
|default(系统默认可以不写)| * | * |||
|protected| * | * | * ||
|public| * | * | * | * |

## <span id="y">==与equals</span>
* `==`是判断两个变量或实例的地址是否相等，是不是指向同一个内存空间（堆内存）
* `equals`是判断两个变量或实例所指向的内存空间的值是不是相同
* `==`比`equals`运行速度快

## <span id="z">hashCode与equals</span>
#### hashCode()
* hashCode() 的作用是获取哈希码，也称为散列码；它实际上是返回一个int整数。这个哈希码的作用是确定该对象在哈希表中的索引位置
* hashCode()方法和equal()方法的作用其实一样
* hashCode() 在散列表中才有用，在其它情况下没用
> 在散列表中：
> * 如果两个对象相等，那么它们的hashCode()值一定要相同
> * 如果两个对象hashCode()相等，它们并不一定相等
#### 关联
* 如果两个对象equals，Java运行时环境会认为两者的hashcode一定相等
* 如果两个对象不equals，两者的hashcode有可能相等
* 如果两个对象hashcode相等，两者不一定equals
* 如果两个对象hashcode不相等，两者一定不equals

## <span id="aa">为什么Java中只有值传递</span>
值传递是指在调用函数时将实际参数复制一份传递到函数中，这样在函数中如果对参数进行修改，就不会影响到实际参数

## <span id="ab">简述线程、程序、进程的基本概念，以及它们之间的关系</span>
#### 线程
* 线程是程序执行的最小单位
* 进程中可独立执行的子任务，只有栈区是独立的
* 要想实现多线程，必须在主线程中创建新的线程对象
* 一个线程完整的生命周期要经历5个状态：创建状态、就绪状态、运行状态、阻塞状态和死亡状态
* 使用`synchonized`关键字进行线程同步
#### 进程
是程序一次动态执行的过程（从产生、发展到消亡）
#### 程序
是一段静态的代码，是应用软件执行的蓝本
#### 三者间关系
* 一个进程可以拥有多个线程
* 一个程序可以有多个进程（多次执行，也可以没有进程不执行）
* 一台机器上可以有多个JVM实例（也可以没有JVM实例）
* 通过多次执行一个程序可以有多个进程，通过调用一个进程可以有多个程序

## <span id="ac">线程有哪些基本状态 & 这些基本状态是怎么定义的</span>
一个线程完整的生命周期要经历5个状态：创建状态、就绪状态、运行状态、阻塞状态和死亡状态
#### 创建状态 Born
执行`Thread myThread = new Thread()`后，线程就处于创建状态，此时已经有了相应的内存空间和其他资源
#### 就绪状态 Ready(也叫可运行状态 Runnable)
执行`myThread.start()`后，就处于就绪状态，将进入线程队列排队等待分配CPU时间片
> 原来处于阻塞状态的线程被解除阻塞后，也将进入就绪状态
#### 运行状态 Running
当线程对象被调度执行时，将自动调用此线程对象的`run()`方法
> 处于运行中的线程，因调用方法`yield()`会自动放弃CPU而进入就绪状态
#### 阻塞状态 Blocked、Waiting、Sleeping
阻塞时该线程不能进入排队队列
* 处于运行状态的线程进入阻塞状态的原因

    * 线程调用了`sleep()`方法，而进入睡眠状态；睡眠时间到期或者线程调用了方法`interrupt()`，使睡眠状态结束，进入就绪状态
      
    * 为等待访问某个共享对象的信号变量，当前线程调用了`wait()`方法而进入等待状态，直到另一线程为共享对象调用了方法`notify()`或`notifyAll()`为止，使该线程等待状态结束而进入就绪状态；处于等待状态的线程，因调用了`interrupt()`方法，也会使等待状态结束，进入就绪状态
      
    * 线程进入同步`synchronized`语句时，因要对共享的对象加排斥锁而未获成功，也将进入阻塞状态，直到获得排斥锁为止
      
    * 线程因输入输出请求，导致线程阻塞，输入输出操作完成时，使线程进入就绪状态
#### 死亡状态 Dead
当一个`thread`执行结束（即从`run()`方法返回时），将到达死亡状态，不再具有继续运行的能力

## <span id="ad">关于final关键字的一些总结</span>
#### 修饰类
* 当用final修饰一个类时，表明这个类不能被继承
* 当一个类不希望被修改，或不希望被继承时才被设计为final
* final类中的成员方法都会被隐式地指定为final方法，因此不能对这些方法进行覆盖和修改
* final类中的非final域变量可以被修改，final类中的成员变量可以根据自己的实际需要设计为final
#### 修饰方法
* 被final修饰的方法不能被重写（可以重载多个final修饰的方法）
* 使用final方法：原因一是把方法锁定，以防任何继承类修改它的含义；原因二是效率
* 一个类的private方法会隐式的被指定为final方法
#### 修饰变量
* final成员变量表示常量，只能被赋值一次，赋值后值不再改变
* 当函数的参数类型声明为final时，说明该参数可以读取，但无法改变它的值

## <span id="ae">Java中的异常处理（异常类层次结构、Throwable类常用方法、异常处理总结）</span>
#### 层次结构
```
Throwable ___Exception ___RuntimeException
         |            |___IOException ___ArithmeticException 算术运算溢出，如除数为零
         |                            ___ArrayIndexOutOfBandsException 数组下标越界异常
         |                            ___ArrayStoreException 数组存储异常，如数组复制时，两者类型不一致时，导致异常
         |                            ___NullPointerException 空指针异常
         |                            ___NumberFormatException 数据格式异常
         |                            ___OutOfMemoryException 内存溢出异常
         |                            ___IOException 输入/输出中的异常
         |                            ___FileNotFoundException 文件找不到异常
         |                            ___NoClassDefFoundException 没有找到类定义时的异常
         |___Error    
```
#### Throwable类常用方法
* Throwable类是所有异常的父类
* 几个常见方法

    * getMessage()：获取异常信息，返回字符串
      
    * toString()：获取异常类名和异常信息，返回字符串
      
    * printStackTrace()：获取异常类名和异常信息，以及异常出现在程序中的位置；返回值void
      
```
public class Demo_Throwable {
    public static void main(String[] args) {
        try{
            System.out.println(1/0);
        }catch(Exception e){    //Exception e = new AithmeticException("/ by zero")
            // System.out.println(e.getMessage()); //获取异常信息  / by zero
            // System.out.println(e); //默认调用toString()方法，打印异常类名和异常信息  
            // java.lang.ArithmeticException: / by zero
            e.printStackTrace();  //JVM默认就用这种方式处理异常
        }
        catch(要处理的异常类型和标识符){
            // catch 一个异常并进行异常处理
        }
        ...
        
        finally{
            // 最终处理
        }
    }

}
```
#### 小结
* 应根据具体的情况选择在何处处理异常
     * 在方法内捕获并处理
     * 用throws子句把它交给调用栈中上层的方法去处理
* 对非运行时异常必须捕获或声明
* 异常可以人为地抛出，用throw new语句
* 异常可以是系统已经定义好的，也可以是用户自己定义的（必须继承自Throwable或Exception类）
* 应该使用finally语句为异常处理提供统一的出口

## <span id="af">java序列化中如果有些字段不想进行序列化，怎么办</span>
#### 序列化
把对象转换为字节序列的过程称为对象的序列化
#### 反序列化
把字节序列恢复为对象的过程称为对象的反序列化
#### 常用用途
* 把对象的字节序列永久地保存到硬盘上，通常存放在一个文件中，让它们离开内存空间
* 在网络上传送对象的字节序列
> 当两个进程在进行远程通信时，彼此可以发送各种类型的数据；无论是何种类型的数据，都会以二进制序列的形式在网络上传送；发送方需要把这个Java对象转换为字节序列，才能在网络上传送；接收方则需要把字节序列再恢复为Java对象
#### JDK类库中的序列化API
###### 对象序列化步骤
1、创建一个对象输出流，它可以包装一个其他类型的目标输出流，如文件输出流
2、通过对象输出流的writeObject()方法写对象
###### 对象反序列化步骤
1、创建一个对象输入流，它可以包装一个其他类型的源输入流，如文件输入流
2、通过对象输入流的readObject()方法读取对象
###### 示例
```java
import java.io.Serializable;

public class Person implements Serializable {
    /**
     * 序列化ID
     */
    private static final long serialVersionUID = -5809782578272943999L;
    private int age;
    private String name;
    private String sex;

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getSex() {
        return sex;
    }

    public void setSex(String sex) {
        this.sex = sex;
    }
}
```
```java
import java.io.*;
import java.text.MessageFormat;

public class TestObjSerializeAndDeserialize {
    public static void main(String[] args) throws Exception{
        SerializePerson();
        Person p = DeserializePerson();
//        System.out.println(p);
        System.out.println(MessageFormat.format("name={0}, age={1}, sex={2}",p.getName(),p.getAge(),p.getSex()));
    }
    /**
     * 序列化Person对象
     */
    private static void SerializePerson() throws IOException{
        Person person = new Person();
        person.setName("fortunate");
        person.setSex("female");
        person.setAge(26);
        // ObjectOutputStream 对象输出流，将Person对象存储到E盘的Person.txt文件中，完成对Person对象的序列化操作
        ObjectOutputStream oo = new ObjectOutputStream(new FileOutputStream(new File("Person.txt")));
        oo.writeObject(person);
        System.out.println("Person对象 序列化成功！");
        oo.close();
    }
    /**
     * 反序列化Person对象
     */
    private static Person DeserializePerson() throws Exception {
        ObjectInputStream ois = new ObjectInputStream(new FileInputStream(new File("Person.txt")));
        Person person = (Person) ois.readObject();
        System.out.println("Person对象 反序列化成功！");
        return person;
    }
}
```
输出
```
Person对象 序列化成功！
Person对象 反序列化成功！
name=fortunate, age=26, sex=female
```
