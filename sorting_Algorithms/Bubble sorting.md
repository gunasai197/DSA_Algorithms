
# what is bubble sorting:

- Bubble Sort is one of the simplest **sorting algorithms** in **Data Structures and Algorithms (DSA)**.
- It works by **repeatedly swapping adjacent elements** if they are in the wrong order.
- This algorithm is not suitable for large data sets as its average and worst-case time complexity are quite high.
- Good for **small datasets** and for **learning sorting basics**.

## Working of Bubble Sort

1. Compare the **first two elements**.
    - If the first is greater than the second → swap them.    
2. Move to the next pair (2nd and 3rd elements) → compare and swap if needed.
3. Keep going until the **last element**.
    - After the first pass, the **largest element is at the end**.   
4. Repeat the process for the **remaining elements** until the list is sorted.

## Ex:

   array = [5,3,8,4,2]


## code:
```
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False   # assume no swaps this round
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True   # swap happened
        if not swapped:   # no swap = array already sorted
            break
    return arr

print(bubble_sort([2, 3, 4, 5, 6]))  # already sorted

```
