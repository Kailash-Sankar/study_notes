# Python Notes

* List Comprehension
  - Multi line code in a single line.
  - Eg: list_element = `[x for x in range(1,10) if x%2 ==0 ]`
* Parameters
  - \*args
    - Captures all the positional arguments on a function definition (tuple).
  - \*\*kwargs
    - Captures all the keyword arguments (can access as a dictonary)
  - Python uses call by Object
    - Call by value & Call by reference
    - Call by object & Call by object reference
* lang
  - Interpreter
  - Dynamic typing
    - Python support dynamic typing
    - set s = ‘abc’; later we can define s=3 (variable is defined as a string and later changed to number).
    - Variable type is defined when its assigned and can change dynamically
  - functions are first-class objects
* list vs tuple
    - Mutable vs immutable
    - Tuple is a bit faster because it’s like a constant with defined number of objects.
* Using Tuple as key
  - Key can be any immutable object (number, string). Since a tuple has immutable elements it can be a dict key.
* Class
  ```
  class MyClass:
    def method(self):
        return 'instance method called', self

    @classmethod
    def classmethod(cls):
        return 'class method called', cls

    @staticmethod
    def staticmethod():
        return 'static method called'
        ```
  - Instance methods
    - first method in the above example
    - self points to an instance of the class
    - can modify object state using `self` and class state using `self.__class__`
  - Class methods
    - defined by decorator @classmethod
    - cls points to the class and not the object instance
    - cannot modify object state
    - Usually used as factory method(create class object)
  - Static methods
    - define using decorator @staticmethod
    - does not accept self or cls
    - cannot modify class or object state
  - dunder methods
  - @property(getter,setter)
    - makes a function accesible as a class property
    - we can define @property.getter and @property.setter on it
  - Inheritance
    - method resolution order(MRO)
    - super
  - Monkey Patching
    - modifying a function during runtime
  - `__mro__` : method resolution order
    - the order in which methods are resolved against classes, inherited order
* Regex (import re):
  - `re.search(‘<pattern>’, <string>, flag(eg: re.IGNORECASE) )` : searches entire string and returns first match.
  - `re.match(‘<pattern>’, <string>, flag(eg: re.IGNORECASE) )` : matches from begining.
  - `findall(<pattern>, <string>, flag)` : find all the matches and return as a list/tuple.
  - `re.sub(<pattern>, <sub_string>, <string_variable>, <count>, flag)` : substitutes all the occurance of string with sub_string. Returns the substituted string.
    - If count = 0 or not defined, then replaces all occurance, if 1 then replaces first occurrence.
  - `re.subn(<pattern>, <sub_string>, <string_variable>, <count>, flag)` : same as substitute, along with the string this will return number of substitute as tuple.
  - `re.split(<pattern>, <string>)` : splits the string with pattern and returns list.
* join
  - `‘ ’.join(<list/tuple>)` : joins the list elements and creates a string.
* Map
  - Syntax map(function, iterable): apply a function on all the elements of an iterable and returns a list.
  - `out = map((lambda x: x*x), range(10))`
* Filter
  - Syntax filter(function, iterable): apply function on all the elements of an iterable and returns the element if true. Returns list.
  - `out = filter((lambda x: x %2 == 0), range(11))`
* Zip
  - combines two lists in to a zipped list of tuples
* Reduce
  - use functools.reduce, similar to map/filter but reduces input to a single value
* File Handling
  - `fh = open(<file_name>, <open_mode>)`, mode can be ‘r’, ‘w’, ‘a’ etc etc.
  - `fh.read()` : read all the lines of a file(till the end) or read(4) will read 4 chars.
  - `fh.write(<str>)` : writes to the file.
  - `fh.readline()` : read a single line(until “\n”)
  - `fh.readlines()` : read all the lines of a file and returns a list with each line as a list elements.
  - `fh.seek()` : bring cursor to a position. seek(0) will bring to begining.
  - `fh.tell()` : returns current position of cursor.
  - `fh.close()` : to close the file.
  - for traversing we can also use `for line in fh`
  - With open(<file_name>) as f:
    - When using with, we don't need to close the file, it will do so automatically even if any exception occurs.
* Iterator
  - An object that can be iterated.
  - `__iter__` returns iterator object.
  - `__next__` returns next item in the sequence.
  - If there's no next item, then returns StopIteration exception.
* Generator
  - A way of creating iterator. Returns an iterator object.
  - Using yield keyword to implement generator. yield statement returns a value and pauses the function there)
  - No need to implement __iter__() or __next__(), StopIteration. They are implemented automatically
  - Generator expression `x**x for x in <list>`
  - Similar to  list comprehension but not processing all the elements at a time but returns a generator object.
  - Easy to implement (no need to define iter, next etc) and memory efficient.
  - Represent infinite stream of data (to create large stream of data but it returns one at a time so efficient)
* Enumerate
  - Enumerate adds a counter to the iterator an iterable.
  - `for count, item in enumerate(list_obj)`
* Decorator
  - Decorator is a function that take another function and extends the behavior of the latter function.
* Namespaces and Scope
* Lambda
  - used for creating small, one-time and anonymous function objects in Python
  - `lambda x: x**x`
* With keyword:
  - used when working with unmanaged resources (like file streams)
  - `with open(<filename>) as fh`
  - It ensure, clean code is executed(try except is not required.
  - For  a file operation, we don’t need to close file.
* Closure
  - Similar to javascript closure.
  - When to use: It provides a way to hide data and we can avoid use of global variable.
* Exception Handling
  - try - run a code block
  - except - capture exception
  - else - gets executed if try is run successfully
  - finally - always executed at the end
  - custom exceptions can be defined
* Context managers
  - `__enter__`
  - `__exit__`
* Multi threading
  - Achieved by threading module in python3
  - Operations
    - `lock = threading.Lock()` Create a lock, Semaphore to avoid synchronization issue.
    - `lock.acquire()` : This will get the lock for a thread and then thread can execute.
    - `lock.release()` : Once thread is executed, then lock should release so that other thread can start execution.
    - `t1 = threading.Thread(target=<function to execute>, name=<name>, args=(args))` : Create a thread
    - `t1.start()` : To start a thread.
    - `t1.join()` : this will execute thread(t1) first, then it will execute the main program.
* Multiprocesing
* GIL (Global Interpreter Lock)
* Random
  - shuffle, randint, randrange, choice
* More
  - assert
  - repr(!r) and str(!s)
  - pass
  - collections.namedtuples
  - copy and deepcopy
  - Pickling and Unpickling
    - converting objects in to string and parsing them back
  - Memory
    - All Python objects and data structures are located in a private heap
    - memory manager handles the allocation of heap space
    - garbage collector recycles all the unused memory and so that it can be made available to the heap space
* Guide
  - PyChecker - static analysis, finding bugs
  - Pylint
  - PEP8 - coding convention
  - import this -  Zen of Python
* Qs
  - list vs tuple
* Links
  - https://realpython.com/instance-class-and-static-methods-demystified/
  - https://www.journaldev.com/14893/python-property-decorator
  - https://www.programiz.com/python-programming/args-and-kwargs
  - https://www.python-course.eu/passing_arguments.php
