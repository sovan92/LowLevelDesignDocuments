
## SOLID
- Single Responsibility - Each class should have a single responsibility. 
- Open Close Principle - Class should be open for extension and close for modification. 
- Liskov Substitution Principle - Objects of super class can be replaced with objects of subsclass without breaking the system. 
- Interface Segregation Principle - Interfaces may not have methods that it shouldn't use. 
- Dependency Inversion Principle - High level modules like interfaces shouldn't depend on low level modules.


### Explanation of Liskrov substitution principle. 


* Liskorv Substitution principle deals with class and extends. So if we have a method in the base class, that should always be applicable in the subclasses as well. 

```mermaid

---
title: Violation of Liskov Substitution principle
---

classDiagram
  class Vehicle
  Vehicle:+startEngine()
  Vehicle <|-- Car
  Vehicle <|-- Bike
  class Car
  Car:+startEngine()

  class Bike
  Bike:+startEngine()
```

```mermaid
---
title: Fixing liskorv Substitution Principle. 
---

classDiagram
  class Vehicle
  Vehicle <|-- VehicleWithEngine
  Vehicle <|-- VehicleWithoutEngine

  class VehicleWithEngine
  VehicleWithEngine:+startEngine()
  VehicleWithEngine <|-- Car
  
  class VehicleWithoutEngine
  VehicleWithoutEngine:+moveVehicle()
  VehicleWithoutEngine <|-- Bike
  
  class Car
  Car:+startEngine()

  class Bike
  Bike:+moveVehicle()

```
### Explanation of Interface segregation principle . 

```mermaid
---
title: Interface segaregation principle problem. 
---

classDiagram
  interface Shape
  Shape:+area()
  Shape <|-- Square
  Shape <|-- Rectangle
  Shape <|-- Cube
  

  interface Square
  Square:+area()
  
  interface Rectangle 
  Rectangle:+area()
  
  interface Cube
  Cube:+area()
```


