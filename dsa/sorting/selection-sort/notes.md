# Selection Sort

## Concept
This is a very basic sorting algorithm. Selection sort repeatedly find the smallest element in the unsorted portion of the array and places it at the beginning of the unsorted section. It does this by scanning the remaining elements to find the minimum value and then performing a swap. After each swap, one more element is sorted in its correct position. <br>

## Pseudo code
```code
selection_sort(arr) {
    for i = 0 to len(arr):
        min = i

        for j = i + 1 to len(arr):
            if arr[j] < arr[min]:
                min = j

        swap(arr[i], arr[min])
}
```

## Time and Space complexity
- **Space complexity** is **O(1)**, because the sorting is being performed in place without creating any new array. 
- **Time complexity** is **O(n x n)**, because you are iterating through the array twice to check each element with the other. 