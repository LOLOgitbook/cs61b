# lecture

1. Before Java variables can be used, they must be declared
2. java variables must have a specific type
3. java variable types can never change
4. types are verified before the code runs! If there are type issues, the code will not compile.
5. &#x20;all parameters of a function must have a type and the function itself must have a return type.
6. all functions must be part of a class. in programming language terminology, a function that is a part of a class is called  a method. so all functions in  java are methods.

<figure><img src="../../.gitbook/assets/Screenshot 2024-05-20 at 2.19.02 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-05-20 at 2.24.42 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-05-20 at 2.36.44 pm.png" alt=""><figcaption></figcaption></figure>

## 2. Defining and Using Classes

**Static vs. Non-Static Methods**

**Static Methods**

```java
public class Dog {
    public static void makeNoise() {
        System.out.println("Bark!");
    }
}
public class DogLauncher {
    public static void main(String[] args) {
        Dog.makeNoise();
    }
}
```

**Instance Variables and Object Instantiation**

\








