# Homework-MaxSub
1.	Function Definition (max_subarray_sum):
	•	The code defines a function named maxsub that takes a single argument arr, which is the input array for which we want to find the maximum subarray sum.
	2.	Initialization:
	•	maxend and maxsof variables are initialized to the first element of the input array arr. These variables will track the maximum subarray sum ending at the current index (maxend) and the overall maximum subarray sum encountered so far (maxsof).
	3.	Iteration:
	•	The code iterates through the input array arr starting from the second element (index 1).
	•	For each element x in the array:
	•	maxend is updated by taking the maximum value between the current element x and the sum of the current element and the previous maximum subarray sum ending at the previous index (maxend + x).
	•	maxsof is updated by taking the maximum value between the previous maxsof and the updated maxend. This ensures that maxsof always stores the maximum subarray sum encountered so far.
	4.	Return:
	•	After iterating through the entire array, the function returns the final value of maxsof, which represents the maximum subarray sum found in the input array.
	5.	Example Usage:
	•	An example usage of the function is provided where it is called with an input array arr and the maximum subarray sum is printed to the console.
