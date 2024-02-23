# 1. Introduction to Java

## 1.1 Essentials <a href="#running-a-java-program" id="running-a-java-program"></a>

## Running a Java Program <a href="#running-a-java-program" id="running-a-java-program"></a>

1. javac HelloWorld.java
2. java HelloWorld

## Variables and Loops

1. variables 使用前需要先声明一个类型
2. loop 的内容需要用{}括起来，判断用()括起来
3. System.out.print不会另起一行，System.out.println会另起一行

## Static Typing

静态变量属于类，不属于类中任何一个对象，因此**静态变量又叫做类变量**，一个类不管创建多少个对象（对象是类的一个实例），**静态变量在内存中有且仅有一个**。

## Defining Functions in Java

对于java，我们必须定义functions 是属于哪个class的。Functions 是class 的一部分，称为"method"。

我们可以用  `public static` 声明，和python 里的 `def` 类似。

## Code Style, Comments, Javadoc

规范很重要

## Comments

写代码 self-documenting，描述自己的代码是什么功能，可以遵循Javadoc格式。比如，使用`/**` 。



## 1.2 Objects

### Defining and Using Classes

### static Methods

所有的代码写在methods里

```java
public class Dog {
    public static void makeNoise() {
        System.out.println("Bark!");
    }
}
```

会报错，因为dog class 没有坐任何事情。要想让Dog class运行，要不就加一个main method， 或者可以create一个 `DogLauncher class`用来运行Dog Class 中的methonds.

```java
public class DogLauncher {
    public static void main(String[] args) {
            Dog.makeNoise();
        } 
    }
```

一个类型用另一个类型，通常称为这个类型的client，比如`DogLauncher`就是Dog的Client。

### Instance Variables and Object Instantiation

不是所有的狗都是一样的，需要为每个类型的狗来创建一个自己的不同的class。

```javascript
public class TinyDog {
    public static void makeNoise() {
        System.out.println("yip");
        }
}
public class MalamuteDog{
    public static void makeNoise() {
        System.out.println("aroo");        
    }
}
```

```java
public class DogLauncher {
    public static void main(String[] args) {
        Dog d;
        d = new Dog();
        d.weightInPounds = 20;
        d.makeNoise();
    }
}
```

classes 可以用来实例化，实例包括data。使得dog的行为取决于properties，因为我们把狗实例化。

* 对象是class的一个实例化
* dog class 有自己的变量，叫作instance variables 或者是non-static variables。这些必须在class里声明，python和matlab可以在任何地方添加variables.
* 为了调用 `makeNoise` method, 我们首先用new实例化Dog，然后make a specific Dog bark。也就是说我们用 d.makeNoise 而不是 Dog.makeNoise()
* 一旦一个对象（object)被实例化，可以分配一个已声明的变量。d = new Dog();
* 变量和方法也称作class 的members
* 一个class的members用dot 符号表示

## Constructors in java

对于面向对象编程，用constructor 来构建objects

```
public class DogLauncher {
    public static void main(String[] args) {
        Dog d = new Dog(20);
        d.makeNoise();    
    }
}
```

下面，实例被参数化，需要加一个constructor 到 Dog class

```java
public class Dog {
    public int weightInPounds;
    
    public Dog(int w) {
        weightInPounds = w;
    }
    public void makeNoise() {
        if (weightInPounds < 10) {
            System.out.println("yipy");
        } else if (weightInPounds < 30) {
            System.out.println("bark");
        } else {
            System.out.println("woof");
        }
    }
}
```

这个constructor 有一个public Dog(int w) 类似于 python `__init__` ,当用 `new` 关键字和 一个整数参数的时候，创建一个新的Dog。

## Array Instantiation, Arrays of objects

arrays 可以通过 `new` 关键字实例化

```java
public class ArrayDemo {
    public static void main(String[] args) {
        int[] someArray = new int[5];
        someArray[0] = 3;
        someArray[1] = 4;
    }
}
```

同样

```
public class DogArrayDemo {
    public static void main(String[] args) {
        Dog[] dogs = new Dog[2];
        dogs[0] = new Dog(8);
        
        dogs[0].makeNoise();
    }
}
```

main()方法的参数是一个String对象的数组。args，Java编译器要求必须这样写，因为args要用来存储命令行参数。

`new` 这个关键字可以用于两种方式，第一个是 创建一个array（包括2个dog 对象），用\[]，第二个是创建一个真实的狗，用()

## Class Methods vs. Instance Methods

Java 定义2种methods

* 类method, 静态方法
* 例method, 非静态

Instance methods 是类的特别例子。类methods是类自己。

比如一个静态的例子， `math`类提供`sqrt` method:

```
x = Math.sqrt(100);

Math m = new Math();
x = m.sqrt(100);
```

比如一个类里包含instance methods 和 static methods.

我们想比较两种狗，一个方法是通过static method

```
public static Dog maxDog(Dog d1, Dog d2) {
    if (d1.weightInPounds > d2.weightInPounds) {
        return d1;
    }
    return d2;
}
```









