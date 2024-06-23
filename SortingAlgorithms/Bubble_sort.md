# Bubble sort
- Approach : bubble highest element to the last in each iteration
- Brute Force ,decrease and conquer
- Time Complexity : $O(n^2)$
- Space Complexity : $O(1)$

```python
BubbleSort(A,n)
for i = n-1 to 0:# i marks the last index of unsorted array.
    for j = 0 to i-1:# used bubble the largest element
        if A[j+1]<A[j]:
            swap(A[j],A[j+1])
```

``` python
SWAP(a, b) # 5, 6
a = a+b # a = 11
b = a-b # 5
a = a-b # 6
```
