# Collections and Generics

## List , Set, Queue, Map

```java
    Collection
        - Set
            - HashSet
            - SequencedSet
                - LinkedHashSet
                - TreeSet
        - SequencedCollection
            - List
                - ArrayList
                - LinkedList        
        - Queue
            - Dequeue
                - LinkedList
                - ArrayDeque
    Map
        - HashMap
        - SequencedMap
              - LinkedHashMap
              - TreeMap
    
```
## Generics -
Generics are nothing but parametrized types. Generics can be infered both from left as well as from the right side of the expression. 

### Generics infered from the left side when diamond operator is used in the right. 

```java

List<Integer> arrList = new ArrayList<>(List.of(1,2,3));
Map<List<Integer>, Integer> map = new HashMap<>();

```
### Generics can be infered from the right side when var is used on the left
```java

var list = new ArrayList<Integer>();
var mapOfList = new HashMap<Long, List<Integer>>();
```
## Adding Data

The add method inserts a new element into Collection and returns whether it was successful . 
```java
public boolean add(E element)

Collection<String> list = new ArrayList<>();
list.add("sparrow"); // true
list.add("sparrow"); // true

Collection<String> set = new HashSet<>();
set.add("sparrow");  // true
set.add("sparrow");  // false
```

## Removing Data from Collection
This time the boolean indicates whether the element was removed from the collection or not. 
```java
public boolean remove(Object obj)

Collection<String> birds = new ArrayList<>(List.of("sparrow", "hawk", "cardinal"));
birds.remove("cardinal"); // true
birds.remove("hawk"); // true
```
### Note::Removing data or adding data , isEmpty() or size() to a null collection will cause NPE . 

## Contains
.contains() will check the list for certain value in the collection. 
```java
public boolean contains(Object obj);
```
Contains calls the .equals() method to check if the element matches to the said element. 
## Removing if
Signature
```java
public boolean removeIf(Predicate<? super E> filter);
Collection<String> list = new ArrayList<>();
list.add("Magician");
list.add("Assistant");
System.out.println(list);
list.removeIf(s -> s.startsWith("A"))
System.out.println(s);


Collection>

```



