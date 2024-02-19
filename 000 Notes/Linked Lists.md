A linked list is a sequential [[Data Structure|list]] of nodes that hold data which point to other nodes also containing data.
## Usage
* Many List, Queue & Stack implementations;
* Great for creating circular lists;
* Can easily model real-life objects, such as trains;
* Often used for implementing of adjacency lists for graphs.
## Terminology
* Pointer – reference to another node.
* Node – an object containing data and pointer(s).
* Head – the first node in a linked list.
* Tail – the last node in a linked list.
## Singly vs Doubly Linked Lists
* Singly-linked lists only hold a reference to the next node.
* Doubly-linked lists hold references for both the next and previous nodes.
* In implementations, you always maintain a reference to the head and the tail for quick addition/removals (both sided for doubly-linked lists).
## Complexity
* Search – $O(n)$
* Inserting at head – $O(1)$
* Inserting at tail – $O(1)$
* Remove at head – $O(1)$
* Remove at tail – $O(n)$|$O(1)$
* Remove in the middle – $O(n)$
## References
[Algorithms/src/data_structures/linked_list.rs](https://github.com/TianyiShi2001/Algorithms/blob/main/src/data_structures/linked_list.rs)
[Algorithms/src/data_structures/linked_list/doubly_linked.rs](https://github.com/TianyiShi2001/Algorithms/blob/main/src/data_structures/linked_list/doubly_linked.rs)