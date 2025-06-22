# FactoryPattern 
A factory pattern provides ways to instanciate classes without using new. 

## SimpleFactoryPattern

```mermaid
classDiagram
  class PizzaStore:
    PizzaStore : -PizzaFactory pizzafactory
    PizzaStore : +orderPizza()
  
  class PizzaFactory:
    PizzaFactory : +createPizza()
    PizzaFactory <|-- SimplePizzaFactory
    
  
  class SimplePizzaFactory:
    SimplePizzaFactory : + createPizza()
  
  
```


## FactoryMethodPattern
