# Stacks

Stacks are a data structure that allow you to organize and access data in a specific way. The idea of a stack is a fundamental, abstract concept that is applicable all programming languages and even things unrelated to programming. Uncouple it from programming and think of it as a way of organizing things.



---



A stack is defined as a linear data structure that has a first in, last out (FILO). The two fundamental operations are:

- **push**, which adds an element to the collection 

- **pop**, which removes the **most recently added element** that has not yet been removed

  

Similar to how lunch trays are stacked in your cafeteria, you're only allowed to add to the top of the stack, or remove from the top of the stack. The power of stacks (and queues) is that they allow for very efficient insertion and deletion of elements.



---



### Why lists?

Stacks can be implemented any number of ways include Java's arrays, arraylists and Python's lists, collections.deque, and queue.LifoQueue. So, yes, when it comes to Python there are modules that implement a stack for you. In fact, their implementation is probably better than what we can do using a list. However, implementing a stack using Python's list allows us to focus on learning the properties of a stack, rather than the implementation details of a stack.



Basically, even though we could and should use Python's standard library for stacks rather than implementing them ourselves, we still need to understand what's going on in the background. 



### Why not lists?

Python's list is actually a dynamic array in the background. Python reserves some amount of memory for the array and while the list is less then the length of the array, everything is fine. When the list starts growing in size, Python needs to do some memory allocations which eventually lead to some .append() calls taking much longer than others.

The collections.deque module implements stacks as a doubly linked list. The main take away from that word-vomit sentence is that adding/removing elements from either end of the list takes constant time, O(1). 

Whereas with arrays, adding/removing elements takes linear time, O(n). This assumes you're using a fixed size array, which Python is using in the background as a list. The reason for this is because if you try to insert or delete something in the middle of the array, you would have to shift all the elements accordingly. If you have n elements after the middle, you would need to do n operations. 



![img](https://lh6.googleusercontent.com/DlcuCURArfoVOcwpl9cuZZjCVZeUkq0R74CpONmbY5gc57b9qJiV9wBr6gtghs_qqEEkmdcoBwMJoG27pqCEJXVEwACaKYi88HGpunhNLZkIyPBbg0i2D_pg1LuXYYdCkxo8DL3f)



---



### Stack Operations

- Push
  - Adds an element to the top of the stack
  - In the context of Python lists, **stack.append()** works as a push operation
- Pop
  - Removes the element at the top of the stack, and returns it
  - In the context of Python lists, **stack.pop()**



Quality of Life operations

- Peek

  - Returns the element at the top of the stack, without removing it

- isEmpty()

  - Returns true/false if stack is empty

  - Called before trying to add or remove an element

    