# Selection Sort

```cpp
SelectionSort(A,n)
for i=0 to n-1: // repeats n times
    min = i
    for j=i+1 to n-1: // repeats n-i times(for every iteration of i loop)
        if A[j] < A[min]:
            min = j
    temp = A[i]
    A[i] = A[min]
    A[min] = temp
```
- Time complexity: O(n^2)
- Space complexity: O(1)