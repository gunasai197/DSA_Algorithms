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

### Real-World Example of Insertion Sort

### 1. **Arranging Playing Cards in Your Hand**

When you play cards, you usually:
- Pick one card at a time.
- Compare it with the cards already in your hand.
- Insert it at the right place.
👉 This is exactly how **Insertion Sort** works.

### 2. **Arranging Books on a Shelf**
Suppose you want to arrange books by height:
- Start with the first book (already "sorted").
- Take the next book and insert it into its correct place among the arranged ones.
- Continue until all books are sorted
### 3. **Sorting Emails by Date (Manually)**
If you look at your unsorted emails and move each one into the correct place in a sorted list (say, from newest to oldest), you are performing insertion sort.

### 4. **Classroom Attendance Roll**
When a new student joins a class:
- The teacher finds the correct alphabetical position of the new name in the list.
- Shifts the names downward.
- Inserts the new student’s name.
That’s insertion sort in real life.