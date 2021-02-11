# Python & Object-oriented programming
From: [Structuring Your Project — The Hitchhiker’s Guide to Python](https://docs.python-guide.org/writing/structure/)
Study and reword:

- - - -
* Python is sometimes described as an object-oriented programming language. This can be somewhat misleading and needs to be clarified.
* In Python, everything is an object, and can be handled as such. This is what is meant when we say, for example, that functions are first-class objects. Functions, classes, strings, and even types are objects in Python: like any object, they have a type, they can be passed as function arguments, and they may have methods and properties. In this understanding, Python is an object-oriented language.
* However, unlike Java, Python does not impose object-oriented programming as the main programming paradigm. It is perfectly viable for a Python project to not be object-oriented, i.e. to use no or very few class definitions, class inheritance, or any other mechanisms that are specific to object-oriented programming.
* Moreover, as seen in the  [modules](https://docs.python-guide.org/writing/structure/#modules)  section, the way Python handles modules and namespaces gives the developer a natural way to ensure the encapsulation and separation of abstraction layers, both being the most common reasons to use object-orientation. Therefore, Python programmers have more latitude to not use object-orientation, when it is not required by the business model.
* There are some reasons to avoid unnecessary object-orientation. Defining custom classes is useful when we want to glue together some state and some functionality. The problem, as pointed out by the discussions about functional programming, comes from the “state” part of the equation.
* In some architectures, typically web applications, multiple instances of Python processes are spawned to respond to external requests that can happen at the same time. In this case, holding some state in instantiated objects, which means keeping some static information about the world, is prone to concurrency problems or race conditions. Sometimes, between the initialization of the state of an object (usually done with the __init__() method) and the actual use of the object state through one of its methods, the world may have changed, and the retained state may be outdated. For example, a request may load an item in memory and mark it as read by a user. If another request requires the deletion of this item at the same time, it may happen that the deletion actually occurs after the first process loaded the item, and then we have to mark as read a deleted object.
* This and other issues led to the idea that using stateless functions is a better programming paradigm.
* Another way to say the same thing is to suggest using functions and procedures with as few implicit contexts and side-effects as possible. A function’s implicit context is made up of any of the global variables or items in the persistence layer that are accessed from within the function. Side-effects are the changes that a function makes to its implicit context. If a function saves or deletes data in a global variable or in the persistence layer, it is said to have a side-effect.
* Carefully isolating functions with context and side-effects from functions with logic (called pure functions) allow the following benefits:
* Pure functions are deterministic: given a fixed input, the output will always be the same.
* Pure functions are much easier to change or replace if they need to be refactored or optimized.
* Pure functions are easier to test with unit tests: There is less need for complex context setup and data cleaning afterwards.
* Pure functions are easier to manipulate, decorate, and pass around.
* In summary, pure functions are more efficient building blocks than classes and objects for some architectures because they have no context or side-effects.
* Obviously, object-orientation is useful and even necessary in many cases, for example when developing graphical desktop applications or games, where the things that are manipulated (windows, buttons, avatars, vehicles) have a relatively long life of their own in the computer’s memory.

#tk/code


