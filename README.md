# EXPERIMENT 14
# AIM
To study and implement inheritance 
# THEORY
A key concept in object-oriented programming in C++ is inheritance, which enables a class to inherit properties and features from another class. This establishes a hierarchical link between classes and promotes reusing of code.

1. Key Concepts:
* Base Class (Parent Class) : The class from which properties and methods are inherited. It is also called the parent or superclass. <BR>
* Derived Class (Child Class) : The class that inherits the properties and methods from the base class. It can add new members or modify the inherited ones. <BR>

2. Access Specifiers in Inheritance:

* Public Inheritance (: public):
  * Public members of the base class become public in the derived class.
  * Protected members remain protected.
  * Private members are inaccessible directly but can be accessed through public/protected functions.

* Protected Inheritance (: protected):
  * Public and protected members of the base class become protected in the derived class.

* Private Inheritance (: private):
  * Public and protected members of the base class become private in the derived class.
