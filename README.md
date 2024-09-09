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

3. Types of Inheritance : <br>

  * Single Inheritance
A derived class inherits from only one base class. <BR>
```
lass Base {
    // Base class members
};

class Derived : public Base {
    // Derived class members
};
```

  *  Multiple Inheritance
A derived class inherits from more than one base class. <BR>
```
class Base1 {
    // Base1 class members
};

class Base2 {
    // Base2 class members
};

class Derived : public Base1, public Base2 {
    // Derived class members
};
```

  * Multilevel Inheritance
A class is derived from a class that is also derived from another class, forming a chain. <BR>
```
class Base {
    // Base class members
};

class Intermediate : public Base {
    // Intermediate class members
};

class Derived : public Intermediate {
    // Derived class members
};
```

  * Hierarchical Inheritance
Multiple derived classes inherit from a single base class.
```
class Base {
    // Base class members
};

class Derived1 : public Base {
    // Derived1 class members
};

class Derived2 : public Base {
    // Derived2 class members
}
```

# CODE & OUTPUT 
1. CODE A
```
//SARA KANYAL
//23070123115
//SINGLE INHERITANCE
# include <iostream>
# include <string>
using namespace std;
class Uni{
    public:
    string uni= "Symbiosis";
    void discipline(){
        cout << "Engineering" << endl;
    }
};
class Dep : public Uni{
    public:
    string dept= " Electronics & Telecommunication";
};
int main(){
    Dep u1;
    u1.discipline();
    cout<<u1.uni + " "+u1.dept ;
}
```
 * OUTPUT A 
![14A](https://github.com/sarakanyal03/CDS_Experiment14/blob/main/A.png)

2. CODE B
```
//SARA KANYAL
//23070123115
//MULTIPLE INHERITANCE
# include <iostream>
# include <string>
using namespace std;
// Parent CLass1 
class Vehicle {
    public:
    string company=" Ford";
    void type(){
        cout << "Mustang"<< endl;
    }
};
// Parent Class 2
class Specs{
    public:
    string mileage="8 kmpl";
    void colour(){
        cout<<"Grey"<<endl;
    }
};
// Child Class-1 (derived from parent- 1&2)
class Car: public Vehicle,public Specs{
    public:
    string seater = " 4 seater";
};
int main(){
    //multiple inheritance
    Car f2;
    f2.colour();
    cout<<f2.company<<" ";
    f2.type();
    cout<<"("<<f2.seater<<")"<<endl<<"MILEAGE:"<<f2.mileage<<endl;
}
```
 * OUTPUT B
![14B](https://github.com/sarakanyal03/CDS_Experiment14/blob/main/B.png)

3. CODE C
```
//SARA KANYAL
//23070123115
//MULTILEVEL INHERITANCE
#include <iostream>
using namespace std;

// Parent class (Level 1)
class Animal {
public:
    void eat() {
        cout << "Animal is eating." << endl;
    }
};

// Derived class 1  inheriting from Animal
class Mammal : public Animal {
public:
    void walk() {
        cout << "Mammal is walking." << endl;
    }
};

//  derived class 2 inheriting from Mammal
class Dog : public Mammal {
public:
    void bark() {
        cout << "Dog is barking." << endl;
    }
};

int main() {
    Dog f1;
    
    // Dog class can access functions of Animal and Mammal classes
    f1.eat();   // Inherited from Animal
    f1.walk();  // Inherited from Mammal
    f1.bark();  // Function of Dog class
    
    return 0;
}

```
 * OUTPUT C
![14C](https://github.com/sarakanyal03/CDS_Experiment14/blob/main/C.png)

4. CODE D
```
//SARA KANYAL
//23070123115
// HIERARCHIAL INHERITANCE
#include <iostream>
using namespace std;

// Base class
class Animal {
public:
    void eat() {
        cout << "Eating " << endl;
    }
};

// Derived class 1
class Dog : public Animal {
public:
    void bark() {
        cout << "Barking " << endl;
    }
};

// Derived class 2
class Cat : public Animal {
public:
    void meow() {
        cout << "Meowing " << endl;
    }
};

int main() {
    // Creating an object of Dog
    Dog dog;
    dog.eat();   // Calling the base class function
    dog.bark();  // Calling the derived class function

    // Creating an object of Cat
    Cat cat;
    cat.eat();   // Calling the base class function
    cat.meow();  // Calling the derived class function

    return 0;
}
```
 * OUTPUT D
![14AD](https://github.com/sarakanyal03/CDS_Experiment14/blob/main/D.png)

# CONCLUSION

A useful object-oriented programming (OOP) technique in C++ is inheritance, which lets a class (also referred to as a derived class) inherit traits and actions (data members and member functions) from another class (referred to as the base class). It encourages flexibility, hierarchical relationships between classes, and reusing code. <BR>
  By extending the functionality of existing classes through inheritance, programmers can create more specialized classes and simplify the maintenance and updating of the code. In C++, inheritance comes in a variety of forms that can be used to meet different design requirements. These include single, multiple, multilevel, hierarchical, and hybrid inheritance.
