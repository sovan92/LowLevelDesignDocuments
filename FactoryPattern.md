# FactoryPattern 
A factory pattern provides ways to instanciate classes without using new. 

## SimpleFactoryPattern
```mermaid
---
title: Simple Factory Pattern
---


classDiagram
    
    PizzaFactory<|--SimplePizzaFactory
    PizzaStore -- PizzaFactory

    class PizzaStore {
        +PizzaFactory factory
    }
    class PizzaFactory {
        + createPizza()
    }
    
    class SimplePizzaFactory{

    }
```



## FactoryMethodPattern

```mermaid

classDiagram
    direction LR

    class Product {
        <<abstract>>
        +createProduct()
    }
    class ConcreteProductA {
        +createProduct()
    }
    class ConcreteProductB {
        +createProduct()
    }
    class Creator {
        <<abstract>>
        +factoryMethod() Product
    }
    class ConcreteCreatorA {
        +factoryMethod() Product
    }
    class ConcreteCreatorB {
        +factoryMethod() Product
    }

    Creator <|-- ConcreteCreatorA
    Creator <|-- ConcreteCreatorB

    Creator --> Product : creates >

    Product <|-- ConcreteProductA
    Product <|-- ConcreteProductB

    ConcreteCreatorA ..> ConcreteProductA : creates
    ConcreteCreatorB ..> ConcreteProductB : creates


```
