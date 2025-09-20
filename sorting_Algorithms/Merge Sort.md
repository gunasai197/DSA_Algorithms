## What is Merge sort:

**Merge sort  is a popular sorting algorithm known for its efficiency and stability. 
It follows the divide-and-conquer** approach. It works by recursively dividing the input array into two halves, recursively sorting the two halves and finally merging them back together to obtain the sorted array.
## or

**Merge Sort** is a **divide and conquer** sorting algorithm.
It works by repeatedly **dividing** the array into smaller subarrays until each subarray has only one element, and then **merging** those subarrays back together in sorted order.  

---
![[Pasted image 20250920194937.png]]

## Here's a step-by-step explanation of how merge sort works:

- **Divide:** Divide the list or array recursively into two halves until it can no more be divided.
- **Conquer**: Each subarray is sorted individually using the merge sort algorithm.
- **Merge:** The sorted subarrays are merged back together in sorted order. The process continues until all elements from both subarrays have been merged.
## Example:

**Divide:**

- ****[38, 27, 43, 10]**** is divided into ****[38, 27 ] and ****[43, 10]**** .
- ****[38, 27]**** is divided into ****[38]**** and ****[27]**** .
- ****[43, 10]**** is divided into ****[43]**** and ****[10]**** .

**Conquer:**

- ****[38]**** is already sorted.
- ****[27]**** is already sorted.
- ****[43]**** is already sorted.
- ****[10]**** is already sorted.

**Merge:**

- Merge ****[38]**** and ****[27]**** to get ****[27, 38]**** .
- Merge ****[43]**** and ****[10]**** to get ****[10,43]**** .
- Merge ****[27, 38]**** and ****[10,43]**** to get the final sorted list ****[10, 27, 38, 43]****

Therefore, the sorted list is ****[10, 27, 38, 43]**** .

**Pseudocode**

```
MergeSort(arr):
    if length(arr) <= 1:
        return arr
    mid = len(arr) / 2
    left = MergeSort(arr[0..mid-1])
    right = MergeSort(arr[mid..end])
    return Merge(left, right)

Merge(left, right):
    result = []
    while left and right are not empty:
        if left[0] <= right[0]:
            append left[0] to result
            remove left[0]
        else:
            append right[0] to result
            remove right[0]
    append remaining elements of left or right
    return result

```