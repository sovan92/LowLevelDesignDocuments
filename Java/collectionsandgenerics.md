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
