``` python
BINARY_SEARCH(A, key)
	n = A.size
	low = 0 # left pointer
	high = n-1 # right pointer

	while(low <= high) # Repeat while low lies to the left of high
		mid = (low + high) // 2 # Integer division
		if(A[mid] == key) # Found key
			return mid
		else if(A[mid] < key) # Key lies to the right of A[mid]
			low = mid + 1
		else  # Key lies to the left of A[mid]
			high = mid - 1

	return -1
```
