# ArrayList Vs LinkedList

ArrayList is good for lookups if you know the index . LinkedList is good for inserting and deleting elements. 
ArrayList is poor for adding and removing elements. LinkedList is special as implements List and Deque. 

## Creating a List with a Factory

```java

int[] arr = new int[]{1, 2,3};
List<Integer> arrList = Arrays.asList(arr);   // Returns a fixed size list backed by an array. Can't delete elements. Can replace elements. 

List<Integer> arrList1 = List.of(1,2,3);      // Returns a immutable list. Can't delete or replace elements. 

List.copyOf(collection);                      // returns a copy of the original collection as list. Can't delete or replace elements. 

// If we change the array, we change the list. That't the power of aslist. 
arr[0] = 5;
System.out.println(arrList);   // [5,2,3]
arrList.set(0, 8);
System.out.println(Arrays.toString(arr)); // [8,2,3]

Where as any update to arrList1 will cause the UnsupportedOperationException.

```
## Creating list with a Constructor
Most collections have 2 contructors you need to know for the exam. 

```java

var linked1 = new LinkedList<String>();
var linked2 = new LinkedList<String>(linked1);


// ArrayList on the otherhand has a extra constructor.

var list1 = new ArrayList<String>();
var list2 = new ArrayList<String>(list1);
var list3 = new ArrayList<String>(10); // You can provide a single argument to provide the number of slots. But you dont'; have to. 
```


## Working with lists methods. 

```java

boolean add(E element)  // Available on collection interface.

void add(int index, E element) // Add element at index and moves all other elements by 1 towards the end. There is a difference between collection and this. 

E get(int index) // Get element at index.

int indexOf(E element) // get indexOf or get -1 if not found.

int lastIndexOf(E element) // get last index of or get -1

E remove(int index)  // removes at index . Look at the difference . The Collection remove provides a boolean , this remove provides a Element. 


default void replaceAll(UnaryOperator<E> op)  // So we can do things like this . new ArrayList<>(List.of([1,2,3])).replaceAll(x -> x**2); OP -> [2,4,9]

E set(int index, E element) // replaces element at index and returns the original . Throws Index out of bound if index is invalid. 


default void sort(Comparator<? super E> c) Sorts list. We cover this in the sorting data section.



```





