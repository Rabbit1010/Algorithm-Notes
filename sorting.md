# Sorting Algorithms 

## Terminology

* In-place: uses constant extra space.
* Stability: equal keys stay in the same order. All non-stable algorithms can be made stable by considering indexes as comparison parameter.
* All comparison-based sorting techniques have lower bound time complexity limit of $ O(nlog(n))$ .

## Some selected sorting algorithms

|  | Time Complexity | In-place? | Stability? | Note |
|----------------|----------------------------------|-----------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selection Sort | $ O(n^2) $  | yes | yes | Repeatedly find the min element and swap it to the beginning of the array. |
| Insertion Sort | $ O(n^2) $  | yes | yes | Like we sort poker cards. |
| Bubble Sort | Average $ O(n^2) $ | yes | yes | Repeatedly swap the adjacent elements if in wrong order. The algorithm needs one whole pass without any swap to know it is sorted and stop. |
| Merge Sort | $ O(nlog(n)) $ | no | yes | $ T(n)=2T(n/2) + \theta(n) $ Divide and Conquer algorithm. First repeatedly divides input array in two halves, and starts merging till the size becomes 1. Merge sort accesses data sequentially (no random access), so good for linked list sorting. |
| Quick Sort | Average $O(nlog(n))$ | yes | default no | Divide and conquer using a pivot. $ T(n)=T(k)+T(n-k-1) +\theta(n) $. The selection of pivot (partition strategy) is important. |
| Heap Sort | $ O(nlog(n)) $ | yes | default no | Build a max heap from the input data. Replace the largest item (root) with the last item of the heap and reduce the size of heap by 1 (pop out the largest item). Has limited use in practice. |
| Counting Sort | $ O(n+k) $ | no | yes | Efficient if the range if not significantly greater than the number of objects (k>>n not good!). |
| Bucket Sort | Average $ O(n+k) $ | no | depends on how each bucket is sorted | First we classify input data into $k$ buckets (so floating points would work), then sort each bucket (typically use insertion sort). The algorithm works best if the data is uniformly distributed. |
| Radix Sort | $ O(nd) = O(nlog_b(n)) ~= O(n) $ | no | yes | Sort each digit in a value using counting sort. $O(d*(n+b))$, where there is d digits in input integers and b is 10 in decimal system (can vary). If k is the max possible value, then d would be $O(log_b(k))$. So overall complexity is $O((n+b)*log_b(k))$. Let $k<=n^c$, it becomes $O(nlog_b(n)$. If we make be as n, then we get $O(n)$. |
| Tim Sort | Average $O(nlog(n))$ | no | yes | Insertion sort + Merge sort. An adaptive sorting algorithm used in Python's ```sorted()```. |