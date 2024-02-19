[[Data Structure|Container]] containing $n$ elements, indexable from the range $[0,\text { } n-1]$, that can **grow** and **shrink** in size.
## [[Big-O Notation|Complexity]]
* Access – $O(1)$
* Search – $O(n)$
	* Binary search doesn't work in non-sorted arrays!
* Insertion – $O(n)$
* Appending – $O(1)$
	* When appending, we have to resize the internal static array to append a new item!
* Deletion – $O(n)$
## Creating a dynamic array
Using a [[Static Array|static array]]!
1. Create a static array with an internal capacity.
2. Add elements to the underlying static array, keeping track of the number of elements.
3. If adding another element will exceed the capacity, then create a new static array with twice the capacity of the original array.
## References
