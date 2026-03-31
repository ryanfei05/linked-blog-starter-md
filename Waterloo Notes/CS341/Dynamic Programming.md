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