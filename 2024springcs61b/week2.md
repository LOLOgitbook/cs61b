# week2

<figure><img src="../.gitbook/assets/Screenshot 2024-05-22 at 4.54.32 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

static: generally to all dogs

non-static method: specific to one dog

## 2. Defining and Using Classes

classes can be instantiated, and instances can hold data.\


Some key observations and terminology:

* An `Object` in Java is an instance of any class.
* The `Dog` class has its own variables, also known as _instance variables_ or _non-static variables_. These must be declared inside the class, unlike languages like Python or Matlab, where new variables can be added at runtime.
* The method that we created in the `Dog` class did not have the `static` keyword. We call such methods _instance methods_ or _non-static methods_.
* To call the `makeNoise` method, we had to first _instantiate_ a `Dog` using the `new` keyword, and then make a specific `Dog` bark. In other words, we called `d.makeNoise()` instead of `Dog.makeNoise()`.
* Once an object has been instantiated, it can be _assigned_ to a _declared_ variable of the appropriate type, e.g. `d = new Dog();`
* Variables and methods of a class are also called _members_ of a class.
* Members of a class are accessed using _dot notation_.

**Array Instantiation, Arrays of Objects**

new is used in two different ways: Once to create an array that can hold two `Dog` objects, and twice to create each actual `Dog`.

**Class Methods vs. Instance Methods**\
Instance methods are actions that can be taken only by a specific instance of a class. Static methods are actions that are taken by the class itself.

&#x20;

\
**public static void main(String\[] args)**

* `public`: So far, all of our methods start with this keyword.
* `static`: It is a static method, not associated with any particular instance.
* `void`: It has no return type.
* `main`: This is the name of the method.
* `String[] args`: This is a parameter that is passed to the main method.

\




