*what is Insertion sort*

Insertion Sort is a **simple sorting algorithm** that builds the final sorted array one element at a time just like how we sort playing cards in our hands.

### How it Works (Logic)

1. Start from the **second element** (index `1`) because the first element alone is already “sorted”.
2. Pick the current element (called **key**) and compare it with elements before it.
3. Shift all elements that are **greater than the key** one position to the right.
4. Insert the key into its correct position.
5. Repeat until the whole array is sorted.

**Pseudocode
```
for i = 1 to n-1:
    key = arr[i]
    j = i - 1
    while j >= 0 and arr[j] > key:
        arr[j+1] = arr[j]   // shift right
        j = j - 1
    arr[j+1] = key
```

***Code 
``` python
def insertion_sort(arr):
    # Traverse from the 2nd element to the end
    for i in range(1, len(arr)):
        key = arr[i]   # element to be placed
        j = i - 1

        # Shift elements of arr[0..i-1] that are greater than key
        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1

        # Place key in its correct position
        arr[j + 1] = key

    return arr
# Example usage
nums = [7, 3, 5, 2, 9]
print("Unsorted:", nums)
print("Sorted:", insertion_sort(nums))

```

###  Time Complexity

- **Best case (Already sorted):** O(n)
- **Worst case (Reverse order):** O(n²)
- **Average case:** O(n²)
###  Space Complexity

- **O(1)** → In-place sorting (no extra space needed).