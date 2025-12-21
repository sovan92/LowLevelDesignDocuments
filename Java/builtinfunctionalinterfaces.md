# What are the built in functional interfaces

There are 4 types of Functional Interfaces. 

Supplier    get

Consumer    accept

Predicate   test

Function    apply

## What are the signatures of such interfaces

```java

Supplier<T>         T get()             // Doesn't take any parameter and just returns a value. Note: There is no BiSupplier as it doesn't take parameters. 

Consumer<T>         void accept(T)      // It takes a parameter and doesn't return anything. 

BiConsumer<T, U>    void accept(T , U)  // It takes 2 parameters and doesn't return anything. 

Predicate<T>        boolean test(T)     // It takes 1 parameter and just returns a boolean.

BiPredicate<T, U>   boolean test(T, U)  // It takes 2 parameters and just returns a boolean. 

Function<T, U>      U apply(T)          // Function takes the first parameter as argument and returns the second as return type. 

BiFunction<T, U, V> V apply(T, U)       // Function takes the first 2 parameters and 3rd as the return type.

UnaryOperator<T>    T apply(T)          // Function takes T as parameter and  T as return type.

BinaryOperator<T>   T apply(T, T)       // Function takes 2 T parameters and T as the return type. 

```

