## TO DO
- [ ] Understand merge sort below
- [ ] Modify MERGE to work with MERGE_SORT
- [ ] Analyze MERGE and MERGE_SORT

# Merge and Merge sort
- is a way of merging 2 sorted arrays
- time complexity - O(n\*logn)
- space complexity - O(n)
- divides the array into smaller sub arrays and sorts it
- divide and conquer method

``` python
MERGE(A, p, q, r)
	n1 = q - p + 1  # length of A[p:q]
	n2 = r - q      # length of A[q+1:r]
	let L[n1] and R[n2] be new arrays
	for (i = 0 to n1 - 1)       # copy all elements from A[p:q] into L[0:n1-1]
		L[i] = A[p + i]
	for (j = 0 to n2 - 1)       # copy all elements from A[q+1:r] into R[0:n2-1]
		R[j] = A[q + j + 1]
	i = 0  # indexes smallest remaining element in L
	j = 0  # indexes smallest remaining element in R
	k = p  # location being filled in A
	# As long as both L and R have unmerged elements,
	# copy the smallest element back in A[p:r]
	while (i < n1 and j < n2)
		if (L[i] <= R[j])
			A[k] = L[i]
			i = i + 1
		else
			A[k] = R[j]
			j = j + 1
		k = k + 1
	# Having gone through one of L and R copy the remainder of 
	# other to the end of A[p:r]
	while (i < n1)
		A[k] = L[i]
		i = i + 1
		k = k + 1
	while (j < n2)
		A[k] = R[j]
		j = j + 1
		k = k + 1
```


``` python
MERGE_SORT(A, p, r)
	if(p < r)
		q = (p + r) // 2
		MERGE_SORT(A, p, q)
		MERGE_SORT(A, q+1, r)
		MERGE(A, p, q, r)
```

