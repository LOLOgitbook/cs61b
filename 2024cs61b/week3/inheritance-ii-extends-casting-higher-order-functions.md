# Inheritance II: Extends, Casting, Higher Order Functions

implement: 用于interface

&#x20;extend : 用于class



Great question! Here’s the clean mental model:

## Comparable vs Comparator

**Comparable**

* **Where defined:** _Inside the class itself_ (`class Dog implements Comparable<Dog>`).
* **Purpose:** Gives the type a single **natural order**.
* **Method:** `int compareTo(T o)`
* **How used:** Libraries use it when **no comparator is supplied** (e.g., `Collections.sort(list)`, `Collections.max(list)`, `TreeSet`/`TreeMap` default).
* **How many orders:** **One** per class (you can encode tie-breakers, but still one canonical order).
* **Generic form:** `Comparable<T>`
*   **Example:**

    ```java
    class Dog implements Comparable<Dog> {
        int size; String name;
        @Override public int compareTo(Dog o) {
            int c = Integer.compare(this.size, o.size);
            return (c != 0) ? c : this.name.compareTo(o.name);
        }
    }
    ```

**Comparator**

* **Where defined:** _Outside the class_ (pass at the call site).
* **Purpose:** Provides **alternate/context-specific** orderings.
* **Method:** `int compare(T a, T b)`
* **How used:** Supply to algorithms/collections that accept a comparator (e.g., `list.sort(cmp)`, `Collections.max(list, cmp)`, `new TreeSet<>(cmp)`).
* **How many orders:** **Many**—define as many comparators as you need.
* **Generic form:** `Comparator<? super T>` (consumer → **super**)
*   **Example:**

    ```java
    Comparator<Dog> byName = Comparator.comparing(Dog::getName);
    Comparator<Dog> bySizeDescThenName =
        Comparator.comparingInt(Dog::getSize).reversed()
                  .thenComparing(Dog::getName);
    dogs.sort(bySizeDescThenName);
    ```

### When to use which?

* Use **Comparable** if the type has one obvious, canonical ordering (e.g., numbers, dates, strings).
* Use **Comparator** when:
  * You can’t/shouldn’t modify the class, or
  * You need multiple different orderings (by size, by name, by name length…).

### Gotchas & tips

* Prefer `Integer.compare(a,b)` over `a - b` to avoid overflow.
* If `x.compareTo(y) == 0`, it’s **strongly recommended** that `x.equals(y)` is `true` (important for `TreeSet/TreeMap`).
* In ordered collections built with a **Comparator**, “equality” is determined by `compare(a,b) == 0`, not `equals`.
* Helpful builders: `Comparator.comparing(...)`, `.comparingInt(...)`, `.thenComparing(...)`, `.reversed()`, `Comparator.nullsFirst/Last(...)`, `Comparator.naturalOrder()`.

**TL;DR:**

* **Comparable** = one built-in “natural” order defined by the class.
* **Comparator** = plug-in strategies you choose at use time; have as many as you like.



