# Time Complexity

| Big O | Name | Example | Algorithms |
|--------------|---------------------|----------------------|------------------------------|
| $O(1)$ | Constant |  |  |
| $O(log n)$ | Logarithmic | $log(n)$, $log(n^2)$ | Binary search |
| $O(n)$ | Linear |  |  |
| $O(n log n)$ | Linearithmic | $nlog(n)$, $log(n!)$ | Fast Fourier transform |
| $O(n^2)$ | Quadratic |  | Bubble sort |
| $O(n^3)$ | Cubic |  | Naive matrix multiplication |
|  | Polynomial time (P) | $n^10$, $2n^2+n$ |  |
|  | Exponential time | $1.1^n$, $10^n$ | Find all subsets |
|  | Factorial time | $n!$ | Find all permutations of set |

## Master Theorem
* Used to quickly calculate the time complexity of a recurrence relation.

Let $ T(n) = aT(\frac{n}{b}) + O(n^d) $, then:

1. If $d>log_b(a)$,
	$T(n) = O(n^d) $
	
2. If $d=log_b(a)$,
	$T(n) = O(n^d log_b(n)) $
	
3. If $d<log_b(a)$,
	$T(n) = O(n^{log_b(a)}) $

* For example, consider binary search where $ T(n) = T(\frac{n}{2}) + O(1) $

  Therefore $a=1, b=2, d=0$

  So, $T(n) = O(log(n))$ (Case 2 of master theorem)

  