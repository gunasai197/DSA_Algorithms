*what is Insertion sort*

Insertion Sort is a **simple sorting algorithm** that builds the final sorted array one element at a time just like how we sort playing cards in our hands.

### How it Works (Logic)

1. Start from the **second element** (index `1`) because the first element alone is already “sorted”.
2. Pick the current element (called **key**) and compare it with elements before it.
3. Shift all elements that are **greater than the key** one position to the right.
4. Insert the key into its correct position.
5. Repeat until the whole array is sorted.

Pseudocode
```
for i = 1 to n-1:
    key = arr[i]
    j = i - 1
    while j >= 0 and arr[j] > key:
        arr[j+1] = arr[j]   // shift right
        j = j - 1
    arr[j+1] = key
```
