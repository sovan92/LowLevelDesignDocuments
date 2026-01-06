# Queue and Deque

Queue with LinkedList vs ArrayDeque 

- Arraydeque is more efficient. So if we need list functionality alone we should use the linkedlist otherwise use the arraydeque .
## Queue Methods
One comes up with an exception other doesn't
Add to the back 

- boolean add(Element e)  - Exception
- boolean offer(Element e)

- E element() - Exception if the queue doesn't have any element.
- E peek() - Not an excpetion , gets the data from the front of the queue.

- E remove() - Exception if queue is empty .
- E poll() - Not an exception .

