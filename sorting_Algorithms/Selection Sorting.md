## What is Selection Sort:

Selection Sort is one of the **simplest sorting algorithms** in Data Structures & Algorithms (DSA).  
It is a **comparison-based, in-place sorting technique**.    
👉 In simple words:
- It works by **repeatedly finding the smallest (or largest)** element from the **unsorted part** of the array and placing it in its **correct position** in the sorted part. 

So, the array gets divided into two parts:
1. **Sorted part** (at the left, adding step by step).
2. **Unsorted part** (at the right, reduced step by step).

## working of selection sort:

**Step - by - Step:** 
1. Start with the first element of the array.
2. Find the **minimum element** from the unsorted part.
3. Swap it with the **first element**.
4. Now the first element is sorted.
5. Repeat this process for the remaining elements until the array is sorted.

### **Selecting Top-K Elements**
- In some systems, instead of sorting the full array, you only need the **top few smallest/largest values**.
- Selection sort works well because:
    - You can stop after finding first K values.
    - Example: In a game leaderboard, quickly finding **top 3 scores** out of 20 players.
###  **Sorting Database Query Results (small datasets)**
- When a **small number of records** are fetched from a database (like <100 rows), a simple algorithm like Selection Sort can be applied.
- Example: Sorting search results by price in a lightweight in-memory database in a small app.

# Real-world Analogy
Imagine you are arranging books by height:
- You look at all the books, pick the **shortest one**, place it first.
- Then look at the remaining, pick the **next shortest**, place it second.
- Continue until all are arranged. 
 
**Pseudocode:**
```
for i = 0 to n-1:
    min_index = i
    for j = i+1 to n-1:
        if arr[j] < arr[min_index]:
            min_index = j
    swap arr[i] and arr[min_index]
```

**Code:**
```python 
def selection_sort(arr):
    
    for i in range(len(n)):  # For each position
        min_index = i   # Assume first element is min
        for j in range(i+1,len(n)):
            if arr[j] < arr[min_index]:
                min_index = j   # Update min_index
        
        # Swap min element with first element of unsorted part
        arr[i], arr[min_index] = arr[min_index], arr[i]

    return arr

# Example
arr = [64, 25, 12, 22, 11]
print("Original:", arr)
sorted_arr = selection_sort(arr)
print("Sorted:", sorted_arr)

```
## Time Complexity:

- **Best Case:** O(n²) → Even if already sorted, it still checks all comparisons.
- **Worst Case:** O(n²) → Always scans entire unsorted array.
- **Average Case:** O(n²).
- Total comparisons = `(n-1) + (n-2) + … + 1 = n(n-1)/2 ≈ O(n²)`.
## Space Complexity:

-  O(1) -> In-place sorting (No extra memory needed).



