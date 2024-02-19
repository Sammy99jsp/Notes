- *How* is memory managed?
- *Who* is responsible for this?

For example, look at the following code:
```java
BigClass x = new BigClass(1); // (1)
x = new BigClass(2);          // (2)
// x is now refering to (2).
// But what happens to (1)?
```

After the reassignment, the first `BigClassed` value has no references to it, or more succinctly 'garbage' — that memory could be used for something else!

We can't just leave things willy-nilly in memory without cleaning it up. So, how do we solve this?

### 1. Garbage Collection (GC)
A garbage collector (GC) is code that's usually part of a language's runtime (shipped with compiled code). GC's will occasionally search through memory for inaccessible memory and clean it up.

Often, the GC will have to stop executing the normal code in order to clean the memory, as the code can't keep running if the GC moves things around.

Languages that use this approach include JavaScript, Python, Java, Go, etc.
### 2. Manual Memory Management (MMM)
These languages expect *you (yes, **you!**)* to remember to allocate and deallocate memory yourself. These languages include C, C++, Rust*.

For example, here's some well-written memory management in C:
```c
void* my_memory_p = malloc(12); // 1. Allocate 12 Bytes of Heap memory
free(my_memory_p); // 2. Deallocate those 12 bytes of memory.
```

However, in practice, the `malloc` and `free` may be thousands of lines apart, so sometimes you get (A) memory leaks, or (B) invalid memory access (use after `free`):

(A) Memory Leak:
```c
{
  void* my_memory_p = malloc(12); // 1. Allocate 12 Bytes of Heap memory
}

// Can't access the pointer now, cannot `free`.
// Those 12 bytes can never be deallocated by us now.
```

(B) Use after `free`.
```c
void* my_memory_p = malloc(12); // 1. Allocate 12 Bytes of Heap memory
free(my_memory_p);
*my_memory_p = (void*)"I am a chr*"; // Bang! Memory violation! We can't use it after free!
```

### Advantages and Disadvantages
#### GC
+ + Don't have to worry about managing memory yourself.
+ + Easier to write code that will work
+ - Performance impacts from the GC.
+ - May encourage wasteful allocation.

GC can be problematic in systems that are real-time (such as flight control systems) — often, they have to stop execution completely "stop the world" in order to do its work. In multi-threaded environments, sometimes *all the threads* need to stop for the GC to do its work. There have been many different iterations of GC (such as concurrent GC, where a separate thread is dedicated to GC), but there are problems with these, like cache misses.
#### Manual Memory Management
- + You can optimise your code to run quicker.
- - So many bugs by leaving it in the programmer's hands.
### Reading/Writing from an array/vector
Consider the line:
```python
a[n] = 24;
```
Where `n`  is greater than the size of the vector. Some languages check to see if there are within the bounds, some don't.

- The range checking slows the performance of the lookup/write operation.
- But, it does ensure that it is safe — this is a trade-off.
