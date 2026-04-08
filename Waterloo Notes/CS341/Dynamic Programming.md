![[Pasted image 20260328190445.png]]
![[Pasted image 20260328190456.png]]
![[Pasted image 20260328190514.png]]
- All these improved versions use Theta(n) additions
- **Main feature**: solve subproblems bottoms up and store solutions if needed
	- Solve problems recursively
	- use a small number of nested subproblems
	- may have to store results for all subproblems
	- can often be turned into 1+ loops
-![[Pasted image 20260328190917.png]]

**Weighted Interval Scheduling**
- same setup with intervals 
- However now each interval has a weight, and we want a choice of intervals that don't overlap which maximizes the weighted sum (greedy when weight = 1)
Recursive Solution:
if we sort by non decreasing finish times, for the last interval we either OPT(n) = max{1, 2}
1. pick it (add the w(n) a with the OPT(p(j)) where p(j) returned all of the intervals that don't overlap with the last interval)
2. don't pick it
	1. solve the problem for the n-1 interval (OPT(n-1))

```python
ComputeP(s[1..n], f[1..n])
// Precondition: intervals sorted by finish time
1. for j = 1, ..., n
2.     // binary search for the last i with f[i] <= s[j]
3.     lo = 0, hi = j - 1
4.     while lo < hi
5.         mid = ceil((lo + hi) / 2)
6.         if f[mid] <= s[j]
7.             lo = mid
8.         else
9.             hi = mid - 1
10.    p[j] = lo
11. return p[1..n]
```
- know the difference between leftmost (smallest index) and right most (case here) of binary search
![[Pasted image 20260406195753.png]]
**0/1 knapsack
![[Pasted image 20260406200724.png]]
- define o[w,i] max value  achievable using knapsack with capacity w or i items
- we want o[W,n]
- we either pick item n or we don't pick it
if we pick it then
- v[n] + O[W-w[n], n-1], (w[n] <= W as well)
-O[W,n-1]
base case 
O[0,i] = 0 (no weight = no value)
O[w,0] = 0 (no items = no value)
![[Pasted image 20260406201026.png]]
- recipe for similar problems
- notice the table structure/size
- first define how to measure the problem and what the problem wants in general
- derive recurrence relation (usually pick or don't pick)
- loop and add constraints if applicable

```python
RecoverSubset(O, w, v, W, n)
1. S = empty set
2. w_remaining = W
3. for i = n, n-1, ..., 1
4.     if w_i <= w_remaining and
         v_i + O[w_remaining - w_i, i - 1] > O[w_remaining, i - 1]
5.         add i to S
6.         w_remaining = w_remaining - w_i
7. return S
```

![[Pasted image 20260407112056.png]]
- instead of maximizing value, we just want the sum of values to be equal to K/W
![[Pasted image 20260407112403.png]]
![[Pasted image 20260407112537.png]]
- option 1 if understand DP well, option 2 as an extension of reduction problems

**Longest increasing subsequence**
![[Pasted image 20260407112933.png]]
![[Pasted image 20260407114946.png]]
L[i] = 1 + max{ L[j] : j < i and A[j] < A[i] }
![[Pasted image 20260407115305.png]]

![[Pasted image 20260407125239.png]]
- BONUS IGNORE

**Longest Common Subsequence**
![[Pasted image 20260407125337.png]]
![[Pasted image 20260407125444.png]]

**Edit Distance**
![[Pasted image 20260407130114.png]]![[Pasted image 20260407135330.png]]
**Max independent set in a tree**
![[Pasted image 20260407140300.png]]
- is the root in S or not?
	- if not, then S is the union of sets contained in the children or the root
	- if yes, then the children of S can't be in S, and it includes the union of sets contained in the grandchildren of the root
![[Pasted image 20260407140719.png]]
```python
MaxIndependentSetDP(T, r)
1.  let M[1..n] = [undefined, ..., undefined]
2.  return Solve(r)

Solve(v)
1.  if M[v] is defined, return M[v]
2.  if C[v] is empty
3.      M[v] = 1
4.      return M[v]
5.  exclude = 0
6.  for each child c in C[v]
7.      exclude = exclude + Solve(c)
8.  include = 1
9.  for each child c in C[v]
10.     for each grandchild g in C[c]
11.         include = include + Solve(g)
12. M[v] = max(include, exclude)
13. return M[v]
```
- top down approach for tree structure with memoization
**Optimal Binary Search Trees**
![[Pasted image 20260407141414.png]]
![[Pasted image 20260408080724.png]]

****![[Pasted image 20260407143759.png]]

![[Pasted image 20260407143821.png]]
**Text Segmentation**
![[Pasted image 20260408083220.png]]
![[Pasted image 20260408083334.png]]
![[Pasted image 20260408083350.png]]