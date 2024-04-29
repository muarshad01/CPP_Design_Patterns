# Design Patterns

[CPP Design Patterns](https://refactoring.guru/design-patterns/cpp)

***

## Creational Design Patterns (AB---FPS)

* [Abstract Factory](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/abstract_factory) -- April 28, 2024
* [Builder](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/builder) -- April 28, 2024
* [Factory Method](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/factory_method) -- April 28, 2024
* [Prototype](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/prototype) -- April 27, 2024
* [Singleton](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/singleton) -- April 28, 2024

***

## Structural Design Patterns (ABCD-F2-P)

* [Adapter](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/adapter) -- April 27, 2024
* [Bridge](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/bridge) -- April 27, 2024
* [Composite](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/composite) -- April 27, 2024
* [Decorator](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/decorator) -- April 27, 2024
* [Facade](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/facade) -- April 27, 2024
* [Flyweight](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/flyweight) -- April 28, 2024
* [Proxy](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/proxy) -- April 27, 2024

***

## Behavioral Design Patterns (C2-I-M2-O-S2-TV)

* [Chain of Responsibility](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/chain_of_responsibility) -- April 28, 2024
* [Command](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/command)
* [Iterator](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/iterator) -- April 28, 2024
* [Memento](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/memento)
* [Mediator](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/mediator)
* [Observer](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/observer)
* [Strategy](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/strategy)
* [State](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/state) -- April 28, 2024
* [Template](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/template_method)
* [Visitor](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/visitor)

***

## Intentation

* How to remove "2" spaces and make it to default "Tab (4)" space
```
1. Go to: settings > workspace settings > Text editor
2. uncheck 'Detect Indentation' to stick to your default setting.
3. Then restart the application.
```

## Format Code
* `command A`
* `shift + option + F`
  
***

## Run the Code
#### Run the Code through VSCode Editor

* `main.cpp` -> Terminal -> `Run Build Task` (shift + command + b) then select:
  ```
  C/C++: g++ build active file
  compiler: /usr/bin/g++
  ```
* `main` -> Right-click -> `Open in Integrated Terminal`
* `$ ./main`

***

#### Run the code through Command Line

```
$ g++ --std=c++17 main.cc
$ ./a.out
```
***

## C++ Example Code Explanation

### Object Creation
```c++
Myclass *object = new Myclass();  //object has dynamic   storage duration (usually is on the heap)
Myclass object;                   //object has automatic storage duration (usually is on the stack)
```
* You create objects with `dynamic storage duration (usually on the heap) if you plan on using them throughout a long period of time` and you create objects with `automatic storage duration (usually on the stack) for a short lifetime (or scope)`.
* In fact, `when creating an object with new`, you always have to remember destroying it with `delete object`

***

### Multiple Inheritance
```c++
class A : public B, public C`
{
  ...
};
```

***

### Virtual Destructor
```c++
#include <iostream>
 
using namespace std;
 
class base {
  public:
    base()     
    { cout << "Constructing base\n"; }
    virtual ~base()
    { cout << "Destructing base\n"; }     
};
 
class derived : public base {
  public:
    derived()     
    { cout << "Constructing derived\n"; }
    ~derived()
    { cout << "Destructing derived\n"; }
};
 
int main()
{
  derived *d = new derived();  
  base *b = d;
  delete b;
  getchar();
  return 0;
}
```

```c++
class Target
{
public:
  virtual ~Target() = default;
  ...
};
```
* Making base class destructor virtual guarantees that the object of derived class is destructed properly, i.e., both base class and derived class destructors are called.

***

### Pure Virtual Function
```c++
// C++ Program to illustrate the abstract class and virtual functions
#include <iostream>
using namespace std;
 
class Base {
    // private member variable
    int x;
 
public:
    // pure virtual function
    virtual void fun() = 0;
 
    // getter function to access x
    int getX() { return x; }
};
 
// This class inherits from Base and implements fun()
class Derived : public Base {
    // private member variable
    int y;
 
public:
    // implementation of the pure virtual function
    void fun() { cout << "fun() called"; }
};
 
int main(void)
{
    // creating an object of Derived class
    Derived d;
 
    // calling the fun() function of Derived class
    d.fun();
 
    return 0;
}
```
* A pure virtual function is implemented by classes that are derived from an Abstract class.

*** 
