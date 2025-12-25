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

## Methods examples

```java

||Interface   || ReturnType || Method |

|Consumer   |  Consumer |   andThen() |


Function     Function    andThen()


Function     Function    compose()


Predicte     Predicate   and()


Predicte     Predicate   or()


Predicte     Predicate   negate()


DoubleSupplier  double    getAsDouble()
IntSupplier     int       getAsInt()
LongSupplier    long      getAsLong()

DoubleConsumer  void      accept(double)
IntConsumer     void      accept(int)
LongConsumer    void      accept(long)

DoublePredicate boolean   test(double)
IntPredicate    boolean   test(int)
LongPredicate   boolean   test(long)

DoubleFunction<R> R       apply(double)
IntFunction<R>    R       apply(int)
LongFunction<R>   R       apply(long)

DoubleUnaryOperator double  applyAsDouble(double)
IntUnaryOperator    int     applyAsInt(int)
LongUnaryOperator   long    applyAsLong(long)

DoubleBinaryOperator double applyAsDouble(double, double)
IntBinaryOperator    int    applyAsInt(int, int)
LongBinaryOperator   int    applyAsLong(long, long)

ToDoubleFunction<T>  double applyAsDouble(T)
ToIntFunction<T>     int    applyAsInt(T)
ToLongFunction<T>    long   applyAsLong(T)

ToDoubleFunction<T, U>  double applyAsDouble(T, U)
ToIntFunction<T, U>     int    applyAsInt(T, U)
ToLongFunction<T, U>    long   applyAsLong(T, U)

DoubleToIntFunction     int    applyAsInt(double)
DoubleToLongFunction    long   applyAsLong(double)
IntToDoubleFunction     double applyAsDouble(int)
IntToLongFunction       long   applyAsLong(int)
LongToDoubleFunction    double applyAsDouble(long)
LongToIntFunction       int    applyAsInt(long)

ObjectDoubleConsumer    double accept(T)
ObjectIntConsumer       int    accept(T)
ObjectLongConsumer      long   accept(T)

```

## SomeExamples practiced

```java

public class ConvenienceMethods {
    public static void main(String[] args) {

        Predicate<String> eggs = s -> s.contains("eggs");
        System.out.println(eggs.test("eggs"));

        Predicate<String> brown = s -> s.contains("brown");

        Predicate<String> brownEggs = eggs.and(brown);
        Predicate<String> otherEggs = eggs.and(brown.negate());

        System.out.println(otherEggs.test("Red eggs"));

        System.out.println(brownEggs.test("brown eggs"));


        Consumer<String> c1 = x1 -> System.out.println("1:"+x1);
        Consumer<String> c2 = x2 -> System.out.println("2:"+x2);

        List<String> list = new ArrayList<>(List.of("a", "b", "c"));

        Collections.replaceAll(list, "a", "A");

        System.out.println(list);


        Function<Integer, Integer> before =  x -> x +1 ;
        Function<Integer, Integer> after = x -> x * x;

        Function<Integer, Integer> f3 = after.compose(before);

        System.out.println(f3.apply(1));

        


    }

}
```



