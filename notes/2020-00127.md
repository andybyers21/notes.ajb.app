---
layout: note
title: Constructors and Self
parent: Python
grand_parent: Home
---

# Constructors and Self

Remember, a class is a template for an object (Ref; [[Classes and Objects]]). You can create many objects, known as instances, from your class. Every time you create an object from a class it will create new [[Namespaces]] for that instance. A constructor is responsible for calculating that memory allocated to that instance (`()` is your constructor) which will call the `__init__` method for you. The constructor is called automatically every time you create a new instance.

Lets say you create two instances as follows and alter the data within one:

```py
# Create a class
class ContactBook
	def __init__(self):
		self.name = "Dave"
		self.age = 31


# Create instance objects
c1 = ContactBook()
c2 = ContactBook()
```

**Anything you define within an instance will be only accessible within that namespace.**

To access any attributes of the instance object, eg. `name` or `age`, you need to call the instance name, then the attribute to delineate those attributes that belong to the instance or otherwise:

```py
# Modify the data of c2 instance object
c2.name = "Ronald"
c2.age = 67
```

Instance objects are accessed in the same way

```py
print(c2.name)
# "Ronald"
```

Now add a new function to your class which will update all the names within an instance:

```py
class ContactBook
	def __init__(self):
		self.name = "Dave"
		self.age = 31

	def update(self):
		self.name = "Anonymous"
```

Then call the function

```py
c2.update()
```

When you call `update()`, the function within the class (the template) does not know which instance of `ContactBook` you are calling. By assigning `self` as the first argument you are telling the code to check which instance of `ContactBook` to refer to. You have told the code by prefixing `update()` with `c2.`

`self` is a pointer which lets python know to look for the object you are referring to. **The current instance**

_Whenever you see the word `self` in a class definition, self is referring to the particular instance you are working in._ When defined, `self` is passed automatically as the first argument of an instance. Any other arguments you pass will take up position 2 on so on.

**If you don't include `self` as the first parameterin any method definitions in a class then those methods wil only be avaliable through the class namespace - they won't have access to any instance attributes.**

---
