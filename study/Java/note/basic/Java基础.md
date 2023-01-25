



# Java基础

[toc]

## 基本常识

### 工程，模块，包和类

结构如下

* 工程
  * 模块
    * 包
      	* 类

**工程(project)**

![image-20230123160238603](Java基础.assets/image-20230123160238603.png)

**包(packet)**

在src文件下面右键创立package，package中有.java文件，各种类，接口

**类(class)**

在package底下就可以创建类了，我们在类里面写属性、方法

**模块(module)**

如果想要在这个工程的平行的再建立一个工程，可以右键打开我们的工程存放的文件夹，然后新建module就可以

**关系**

* 一个包下面的资源都是共享的（除非是private），不同包下的资源相互使用的时候，需要引入包

  引入包：import

* 不同的项目之间的资源是不共享的

### 各种文件

#### out 文件

存放javac编译后的字节码的

#### .idea文件

这个是编译的配置文件，编译的内容包括可以控制编译之后的类的位置，工作空间的相关配置，库的配置，编码配置和其他的插件配置等等。如果没有这个配置文件，程序就很难正常的跑起来，即使环境是配置良好的。

##基本语法

### 背景

####Java技术平台

1. Java SE （Java Standard Edition） 标准版

   支持面向**桌面级应用**（如Windows 下的应用程序）的 Java 平台，提供了完整的 Java 核
   心 API ，此版本以前称为 J2SE

2. Java EE    (Java Enterprise Edition) 企业版

   是为开发企业环境下的应用程序提供的一套解决方案。该技术体系中包含的技术如
   Servlet 、 Jsp 等，**主要针对于 Web 应用程序开发**。版本以前称为 J2EE

3. Java ME(Java Micro Edition) 小型版

   支持Java 程序运行在移动终端（手机、 PDA ）上的平台

#### 跨平台

因为JVM

![image-20230119105913314](C:\Users\Fire Keeper\AppData\Roaming\Typora\typora-user-images\image-20230119105913314.png)

#### 核心机制

