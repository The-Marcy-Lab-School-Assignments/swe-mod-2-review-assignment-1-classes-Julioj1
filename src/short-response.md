# Short Response

## Question 1

For each scenario, identify whether the relationship is **inheritance** or **composition**, and provide a brief explanation.

For example, a `Song` and a `MediaItem` have an inheritance relationship because "a song is a type of media item". Meanwhile a team and player have a composition relationship because "a team has many players".

1. A `Car` class and an `Engine` class, where a car contains an engine
2. A `Dog` class and an `Animal` class, where a dog is a type of animal
3. A `Classroom` class and a `Student` class, where a classroom contains multiple students
4. A `Rectangle` class and a `Shape` class, where a rectangle is a type of shape
5. A `Computer` class and a `CPU` class, where a computer contains a CPU
6. A `Manager` class and an `Employee` class, where a manager is a type of employee

### Response 1

1. **Composition** — A `Car` has an `Engine`. The engine is a component of the car, not a type of car.
2. **Inheritance** — A `Dog` is an `Animal`, so it makes sense for `Dog` to inherit from `Animal`.
3. **Composition** — A `Classroom` has many `Students`. Students exist independently of the classroom.
4. **Inheritance** — A `Rectangle` is a `Shape`, so it should extend the `Shape` class.
5. **Composition** — A `Computer` has a `CPU`. The CPU is a part of the computer, not a kind of computer.
6. **Inheritance** — A `Manager` is an `Employee`, with additional responsibilities or behaviors.

---

## Question 2

In Problem 1, you are asked to implement a `Song`, `Podcast`, and `Audiobook` classes that all extend the `MediaItem` base class. Each class has their own `play()` method. This demonstrates **polymorphism**.

In your own words, explain what polymorphism means and why it is useful. Use the `MediaItem` example from this assignment to support your explanation.

### Response 2

**Polymorphism** means that different objects can share the same method name but behave in different ways. In other words, the same method call can produce different results depending on which class the object belongs to.

In the `MediaItem` example, `Song`, `Podcast`, and `Audiobook` all extend the `MediaItem` base class and each implements its own version of the `play()` method. Even though they all respond to `play()`, a song might play music, a podcast might play an episode, and an audiobook might play a chapter. This allows us to treat all of them as `MediaItems` while still getting behavior that is specific to each type.

**Polymorphism** is useful because it makes code more flexible and easier to extend. For example, we can store different media items in a single array and call `play()` on each one without needing to check its type. If a new media type is added later, it can implement its own `play()` method and work with the existing code without changes.

---

## Question 3

In JavaScript classes, properties and methods can be either **instance-level** or **static**.

a) What is the difference between an instance property and a static property?

b) Give an example of when you would want to use a static property or method instead of an instance property or method.

### Response 3

a) An instance property **belongs to a specific object** created from a class. Each instance has its own copy of that property, and it is accessed using the `this` keyword. Changes to an instance property only affect that one object.

A static property **belongs to the class itself**, not to any individual instance. It is shared across all instances and is accessed directly on the class, not with the `this` keyword.

b) You would use a static property or method when the data or behavior is related to the class as a whole, not to a single instance.

Example:
If you have a User class and you want to keep track of how many users have been created, a static property makes sense because the count should be shared across all users.
