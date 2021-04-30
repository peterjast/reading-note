# Stacks and Queues

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## What is a stack?

* data structure consisting of nodes

* nodes refence next node in stack

* nodes don't reference previous node in stack

### Push

* nodes are pushed into the stack

#### Push O(1)

* pushing a node into stack is always O(1)

* push node into stack by assigning it as new top

* property next is equal to original top

##### Push Pseudocode

```javascript
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node
```

### Pop

* nodes are removed, or popped from stack

#### Pop O(1)

* removing node off top

* top node is re-assigned to node below top node and returned to user

* check isEmpty before pop

##### Pop Pseudocode

```javascript
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value
```

### Top

* top of stack

### Peek

* view the value at the top of the stack

#### Peek O(1)

* inspect top of stack

* check isEmpty before peek

##### Peek Pseudocode

```javascript
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   return top.value
```

### IsEmpty O(1)

#### isEmpty PseudoCode

```javascript

ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL
```

## What is a Queue

### Enqueue

* Nodes added to queue  

```javascript
ALGORITHM enqueue(value)
// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
   node = new Node(value)
   rear.next <-- node
   rear <-- node
```

### Dequeue

* Nodes removed from queue

```javascript
ALGORITHM dequeue()
// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty

   Node temp <-- front
   front <-- front.next
   temp.next <-- null

   return temp.value
```

### Front

* first Node of queue

### Rear

* last Node of the queue

### Peek Queue

* view value of first node in queue

```javascript
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of the front Node in Queue
// EXCEPTION if Queue is empty

   return front.value
```

### IsEmpty

 returns true when queue is empty otherwise returns false.

```javascript
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return front = NULL
```

### FIFO

* First in first out

* first item added is first item out

### LILO

* Last in last out

* last item added is last item out

## Resources

[Stacks and Queues](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)
