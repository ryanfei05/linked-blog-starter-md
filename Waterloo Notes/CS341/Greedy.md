Most basic example
**Minimizing Completion Time**
Want to minimize sum T of completion times -> order jobs in non decreasing times (take the min times first) to minimize sum of all completion times
![[Pasted image 20260327161503.png]]

**Interval Scheduling**
maximize the number of intervals that don't overlap
Sort intervals by non decreasing finish times and add the ones which don't create conflicts
![[Pasted image 20260327161614.png]]![[Pasted image 20260327161733.png]]

**Interval coloring**
Minimize number of colors used when assigning colors to each interval
- Finding classrooms for lectures
- colors <-> indices 0,1,2
Sort intervals by non decreasing start times, then for each interval give the smallest existing color (index) that creates no conflict or a new color if needed
![[Pasted image 20260327174412.png]]![[Pasted image 20260327174501.png]]

**Minimizing Lateness**
- given jobs with processing times t(i) and deadlines d(i)
- we want to schedule the jobs which minimize the maximal lateness where
- jobs start at s(i) (TBD decided) and finish at f(i) = s(i) + t(i)
- l(i) = f(i) - d(i)
- maximal lateness = max_i l(i)
Sort jobs in non-decreasing deadline order
![[Pasted image 20260327190433.png]]![[Pasted image 20260327190948.png]]
![[Pasted image 20260327191036.png]]
![[Pasted image 20260327191134.png]]
https://stumash.github.io/Algorithm_Notes/greedy/intervals/intervals.html

**Fractional Knapsack**
![[Pasted image 20260328164620.png]]
- Greedy Version -> fractional amounts
![[Pasted image 20260328164714.png]]
- Pick items in non-increasing value per kilo ratio v_i/w_i
![[Pasted image 20260328165126.png]]![[Pasted image 20260328175317.png]]