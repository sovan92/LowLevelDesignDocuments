# FactoryPattern 
A factory pattern provides ways to instanciate classes without using new. 

## SimpleFactoryPattern

```mermaid

class PizzaStore:
  PizzaStore : -PizzaFactory pizzafactory
  PizzaStore : +orderPizza()
  PizzaStore --> PizzaFactory

class PizzaFactory:
  PizzaFactory : +createPizza()
  PizzaFacotry <|-- SimplePizzaFactory

class SimplePizzaFactory:
  SimplePizzaFactory : + createPizza()

```


## FactoryMethodPattern