1. Java 虚拟机 (Java Virtal Machine）

   ![image-20230119110153271](C:\Users\Fire Keeper\AppData\Roaming\Typora\typora-user-images\image-20230119110153271.png)

   

2. 垃圾收集机制 (Garbage Collection）

#### 环境配置

![image-20230119111303493](C:\Users\Fire Keeper\AppData\Roaming\Typora\typora-user-images\image-20230119111303493.png)

![image-20230119111414971](C:\Users\Fire Keeper\AppData\Roaming\Typora\typora-user-images\image-20230119111414971.png)

**简单而言，使用JDK 的开发工具完成的 java 程序，交给 JRE 去运行。**

* JDK (Java Development Kit）

   Java 开发工具包 包括了JRE

* JRE (Java Runtime Environment)

   Java 运行环境 包括JVM和各种库

  运行只要有JRE就行

* 环境变量 

  path： windows 系统执行命令时要搜寻的路径。正常来说，执行一个程序，需要进入程序所在的目录，设置环境变量，可以全局执行程序

  ![image-20230119130648832](Java基础.assets/image-20230119130648832.png)

  windows中的查找规则就是首先在当前目录中查找，没有，就在环境变量中查找

* Javac

  编译时使用

* Java

  运行时使用

* Javadoc 

  网页文档

###程序如何执行？

1. 把Java代码编写到.java文件中 (使用记事本)

   ![image-20230119151101429](Java基础.assets/image-20230119151101429.png)

2. 通过 javac 命令对该 java 文件进行编译 （使用命令行 + javac）

   注意：class的文件名要和代码中一致

   ![image-20230119151407184](Java基础.assets/image-20230119151407184.png)

   ![image-20230119151125778](Java基础.assets/image-20230119151125778.png)

3. 通过 java 命令对生成的 class 文件进行运行 

   ![image-20230119151441875](Java基础.assets/image-20230119151441875.png)

   ![image-20230119145940817](Java基础.assets/image-20230119145940817.png)



### 文档注释（Java特有）

格式：/**
		@author 指定java程序的作者
		@version 指定源文件的版本
*/

注释内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档。单行多行注释不可以被javadoc解析

### 变量的分类

![image-20230119200843339](Java基础.assets/image-20230119200843339.png)

![image-20230119201732989](Java基础.assets/image-20230119201732989.png)

成员变量：在方法体外，类体内声明的变量

局部变量：在方法体内部声明的变量

成员变量是在对象创建以后存在于堆中，对象回收时，成员变量消失
局部变量是在方法被调用时存在于栈中，方法调执行结束，从栈中清除

成员变量：随对象的创建而创建，对象回收时，成员变量消失
局部变量：随着方法的调用被创建，方法执行结束后，从栈中清除

### Java命名规范

包名 ：多单词组成时所有字母都小写 xxxyyyzzz
类名、接口名 ：多单词组成时，所有单词的首字母大写 XxxYyyZzz
变量名、方法名 ：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写： xxxYyyZzz
常量名 ：所有字母都大写。多单词时每个单词用**下划线**连接 XXX_YYY_ZZZ

### 关键字和保留字

Java中的关键字都是小写的

保留字：goto和const

### 标识符

严格区分大小写，数字不能作为开头，不包含空格

### 基本数据类型

#### 整型和浮点型

![image-20230120100356626](Java基础.assets/image-20230120100356626.png)

![image-20230120100923979](Java基础.assets/image-20230120100923979.png)

java 的整型常量默认为 int 型，声明 long 型常量须后加‘ l’ 或‘ L’
Java 的浮点型常量默认为 double 型 声明 float 型常量，须后加‘ f’ 或‘ F’ 

#### 字符型

char：1字符 = 2字节

Java 中的所有字符都使用 Unicode 编码, 故一个字符可以存储一个字母，一个汉字，或其他书面语的一个字符

字符型变量的三种表现形式:

1. 字符常量是用单引号括起来的单个字符。 例如： char c1 = 'a'; char c2 = '中';
2. Java 中还允许使用转义字符‘ ‘\\’来 将其后的字符转变为特殊字符型常量。例如： char c3 = ‘ \n';
3. 直接使用 **Unicode** 值来表示字符型常量：'\uXXXX', 其中， '\uXXXX' 代表一个十六进制整数。如：\u000a 表示 \n ;

char类型是可以进行运算的。因为它都对应有Unicode码

#### 布尔型

1. 不可以使用0或非 0 的整数替代false和true，这点和C语言不同

2. 在编译之后都使用java虚拟机中的int数据类型来代替：true用1表示，false用0表示

### 数据类型转换

#### 自动类型转换

容量小的类型自动转换为容量大的数据类型。数据类型按容量大小排序为：

![image-20230120103701929](Java基础.assets/image-20230120103701929.png)

注意

1. 有多种类型的数据混合运算时，系统首先自动将所有数据转换成容量最大的那种数据类型，然后再进行计算
2. byte,short,char之间不会相互转换，他们三者在计算时首先转换为int类型
3. boolean类型不能与其它数据类型运算
4. **当把任何基本数据类型的值和字符串(String)进行连接运算时(+)，基本数据类型的值将自动转化为字符串(String)类型**

例子

<img src="Java基础.assets/image-20230120104251990.png" alt="image-20230120104251990" style="zoom:67%;" />

#### 强制类型转换

* 将容量大的数据类型转换为容量小的数据类型，使用时要加上强制转换符：()，但可能造成精度降低或溢出,格外要注意

* 通常，字符串不能直接转换为基本类型，但通过基本类型对应的包装类则可以实现把字符串转换成基本类型
* boolean类型不可以转换为其它的数据类型

<img src="Java基础.assets/image-20230120105107697.png" alt="image-20230120105107697" style="zoom:67%;" />



### 运算符

“+”除字符串相加功能外，还能把非字符串转换成字符串.例如：System.out.println(“5+5=”+5+5); //打印结果： 5+5=55 

#### instanceof 

检查是否是类的对象

```java
if("ellie" instanceof String)
            System.out.println("YES");
else
            System.out.println("No");
```

#### 逻辑运算符

<img src="Java基础.assets/image-20230120112408470.png" alt="image-20230120112408470" style="zoom:67%;" />

* “&”和“&&”的区别：
  单&时，左边无论真假，右边都进行运算；
  双&时，如果左边为真，右边参与运算，如果左边为假，那么右边不参与运算。

#### 位运算符

**位运算是直接对整数的二进制进行的运算**

![image-20230120112959605](Java基础.assets/image-20230120112959605.png)

右移和无符号右移的区别：

![image-20230120113139197](Java基础.assets/image-20230120113139197.png)

![image-20230120113248486](Java基础.assets/image-20230120113248486.png)

### 数组

* 数组一旦初始化，其长度是不可变的

* 每个数组都有一个属性length指明它的长度，例如：a.length 指明数组a的长度(元素个数)

* 数组是引用类型，它的元素相当于类的成员变量，因此数组一经分配空间，其中的每个元素也被按照成员变量同样的方式被隐式初始化

* 对于基本数据类型而言，默认初始化值各有不同
  对于引用数据类型而言，默认初始化值为null (注意与0不同)

* 比如 int[] arr = new int{3,4,5}; 这里arr就是指向堆区中分配3，4，5元素的首地址的指针

  <img src="Java基础.assets/image-20230120144444216.png" alt="image-20230120144444216" style="zoom: 50%;" />

#### 声明方式

type var [] 或 type[] var

注意：Java 语言中声明数组时不能指定其长度 数组中元素的数 例如： int a[5]; 非法

#### 初始化

* 动态初始化

  数组声明且为数组元素分配空间 与 赋值的操作 分开进行

  ```java
  int[] arr = new int[3];
  arr[0] = 3;
  arr[1] = 9;
  arr[2] = 8;
  ```

  

* 静态初始化

  在定义数组的同时就为数组元素分配空间并赋值

  ```java
  int arr[] = new int[]{3, 9, 8};
  int[] arr = {3,9,8};
  String names[] = {"ellie", "joel"};
  ```

#### 二维数组

内存解析

![image-20230120154248409](Java基础.assets/image-20230120154248409.png)

![image-20230120154528843](Java基础.assets/image-20230120154528843.png)

![image-20230123143803539](Java基础.assets/image-20230123143803539.png)

* 动态初始化 

  **int\[][] arr = new int \[3][2];**

  定义了名称为arr的二维数组
  二维数组中有3个一维数组
  每一个一维数组中有2个元素
  一维数组的名称分别为arr[0], arr[1], arr[2]
  给第一个一维数组1脚标位赋值为78写法是：arr\[0][1] = 78;

  **int\[][] arr = new int\[3][];**

  二维数组中有3个一维数组
  每个一维数组都是默认初始化值null (注意：区别于格式1）可以对这个三个一维数组分别进行初始化

  arr[0] = new int[3];    arr[1] = new int[1];   arr[2] = new int[2];

  **int\[][] arr = new int\[][3];  //非法**

* 静态初始化

  **int\[][] arr = new int\[][]{{3,8,2},{2,7},{9,0,1,6}};**

  定义一个名称为arr的二维数组，二维数组中有三个一维数组每一个一维数组中具体元素也都已初始化
  第一个一维数组 arr[0] = {3,8,2};
  第二个一维数组 arr[1] = {2,7};
  第三个一维数组 arr[2] = {9,0,1,6};
  第三个一维数组的长度表示方式：arr[2].length

  * **注意特殊写法情况：int[] x,y[]; x是一维数组，y是二维数组。**
  * **Java中多维数组不必都是规则矩阵形式**

#### 数组中的常见异常

![image-20230121115238398](Java基础.assets/image-20230121115238398.png)

**编译时，不报错**

### 零碎

* 一个源文件中最多只能有一个public类。其它类的个数不限，如果源文件包含一个public类，则文件名必须按该类名命名

* Java中定义成员变量时采用合法的 前向引用

  ```java
  public class Test{
  	int num1 = 12;
  	int num2 = num1 + 2;
  }
  错误形式：
  public class Test{
  	int num2 = num1 + 2
  	int num1 = 12;
  }
  
  ```

  

* switch( 表达式）中 表达式的值 必须 是下述几种类型之一： byte short char int 枚举 (jdk String (jdk 7.0)

  case 子句中的值必须是常量

  ```Java
  String season = "summer";
  switch (season){
              case "spring":
                  System.out.println("Ellie");
                  break;
              case "summer":
                  System.out.println("Joel");
                  break;
              default:
                  System.out.println("Wolf");
   }
  ```

  

* 什么是Unicode？

  一种编码，将世界上所有的符号都纳入其中。每一个符号都给予一个独一无二的编码，使用 Unicode 没有乱码的问题

* 为什么会产生乱码？

  乱码：世界上存在着多种编码方式，**同一个二进制数字可以被解释成不同的符号**。因此，要想打开一个文本文件，就必须知道它的编码方式，否则用错误的编码方式解读，就会出现乱码 。

* UTF_8

  互联网上使用最广的**一种 Unicode 的实现方式**，变长的编码方式。它可以使用 1-6 个字节表示一个符号，根据不同的符号而变化字节长度。





## 面向对象

### 基本概念

#### 属性（成员变量）

修饰符 数据 类型 属性 名 = 初始化值 ;

在方法体外，类体内声明的变量

```java
private int age;
```

<img src="Java基础.assets/image-20230123142326274.png" alt="image-20230123142326274" style="zoom:67%;" />

**在堆或静态域中！！！**

前面可以有修饰符

#### 局部变量

在方法体内部声明的变量

栈区或静态区域内

**前面没有修饰符**

#### 方法（函数）

行 为：对应类中的成员方法（方法就是函数）

方法前面有修饰符

##### 可变参数形参

```java
public static void test(int a ,String…books);//基本语法

public class OOPTest {//例子
    public static void main(String[] args) {
        String[] arr = {"ellie", "joel"};
        test(arr);
        test("joel","ellie");
        test(new String[]{"joel", "ellie"});
    }
    public static void test(String...arg){
        for (int i = 0; i != arg.length; ++i){
            System.out.println(arg[i]);
        }
    }
}
```

可变参数方法的使用与方法参数部分使用数组是一致的

方法的参数部分有可变形参，需要放在形参声明的最后

##### 参数传递

Java里方法的参数传递方式只有一种： 值传递

* 形参是基本数据类型：将实参基本数据类型变量的“数据值”传递给形参

* 形参是引用数据类型：将实参引用数据类型变量的“地址值”传递给形参


**Java里的方法不能独立存在，所有的方法必须定义在类里**



### 类的基本语法格式

堆区：此内存区域的唯一目的就是**存放对象实例**，虚拟机规范中的描述是：所有的
对象实例**以及数组**都要在堆上分配

栈区：自动释放

方法区：用于存储已被虚拟机加载的类信息 、 常量 、 静态变量 、 即时编译器编译后的代码等数据 

![image-20230123141253909](Java基础.assets/image-20230123141253909.png)

![image-20230123104510393](Java基础.assets/image-20230123104510393.png)

### 对象的内存解析

![image-20230123111346996](Java基础.assets/image-20230123111346996.png)

![image-20230123120328072](Java基础.assets/image-20230123120328072.png)

### 封装继承多态

#### 封装

隐藏细节，使用方法来访问数据

**四种访问权限修饰符以及权限（类成员前面的）**

![image-20230123155640722](Java基础.assets/image-20230123155640722.png)

四种权限都可以用来修饰类的内部结构：属性，方法，构造器和内部类

修饰类的话，只能使用：default或者public

#### 继承

**基本知识**

* 子类中继承了父类的方法和变量，但是不能访问父类中的私有成员变量和方法
* Java中不允许多重继承

<img src="Java基础.assets/image-20230125134940818.png" alt="image-20230125134940818" style="zoom: 67%;" />

**Overwrite（方法的重写）**

* 定义

  在子类中可以根据需要对从父类中继承来的方法进行改造，也称为方法的重置、覆盖。在程序执行时，子类的方法将**覆盖**父类的方法

* 要求

  1.	子类重写的方法必须和父类被重写的方法具有相同的方法名称、参数列表
  2.	子类重写的方法的返回值类型不能大于父类被重写的方法的返回值类型（返回值类型更严格）
  3.	子类重写的方法使用的访问权限不能小于父类被重写的方法的访问权限（访问权限更宽松）
  	子类不能重写父类中声明为private权限的方法
  4.	子类方法抛出的异常不能大于父类被重写方法的异常

* 注意

  子类与父类中同名同参数的方法必须同时声明为非static的(即为重写)，或者同时声明为static的（不是重写）。**因为static方法是属于类的**，子类无法覆盖父类的方法。

![image-20230125141915004](Java基础.assets/image-20230125141915004.png)



#### 多态

多态性：父类的引用指向子类的对象

Java**引用变量**有两个类型：**编译时类型**和**运行时类型**。编译时类型由声明该变量时使用的类型决定，运行时类型由实际赋给该变量的对象决定。简称：编译时，看左边；运行时，看右边

若编译时类型和运行时类型不一致，就出现了对象的多态性

**成员变量不具有多态性！**

一个例子：比如有继承关系：Animal - Wolf - BabyWolf

```java
Creature[] arr = new Creature[]{new Animal(), new Wolf(), new Animal(), new BabyWolf()};
        for(int i = 0; i < arr.length; ++i){
            if(arr[i] instanceof BabyWolf){
                System.out.println("No." + i + " is a BabyWolf");
            }
            else if(arr[i] instanceof Wolf){
                System.out.println("No." + i + " is a Wolf");
            }
            else
                System.out.println("No." + i + " is a Animal");
        }
```

![image-20230125154222072](Java基础.assets/image-20230125154222072.png)



<img src="Java基础.assets/image-20230125151216751.png" alt="image-20230125151216751" style="zoom:80%;" />

**虚拟方法调用**

![image-20230125151751609](Java基础.assets/image-20230125151751609.png)

**重载和重写**

![image-20230125152057817](Java基础.assets/image-20230125152057817.png)

**对象类型转换**

Java对象的强制类型转换称为造型

* 从子类到父类的类型转换可以自动进行
  从父类到子类的类型转换必须通过造型(强制类型转换)实现
  无继承关系的引用类型间的转换是非法的
  在造型前可以使用instanceof操作符测试一个对象的类型

**和c++一模一样！**

必看的图

![image-20230125155243365](Java基础.assets/image-20230125155243365.png)

* 若子类重写了父类**方法**，就意味着子类里定义的方法彻底覆盖了父类里的同名方法，系统将不可能把父类里的方法转移到子类中

* 对于**实例变量**则不存在这样的现象，即使子类里定义了与父类完全相同的实例变量，这个实例变量依然不可能覆盖父类中定义的实例变量

### 构造器

* 不能被 static 、 final 、 synchronized 、 abstract 、 native 修饰，不能有return 语句返回值

* 前面有修饰符
* 默认构造器的修饰符和所属类的修饰符一致
* 一旦显示提供构造器，系统不再提供默认构造器
* 可以创建多个重载的构造器
* 父类的构造器不能被子类继承

语法格式：

```java
public class Animal {
	private int legs;
	//构造器
	public Animal() {
    	legs = 4;
	}
	public void setLegs( int i )
		legs = i;
	}
	public int getLegs() {
		return legs;
	}
}
```

**JavaBean**

一种Java语言写成的可重用组件

所谓javaBean，是指符合如下标准的Java类：

1. 类是公共的
2. 有一个无参的公共的构造器
3. 有属性，且有对应的get、set方法

**UML类图**

![image-20230124115045409](Java基础.assets/image-20230124115045409.png)

#### 关键字this

* 它在方法内部使用，即这个方法所属对象的引用

* 它在构造器内部使用，表示该构造器正在初始化的对象

* 使用 this 访问属性和方法时，如果在本类中未找到，会从父类中查找

* **this可以作为一个 类中构造器相互调用的特殊格式**

  "this(形参列表)"必须声明在类的构造器的首行！

  在类的一个构造器中，最多只能声明一个"this(形参列表)"

  <img src="Java基础.assets/image-20230124115542799.png" alt="image-20230124115542799" style="zoom: 67%;" />

  

### 各种关键字

#### packet，import

**packet:**

package语句作为Java源文件的第一条语句，指明该文件中定义的类所在的包。(若缺省该语句，则指定为无包)。它的格式为：
package 顶层包名.子包名 

每"."一次，就是一层文件目录

同一个包下，接口，类的名称必须是唯一的

![image-20230124134841675](Java基础.assets/image-20230124134841675.png)

![image-20230124162913273](Java基础.assets/image-20230124162913273.png)

![image-20230124163917270](Java基础.assets/image-20230124163917270.png)

**上面这个包，每个点都是一层目录！！！**

包对应于文件系统的目录，package语句中，用 “.” 来指明包(目录)的层次；
包通常用小写单词标识。通常使用所在公司域名的倒置：com.atguigu.xxx

![image-20230124135043034](Java基础.assets/image-20230124135043034.png)

**包的作用**

1. 解决类命名冲突的问题
2. 控制访问权限
3. 包可以包含类和子包，划分项目层次，便于管理
4. 包帮助管理大型软件系统：将功能相近的类划分到同一个包中。比如：MVC的设计模式

**MVC(module view and controller)设计模式**

MVC是常用的设计模式之一，将整个程序分为三个层次：视图模型层，控制器层，与数据模型层

![image-20230124135736868](Java基础.assets/image-20230124135736868.png)

<img src="Java基础.assets/image-20230124140008074.png" alt="image-20230124140008074" style="zoom:67%;" />

![image-20230124140547163](Java基础.assets/image-20230124140547163.png)

**import:**

import语句告诉编译器到哪里去寻找**类或接口**

语法格式：import 包名 . 类名

![image-20230124140818079](Java基础.assets/image-20230124140818079.png)

Tips

1. 声明在包的声明和类的声明之间
2. 举例：可以使用java.util.*的方式，一次性导入util包下所有的类或接口
3. 如果在代码中使用不同包下的同名的类。那么就需要使用类的全类名的方式指明调用的是哪个类
4. 如果已经导入java.a包下的类。那么如果需要使用a·包的子包下的类的话，仍然需要导入
5. import static组合的使用：调用指定类或接口下的静态的属性或方法

#### super

使用super来调用父类中的指定操作

* super可用于访问父类中定义的属性
* super可用于调用父类中定义的成员方法
* super可用于在子类构造器中调用父类的构造器

![](Java基础.assets/image-20230125142331463.png)

注意：

* 尤其当子父类出现同名成员时，可以用super表明调用的是父类中的成员
* **super的追溯不仅限于直接父类**
* super和this的用法相像，this代表本类对象的引用，super代表父类的内存空间的标识

**调用父类的构造器**

* 子类中所有的构造器默认都会访问父类中**空参数的构造器**

* 当父类中没有空参数的构造器时，子类的构造器必须通过this(参数列表)或者super(参数列表)语句指定调用本类或者父类中相应的构造器。同时，只能”二选一”，且必须放在构造器的首行
* 如果子类构造器中既未显式调用父类或本类的构造器，且父类中又没有无参的构造器，则编译出错

![image-20230125142717223](Java基础.assets/image-20230125142717223.png)

<img src="Java基础.assets/image-20230125142909542.png" alt="image-20230125142909542" style="zoom:67%;" />

**子类对象实例化过程**

一句话概括，非常简单，就是正常函数的调用过程

<img src="Java基础.assets/image-20230125144254674.png" alt="image-20230125144254674" style="zoom:150%;" />

<img src="Java基础.assets/image-20230125144842743.png" alt="image-20230125144842743" style="zoom: 50%;" />

<img src="Java基础.assets/image-20230125145030126.png" alt="image-20230125145030126" style="zoom: 50%;" />

上图中，箭头表示构造器之间的相互调用



### 静态变量和函数

#### 静态成员函数（静态方法）

只能访问静态成员变量，不然会报错



### 匿名对象

```java
new Person().shout();//可以使用匿名对象调用方法
```



## 高级应用



## 各种工具类

### Arrays

java.util.Arrays类即为操作数组的工具类，包含了用来操作数组（比如排序和搜索）的各种方法。

java.util is a packet

Arrays 是这个包下的一个类

常用接口

![image-20230121115017752](Java基础.assets/image-20230121115017752.png)