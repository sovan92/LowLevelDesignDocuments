# FactoryPattern 
A factory pattern provides ways to instanciate classes without using new. 

## SimpleFactoryPattern

```mermaid

class PizzaStore:
  PizzaStore : -PizzaFactory pizzafactory
  PizzaStore : +orderPizza()

class PizzaFactory:
  PizzaFactory : +createPizza()
  

class SimplePizzaFactory:
  SimplePizzaFactory : + createPizza()

PizzaFactory <|-- SimplePizzaFactory
```


## FactoryMethodPattern
