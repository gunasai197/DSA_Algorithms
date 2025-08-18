
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

## Real World Examples using bubble sort:

   1 **Arranging students by height in a line**
- Suppose students are standing randomly.
- You keep checking each **pair of neighbors**:
    - If the left one is taller than the right one → swap.   
- After one full round, the **tallest student goes to the end** (like the "largest bubble").

 2 **Sorting books on a shelf (small collection)**
    - If you only have a few books, you might check two books next to each other and swap them if they’re out of order.
    - After repeating, the heaviest/largest book keeps moving to the end.

 3 **Small-Scale Data Sorting**
- For example, if a **shopkeeper** has just 5–10 products and wants to sort prices quickly in a simple program, Bubble Sort works fine.
- Sorting **student marks** in a small classroom.


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

## Time and space 
