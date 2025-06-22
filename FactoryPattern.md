# FactoryPattern 
A factory pattern provides ways to instanciate classes without using new. 

## SimpleFactoryPattern
```mermaid
---
title: Simple Factory Pattern
---



classDiagram
    class PizzaStore
    PizzaStore : +SimplePizzaFactory owner
    PizzaStore --> PizzaFactory

    class PizzaFactory

    class SimplePizzaFactory
    PizzaFactory<|--SimplePizzaFactory

```

```mermaid


---
title: Animal example
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }


```

## FactoryMethodPattern
