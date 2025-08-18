
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


## code for bubble sort:
```python
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

## Time and space complexity for bubble sort:
# 1. Time Complexity

Time complexity measures **how many operations** (comparisons, swaps, etc.) the algorithm performs in terms of input size `n`.

👉 **Steps to find it:**

1. **Look at loops** (for/while).
    - Each loop contributes to time complexity.
2. **Count operations inside loops.**
    - Comparisons, swaps, assignments.
3. **Multiply nested loops.**
    - Example: a loop inside a loop (`O(n) * O(n) = O(n²)`).
4. **Take the dominant term** (ignore constants and lower-order terms).
---

**Example: Bubble Sort**
```
for i in range(n):                 # Loop 1 → runs n times
    for j in range(0, n-i-1):      # Loop 2 → runs (n-i-1) times
        if arr[j] > arr[j+1]:      # comparison → O(1)
            swap(arr[j], arr[j+1]) # swap → O(1)

```
- Outer loop → **n times**
- Inner loop → ~**n times** (on average)
- Total → **n × n = O(n²)**
👉 That’s how we say Bubble Sort takes **O(n²)** in worst and average case.
	If no swaps (already sorted array) → **O(n)** (best case).
# 2. Space Complexity

Space complexity measures **how much extra memory** the algorithm uses.

👉 **Steps to find it:**
1. **Check extra variables.**
    - Integers, booleans → O(1)
2. **Check extra arrays/structures.**
    - New array of size n → O(n)
3. **Check recursion stack.**
    - Recursive calls may add extra space.

 **Example: Bubble Sort**
- Uses only:
    - `i`, `j` (loop variables) → O(1)
    - `swapped` (boolean flag) → O(1)
    - `temp` (for swapping) → O(1)
- No extra arrays → **O(1) space**
#  General Formula to find the time complexity

- If you see **one loop** → O(n)
- **Two nested loops** → O(n²)
- **Three nested loops** → O(n³)
## Time Complexity:
- Best Case: **O(n)**
- Average Case: **O(n²)** --> when data is **randomly ordered** like some elements are arrange in asc order, some are in desc orders
- Worst Case: **O(n²)**
## Space Complexity
- Bubble Sort sorts **in-place** (no extra arrays needed).
- Only a few temporary variables (like `swapped` or `temp`).
👉 Space Complexity = O(1)