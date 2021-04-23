# Linked List

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## What is a Linked List?

* A sequence of connected nodes - each node references the next node in the list

### Terminology

1. **Linked List** - A data structure containing nodes that link to the next node in the list.

1. **Singly** - refers to the reference the node has pointing towards the next node in the linked list

1. **Doubly** - refers to references to both the next and previous nodes

1. **Node** - individual items in the link list

1. **Next** - a property that each node contains - the Next property contains the reference to the next node

1. **Head** - reference of type Node to the first node in a linked list

1. **Current** - reference of type Node to the node currently being looked at - to traverse linked list, create new Current variable at Head to make sure you start from the beginning

## Traversal

* the **Next** value is extremely important for traversing a linked list and extracting the appropriate data because you can't use forEach or for loops and have to rely on Next value in each node to guide us to the next reference point

* the best way to traverse a linked list is with a while() loop, which allows us to check that the Next node in the list is not null with each iteration - if we do try to traverse on null, a NullReferenceException gets throw and will our program will crash

* While traversing the linked list, the Current variable will tell us where exactly we are in the linked list and will allow us to traverse the entire linekd list

### Traversal Example 

We give our traversal a use case by checking if our LinkedList includes a specific value

Pseudo-code:

```javascript
ALGORITHM Includes (value)
// INPUT <-- integer value
// OUTPUT <-- boolean

  Current <-- Head

  WHILE Current is not NULL
    IF Current.Value is equal to value
      return TRUE

    Current <-- Current.Next

  return FALSE
```

1. make sure we start at the beginning by creating Current at the Head

1. create while loop that runs if the node that Current is pointing to is not null

> Once we are in the while loop, we are checking if the value of the current node is equal to the value we are looking for. Given the logic, if that condition is true, then we have found the value we were looking for, so we return true.
> If the Current node does not contain the value we are looking for, we then must move Current to the next node that is being referenced. Again, because the condition of this while loop is to only run if we are still at a node, we can safely traverse to the next node without fear of getting a NullReferenceException.
> At this point, the while loop is re-evaluated. Step 3 & 4 will continue until Current reaches the end of the LinkedList. We will know we are at the last node in the linked list because the current node will be null. Once this condition becomes true, the while loop breaks, and we now know that we are at the end.
> Once we hit the end, we know that we did not find the value and return true at any point, so the value is not in the LinkedList. We return false.

## Resources

[linked list](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

[Whats a linked list anyway pt 1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

[Whats a linked list pt 2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)