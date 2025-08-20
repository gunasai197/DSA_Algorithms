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

# Real-world Analogy
Imagine you are arranging books by height:
- You look at all the books, pick the **shortest one**, place it first.
- Then look at the remaining, pick the **next shortest**, place it second.
- Continue until all are arranged. 
```
python 
def selection_sort(arr):
    n = len(arr)
    
    for i in range(n):  # For each position
        min_index = i   # Assume first element is min
        for j in range(i+1, n):
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


