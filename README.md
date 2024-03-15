# Homework-MaxSub
# Function Definition: max_subarray_sum

This code defines a function named `max_subarray_sum` which takes a single argument `arr`, representing the input array for which we want to find the maximum subarray sum.

## Initialization

- Two variables, `maxend` and `maxsof`, are initialized to the first element of the input array `arr`. These variables track the maximum subarray sum ending at the current index (`maxend`) and the overall maximum subarray sum encountered so far (`maxsof`).

## Iteration

- The code iterates through the input array `arr` starting from the second element (index 1).
- For each element `x` in the array:
  - `maxend` is updated by taking the maximum value between the current element `x` and the sum of the current element and the previous maximum subarray sum ending at the previous index (`maxend + x`).
  - `maxsof` is updated by taking the maximum value between the previous `maxsof` and the updated `maxend`. This ensures that `maxsof` always stores the maximum subarray sum encountered so far.

## Return

- After iterating through the entire array, the function returns the final value of `maxsof`, which represents the maximum subarray sum found in the input array.

## Example Usage

An example usage of the function is provided where it is called with an input array `arr` and the maximum subarray sum is printed to the console.
```python
def maxsub(arr):
    maxend = maxsof = arr[0]
    for i in arr[1:]:
        maxend = max(i, maxend + i)
        maxsof = max(maxsof, maxend)
    return maxsof

arr = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
print(f"Maximum subarray sum: {maxsub(arr)}")

