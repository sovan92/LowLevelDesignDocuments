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

