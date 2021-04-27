#  Unit III - Searching and Sorting

## ✧ Syllabus:
> * Searching:
>   * Search Techniques:
>       * Sequential Search/linear Search
>       * Variant of Sequential Search:
>           * Sentinel Search
>           * Binary Search
>           * Fibonacci Search
>           * and Indexed Sequential Search
> * Sorting
>   * Types of Sorting:
>       * Internal and External Sorting
>       * General Sort Concepts:
>           * Sort Order
>           * Stability
>           * Efficiency and Number of passes
>       * Comparison Based Sorting Methods:
>           * Bubble Sort
>           * Insertion Sort
>           * Selection Sort
>           * Quick Sort
>           * Shell Sort
>       * Non-Comparison based sorting methods:
>           * Radix Sort
>           * Counting sort
>           * and Bucket Sort
>           * Comparison of All sorting methods and their complexities.

---
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
> * Time Complexity: O(log n)
>	* After first iteration, length of array = n
> 	* After second, length = n/2
> 	* ...
> 	* After k iterations, length of array = n/2<sup>n</sup>
>	* Let the length of array become 1 after k iterations
> 		* n/2<sup>n</sup> = 1
> 		* n = 2<sup>n</sup>
> 		* log<sub>2</sub>(n) = log<sub>2</sub>(2<sup>n</sup>)
>		* k = log<sub>2</sub>(n)
>
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

---

* Fibonacci Search:
> * Fibonacci sequence is: 0 1 1 2 3 5 8 13 ......
> * Which is F<sub>i</sub> = F<sub>i-1</sub> + F<sub>i-2</sub>, i >= 2
> * In binary search list is divided into half around the center.
> * In Fibonacci search, the list splits according to the Fibonacci sequence.
> * Fibonacci search requires that elements be ordered in non-decreasing order.
> * Fibonacci search in an array with n elements starts by locating F<sub>K</sub>,
>   * F<sub>K</sub> >= n and F<sub>K-1</sub> < n
> * Algorithm:
>   * We have to maintain three values during iteration: mid, p, q
>       * ![image](https://user-images.githubusercontent.com/68887544/116198321-71e6b000-a753-11eb-9c7b-b4e63b8f7dad.png)
>   * Key to be searched is compared with F<sub>mid</sub> with following outcomes:
>       * ![image](https://user-images.githubusercontent.com/68887544/116198801-08b36c80-a754-11eb-92aa-a0baac1f60c2.png)
>   * Search Continues, either by selecting the array right of the mid or  left of the mid.
>   * In each case, three values are maintained.
>   * ![image](https://user-images.githubusercontent.com/68887544/116199877-3fd64d80-a755-11eb-90ab-f13e43a3df5d.png)
> * Code:
> ```
> // C program for Fibonacci Search
> #include <stdio.h>
>
> // Utility function to find minimum of two elements
> int min(int x, int y) { return (x <= y) ? x : y; }
>
> /* Returns index of x if present, else returns -1 */
> int fibMonaccianSearch(int arr[], int x, int n)
> {
>	/* Initialize fibonacci numbers */
>	int fibMMm2 = 0; // (m-2)'th Fibonacci No.
>	int fibMMm1 = 1; // (m-1)'th Fibonacci No.
>	int fibM = fibMMm2 + fibMMm1; // m'th Fibonacci
>
>	/* fibM is going to store the smallest Fibonacci
>	Number greater than or equal to n */
>	while (fibM < n) {
>		fibMMm2 = fibMMm1;
>		fibMMm1 = fibM;
>		fibM = fibMMm2 + fibMMm1;
>	}
>
>	// Marks the eliminated range from front
>	int offset = -1;
>
>	/* while there are elements to be inspected. Note that
>	we compare arr[fibMm2] with x. When fibM becomes 1,
>	fibMm2 becomes 0 */
>	while (fibM > 1) {
>		// Check if fibMm2 is a valid location
>		int i = min(offset + fibMMm2, n - 1);
>
>		/* If x is greater than the value at index fibMm2,
>		cut the subarray array from offset to i */
>		if (arr[i] < x) {
>			fibM = fibMMm1;
>			fibMMm1 = fibMMm2;
>			fibMMm2 = fibM - fibMMm1;
>			offset = i;
>		}
>
>		/* If x is greater than the value at index fibMm2,
>		cut the subarray after i+1 */
>		else if (arr[i] > x) {
>			fibM = fibMMm2;
>			fibMMm1 = fibMMm1 - fibMMm2;
>			fibMMm2 = fibM - fibMMm1;
>		}
>
> 		/* element found. return index */
> 		else
> 			return i;
> 	}
>
> 	/* comparing the last element with x */
> 	if (fibMMm1 && arr[offset + 1] == x)
> 		return offset + 1;
>
> 	/*element not found. return -1 */
> 	return -1;
> }
>
> /* driver function */
> int main(void)
> {
> 	int arr[]
>		= { 10, 22, 35, 40, 45, 50, 80, 82, 85, 90, 100,235};
>	int n = sizeof(arr) / sizeof(arr[0]);
>	int x = 235;
> 	int ind = fibMonaccianSearch(arr, x, n);
> if(ind>=0)
> 	printf("Found at index: %d",ind);
> else
> 	printf("%d isn't present in the array",x);
> 	return 0;
> }
> ```
> * Time Complexity: O(log n)
---

* Binary vs Fibonacci search:
> ![image](https://user-images.githubusercontent.com/68887544/116200256-bf641c80-a755-11eb-8564-d14eedb60929.png)

---

* Indexed Sequential Search:
> ![image](https://user-images.githubusercontent.com/68887544/116201511-3221c780-a757-11eb-8b2d-7fab57d4ba2e.png)

---

## &#10023; Sorting:

* Comparison of Sorting Algorithms:
> ![image](https://user-images.githubusercontent.com/68887544/116205533-7dd67000-a75b-11eb-8a58-2bcc36bf31d6.png)
> ![image](https://user-images.githubusercontent.com/68887544/116205585-89299b80-a75b-11eb-8ed0-a3bc95862883.png)

----

> P.S. Done Unit III - Searching and Sorting
