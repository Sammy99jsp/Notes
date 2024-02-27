What happens when you want to call a method `a.foo()`?
Well, it depends...

- Sometimes, this is static (when only one class implements that method)
- Or, it's at runtime — this is where it gets interesting.
## Static Lookup
Here, the method `a.foo()` is looked up at runtime:
- The compiler knows the type of `a`
- It can then find the appropriate method at compile-time.

This approach is as fast as calling a (pure) function.
## Dynamic Lookup
Sometimes, the type of a value can change: imagine the following:
```java
Dog dingo = new Dog();
Animal myDog = (Animal)dingo;
```
What happens if you have two classes:
```java
interface Animal {
    void makeNoise();
}

class Cat implements Animal {
    @Override
    void makeNoise() {
        System.out.prinln("Meow");
    }
}

class Dog implements Animal {
    @Override
    void makeNoise() {
        System.out.prinln("Woof");
    }
}
```

And you want to do this:
```java
void petAnimal(Animal pet) {
    pet.makeNoise(); // <-- Here
}
```
We can't determine which implementing class' (either `Cat` or `Dog`) method to call ahead of time: the compiler does not know this information at compile-time!

So, that means at runtime, the method `makeNoise()` will need to be looked up for `pet` (either the `Dog`, or the `Cat`'s implementation), which leads it to be much slower.

This allows for the layers of abstraction and hierarchy that OOP programmers are used to.
### Duck Typing
This is a highly-dynamic kind of typing.

*Examples*: JavaScript, Python, Ruby, Common Lisp

When you evaluate `a.foo()`, this is only done when it's evaluated — this means that the type of `a` itself can change during the course of the programming.