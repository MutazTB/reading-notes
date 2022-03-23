# Linked Lists

Linked List is a linear data structure which consists of a group of nodes in a sequence. 
Each node contains two parts :

1. Data− Each node of a linked list can store a data.
2. Address − Each node of a linked list contains an address to the next node, called "Next".

***The first node of a Linked List is referenced by a pointer called Head***

---

**Advantages of Linked List**
1. They are dynamic in nature and allocate memory as and when required.
2. Insertion and deletion is easy to implement.
3. It has faster access time and can be expanded in constant time without memory overhead.

---

**Types of Linked List**

1. **Singly Linked List** : Singly linked lists contain nodes which have a data part and an address part, i.e., Next, which points to the next node in the sequence of nodes. The next pointer of the last node will point to null.

2. **Doubly Linked List** : In a doubly linked list, each node contains two links - the first link points to the previous node and the next link points to the next node in the sequence.The prev pointer of the first node and next pointer of the last node will point to null.

3. **Circular Linked List** : In the circular linked list, the next of the last node will point to the first node.

4. **Doubly Circular Linked List** : In this type of linked list, the next of the last node will point to the first node and the previous pointer of the first node will point to the last node.

***To learn more*** [Linked List](https://www.c-sharpcorner.com/article/linked-list-implementation-in-c-sharp/)