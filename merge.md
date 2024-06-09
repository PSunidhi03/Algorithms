# Merge and Merge sort
- is a way of merging 2 sorted arrays
- time complexity - O( n logn )
- space complexity - O( n )
- divides the array into smaller sub arrays and sorts it
- divide and conquer method

``` python
MERGE(m1,m2)
  i=0,j=0,k=0#looping variables associated with arrays m1 m2 and m3
  m1[],m2[],m3[]#m1 m2 are the arrays to be merged and m3 is the merged array
  while(i < m1.size() && j < m2.size())#loop will continue till i and j are less than the size of the array
    if(m1[i] <= m2[j])#if element of m1 is less than element of m2
        m3[k] = m1[i]#element of m1 goes into the merged array
        i++
        k++
    else
        m3[k] = m2[j]
        j++
        k++
  
  while(i<m1.size())
    m3[k] = m1[i];
    i++
    k++

  while(j<m2.size())
    m3[k] = m2[j]
    j++
    k++

return m3

