# Binary Search

## Concept
Binary search only works on a *sorted* list. Suppose you have a list of students sorted alphabetically. If you want to search for Abhishek, you can simply start from the top of the list because names starting with A will appear first. But what if you want to search for Madhu, which is somewhere around the middle of the list? Do you start from A and go through every name until you reach M? Instead, you can start by checking the middle of the list. To do that, we first need to find the middle index. We are not talking about the middle of the alphabet, but the middle position in the list. Since each student has a unique index, we can calculate the middle index using the following formula: <br>
```text
middle_index = (first_index + last_index) / 2
```
We can find the middle index by using this formula. But there are nuances here if we use this in programming languages. There are different data types to store values such as int, float, double, etc. Each data types can only hold values within certain ranges. So when you use the above formula to calculate middle index, the value might go out of the range. Which means it causes the interger to overflow. So, in this case we use this formula: <br>
```text
middle_index = first_index + ((last_index - first_index) / 2)
```
Now, Compare the middle element with the target. If the middle element is smaller than the target, eliminate the left half and continue searching on the right. Otherwise, if the middle element is larger than the target, eliminate the right half and continue searching on the left. <br>

## Pseudo code
```code
BinarySearch(arr, target)
    low = 0
    high = length(arr) - 1
    while low <= high
        mid = low + (high - low) / 2
        if arr[mid] == target
            return mid
        else if arr[mid] < target
            low = mid + 1
        else 
            high = mid - 1
    return -1
```

## Time and space complexity
| Number of Elements (`n`) | Maximum Steps | Relationship          |
| -----------------------: | ------------: | --------------------- |
|                        8 |             3 | `2³ = 8`              |
|                       16 |             4 | `2⁴ = 16`             |
|                       32 |             5 | `2⁵ = 32`             |
|                       64 |             6 | `2⁶ = 64`             |
|                      128 |             7 | `2⁷ = 128`            |
|                      256 |             8 | `2⁸ = 256`            |
|                    1,024 |            10 | `2¹⁰ = 1,024`         |
|                1,048,576 |            20 | `2²⁰ = 1,048,576`     |
|            1,073,741,824 |            30 | `2³⁰ = 1,073,741,824` |
|            4,294,967,296 |            32 | `2³² = 4,294,967,296` |

Since binary search eliminates half of the remaining elements in every iteration, the number of steps grows very slowly as the input size increases. Even for a list containing over 4 billion elements, binary search requires at most 32 comparisons. Therefore, the *time complexity* is *O(log n)*.

*Space complexity*: *O(1)*, since we are only using few variable such as low, high and mid.