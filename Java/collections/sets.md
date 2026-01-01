# Sets

## Initialization of sets
```java
// Immuatable set
Set<Character> letters = Set.of('a','b','c');
Set<Character> lettersCopy = Set.copyOf(letters);

Set<Integer> integers = Set.of(66, 50, 82);

for(Integer x : integers):
    System.out.println(x);

// prints in any order. 

Set<Integer> integers = new LinkedHashSet<>();

integers.add(100); // true
integers.add(120); // true
integers.add(300); // true

for(Integer x : integers):
    System.out.println(x);

// prints [100, 200, 300]

Set<Integer> integers = new TreeSet<>();

// Prints in the natural order or integers . Stores them in a binary search tree. 

```
