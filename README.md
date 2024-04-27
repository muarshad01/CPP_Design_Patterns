# Design Patterns

[CPP Design Patterns](https://refactoring.guru/design-patterns/cpp)

***

## Creational Design Patterns (AB---FPS)

* [Abstract Factory](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/abstract_factory)
* [Builder](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/builder)
* [Factory Method](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/factory_method)
* [Prototype](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/prototype)
* [Singleton](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Creational_Patterns/singleton)

***

## Structural Design Patterns (ABCD-F2-P)

* [Adapter](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/adapter)
* [Bridge](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/bridge)
* [Composite](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/composite)
* [Decorator](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/decorator)
* [Facade](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/facade)
* [Flyweight](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/flyweight)
* [Proxy](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Structural_Patterns/proxy)

***

## Behavioral Design Patterns (C2-I-M2-O-S2-TV)

* [Chain of Responsibility](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/chain_of_responsibility)
* [Command](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/command)
* [Iterator](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/iterator)
* [Memento](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/memento)
* [Mediator](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/mediator)
* [Observer](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/observer)
* [Strategy](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/strategy)
* [State](https://github.com/muarshad01/CPP_Design_Patterns/tree/main/Behavioral_Patterns/state)
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
* `main.cpp` -> Terminal -> `Run Build Task` (shift + command + b)
  ```
  C/C++: g++ build active file
  compiler: /usr/bin/g++
  ```
* `main` -> Right-click -> `Open in Integrated Terminal`
* `$ ./main`

***

### Object Creation
```c++
Myclass *object = new Myclass();  //object has dynamic   storage duration (usually is on the heap)
Myclass object;                   //object has automatic storage duration (usually is on the stack)
```
* You create objects with `dynamic storage duration (usually on the heap) if you plan on using them throughout a long period of time` and you create objects with `automatic storage duration (usually on the stack) for a short lifetime (or scope)`.
* In fact, `when creating an object with new`, you always have to remember destroying it with `delete object`

  ## Multiple Inheritance
  * `class A : public B, public C`
