Gives an upper bound of the complexity in the *worst* case, helping to quantify performance as the input size becomes *arbitrarily large*.

For example, $O(1)$ being ``constant time``. Essentially, any valid mathemetical expression can be used as a parameter for $O(n)$.
## Properties
$O(n + c) = O(n)$
$O(cn) = O(n), \text{ } c > 0$
Here $n$ basically behaves like an infinity would.

Let $\int$ be a function that describes running time of a particular algorithm
$\int(n) = 7\log(n)^3 + 15n^2 + 2n^3 + 8$
$O(\int(n)) = O(n^3)$
## Examples
$$O(1) \text{ – Constant Time}$$
```c
a = 1
b = 2
c = 3
```
```c
for (int i = 0; i < 11; i++)
{

}
```
$$O(n) \text{ – Linear Time}$$
```c
for (int i = 0; n < 11; i++)
{
  // f(n) = n
  // O(f(n)) = O(n)
}
```
```c
for (int i = 0; i < 11; i += 3)
{
  // f(n) = n/3
  // O(f(n)) = O(n)
}
```
$$O(n^2) \text{ – Quadratic Time}$$
```c
for (int i = 0; i < n; i++)
{
  for (int j = 0; j < n; j++)
  {
	  // f(n) = n*n = n^2
	  // O(f(n)) = O(n^2)
  }
}
```
```c
for (int i = 0; i < n; i++)
{
  for (int j = i; j < n; j++)
  {
	  // f(n) = n*(n-1) = n^2 - n
	  // O(f(n)) = O(n^2)
	  // Nevermind! I was wrong here!
	  //
	  // It's supposed to be the following:
	  // What is (n-1) + (n-2) + n(-3) ... + 3 + 2 + 1
	  // In fact, it is n(n+1)/2, so
	  // O(n(n+1)/2) = O(n^2/2 + n/2) = O(n^2)
	  //
  }
}
```
```c
for (int i = 0; i < n; i++)
{
  for (int j = 0; j < 3*n; j++)
  {
  }
  for (int k = 0; k < 2*n; k++)
  {
  }
}
// f(n) = n * (3*n + 2*n) = 5n^2
// O(f(n)) = O(n^2)
`````````
$$O(n^4) \text{ – Quatric Time}$$
```c
for (int i = 0; i < 3*n; i++)
{
  for (int j = 10; j < 50; j++)
  {
  }
  for (int k = 0; k < n*n*n; k += 2)
  {
  }
}
// f(n) = 3*n * (40 + n*n*n/2) = 3*n^4/2
// O(f(n)) = O(n^4)
```
$$O(\log_2n) \text{ – Logarithmic Time}$$
```c
// Binary search algorithm – return the index of a value in an array.
unsigned int low = 0;
unsigned int high = n-1;
while low <= high
{
  unsigned int mid = (low + high) / 2;
  if array[mid] == value: return mid
  else if array[mid] < value: lo = mid + 1
  else if array[mid] > value: hi = mid - 1
}
return -1
```
## Other examples
* Finding all subsets of a set – $O(2^n)$
* Finding all permutations of a string – $O(n!)$
* Sorting using mergesort – $O(n \times log(n))$
* Iterating over cells in a matrix sized n by m – $O(n \times m)$