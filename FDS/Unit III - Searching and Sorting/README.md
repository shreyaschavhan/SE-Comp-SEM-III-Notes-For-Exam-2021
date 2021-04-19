#  Unit III - Searching and Sorting 

## ✧ Searching

* **Linear Search / Sequential Search:**
> * Algorithm:
> 	* Start from the leftmost element of arr[] and one by one compare x with each element of arr[]
>	* If x matches with an element, return the index.
> 	* If x doesn’t match with any of elements, return -1.
> 
> * Code: 
> ``` 
> int linear_search(int arr[] int n, int key){
> 	for (int i = 0; i < n; i++){
>		if(arr[i] == key){
>			return i;
>		}	
>	}
> 	return -1;
> }
> ```
> 
> * Time Complexity: O(n)

---
* **Binary Search:**
> * General:
>       * Elements should be present in sorted order
>       * We will find mid element and compare the key
>       * if key greater than mid then search in next half
>       * vice versa
>
> * Algorithm:
> 	* Compare key with the middle element.
>	* If key matches with middle element, we return the mid index.
> 	* Else If key is greater than the mid element, then key can only lie in right half subarray after the mid element. So we recur for right half.
>	* Else (key is smaller) recur for the left half.
>
> * Code:
> * Iterative:
> ```
> int binary_search(int arr[], int n, int key){
> 	int start = 0;
>	int end = n;
>	while(start == end){
>		int mid = (start+end)/2;
>		if(key == arr[mid]){
>			return mid;
>		}
>		else if(key > arr[mid]){
>			start = mid + 1;
>		}
>		else{
>			end = mid - 1; 
>		}
>	}
> }
> ```
>
> * Time Complexity: 
>	* After first iteration, length of array = n
> 	* After second, length = n/2
> 	* ...
> 	* After k iterations, length of array = n/2<sup>n</sup>
>	* Let the length of array become 1 after k iterations
> 		* n/2<sup>n</sup> = 1
> 		* n = 2<sup>n</sup>
> 		* log<sub>2</sub>(n) = log<sub>2</sub>(2<sup>n</sup>)
>		* k = log<sub>2</sub>(n) 

---

* **Sentinel Search:**
> * Algorithm:
> 	* In this search, the last element of the array is replaced with the element to be searched and then the linear search is performed on the array without checking whether the current index is inside the index range of the array or not because the element to be searched will definitely be found inside the array even if it was not present in the original array since the last element got replaced with it. So, the index to be checked will never be out of bounds of the array. The number of comparisons in the worst case here will be (N + 2).
>
> * Code:
> ```
> int sentinel_search(int arr[], int n, int key){
>	int last = arr[n-1];
> 	arr[n-1] = key;
> 	int i = 0;
> 	while(arr[i] != key)
>		i++;
> 	
> 	arr[n-1] = key;
> 	if((i < n - 1) || arr[n-1] == key)
> 		return i;
> 	return -1;
> }
> ```
>
> * Time Complexity: O(n)
> 
