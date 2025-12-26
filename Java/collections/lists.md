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






