Python Magic Methods\
\
__new__ - first method called in object instation.\
__init__ - intializer for the class, gets passed whatever primary constructor was called with.\
__del__ - destructor, defines behavior when object is garbage collected. usefull for objects which require extra cleanup after deletion.\
\
__cmp__ - implements behavior for all comparison operators (< ,==, !=, etc.)\
__eq__ - define behaviour for the equality, ==.\
__ne__ - define behaviour for the inequality, !=.\
__lt__ - define behaviour for the less-than, <.\
__gt__ - define behaviour for the greater-than, >.\
__le__ - define behaviour for the less-than-or-equal, <=.\
__ge__ - define behaviour for the greater-than-or-equal, >=.\
\
__pos__ - implements behavior for unary positive (e.g. +some_object)\
__neg__ - implements behavior for negation (e.g. -some_object)\
__abs__ - implements behavior for the built in abs() function.\
__invert__ -implements behavior for inversion using the ~ operator.\
__round__ - implements behavior for the built in round() function. n is the number of decimal places to round to.\
__floor__ - implements behavior for math.floor(), i.e., rounding down to the nearest integer.\
__ceil__ - implements behavior for math.ceil(), i.e., rounding up to the nearest integer.\
__trunc__ - implements behavior for math.trunc(), i.e., truncating to an integral.\
\
__add__ - implements addition.\
__sub__ - implements subtraction.\
__mul__ - implements multiplication.\
__floordiv__ - implements integer division using the // operator.\
__div__ - implements division using the / operator.\
__truediv__ - implements true division.\
__mod__ - implements modulo using the % operator.\
__divmod__ - implements behavior for long division using the divmod() built in function.\
__pow__ - implements behavior for exponents using the ** operator.\
__lshift__ - implements left bitwise shift using the << operator.\
__rshift__ - implements right bitwise shift using the >> operator.\
__and__ - implements bitwise and using the & operator.\
__or__ - implements bitwise or using the | operator.\
__xor__ - implements bitwise xor using the ^ operator.\
\
__int__ - implements type conversion to int.\
__long__ - implements type conversion to long.\
__float__ - implements type conversion to float.\
__complex__ - implements type conversion to complex.\
__oct__ - implements type conversion to octal.\
__hex__ - implements type conversion to hexadecimal.\
__index__ - implements type conversion to an int when the object is used in a slice expression.\
__trunc__ - called when math.trunc(self) is called.\
__coerce__ - method to implement mixed mode arithmetic.\
\
__str__ - defines behavior for when str() is called on an instance of your class.\
__repr__ - defines behavior for when repr() is called on an instance of your class.\
__unicode__ - defines behavior for when unicode() is called on an instance of your class.\
__format__ - defines behavior for when an instance of your class is used in new-style string formatting.\
__hash__ - defines behavior for when hash() is called on an instance of your class.\
__nonzero__ - defines behavior for when bool() is called on an instance of your class.\
__dir__ - defines behavior for when dir() is called on an instance of your class.\
__sizeof__ - defines behavior for when sys.getsizeof() is called on an instance of your class.\
\
__getattr__ - you can define behavior for when a user attempts to access an attribute that doesn't exist (either at all or yet). This can be useful for catching and redirecting common misspellings, giving warnings about using deprecated attributes (you can still choose to compute and return that attribute, if you wish), or deftly handing an AttributeError.\
__setattr__ - unlike __getattr__, __setattr__ is an encapsulation solution. It allows you to define behavior for assignment to an attribute regardless of whether or not that attribute exists, meaning you can define custom rules for any changes in the values of attributes.\
__delattr__ - this is the exact same as __setattr__, but for deleting attributes instead of setting them.\
__getattribute__ - it allows you to define rules for whenever an attribute's value is accessed. It suffers from some similar infinite recursion problems as its partners-in-crime (this time you call the base class's __getattribute__ method to prevent this). It also mainly obviates the need for __getattr__, which, when __getattribute__ is implemented, only gets called if it is called explicitly or an AttributeError is raised.\
\
__enter__ - defines what the context manager should do at the beginning of the block created by the with statement.\
__exit__ - defines what the context manager should do after its block has been executed (or terminates). It can be used to handle exceptions, perform cleanup, or do something always done immediately after the action in the block.\
\
__call__ - allows an instance of a class to be called as a function. Essentially, this means that x() is the same as x.__call__().\
\
__len__ - returns the length of the container.\
__getitem__ - defines behavior for when an item is accessed, using the notation self[key].\
__setitem__ - defines behavior for when an item is assigned to, using the notation self[nkey] = value.\
__delitem__ - defines behavior for when an item is deleted (e.g. del self[key]). \
__iter__ - should return an iterator for the container.\
__reversed__ - called to implement behavior for the reversed() built in function.\
__contains__ - __contains__ defines behavior for membership tests using in and not in.\
__missing__ - __missing__ is used in subclasses of dict. It defines behavior for whenever a key is accessed that does not exist in a dictionary (so, for instance, if I had a dictionary d and said d["george"] when "george" is not a key in the dict, d.__missing__("george") would be called).\
