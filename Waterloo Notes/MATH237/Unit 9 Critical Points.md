in 1 variable:
![[Pasted image 20260401113409.png]]

**Local Extrema in 2 variables**
![[Pasted image 20260401113635.png]]![[Pasted image 20260401113722.png]]
![[Pasted image 20260401113745.png]]
- all local max/mins are critical points but not all critical points are local max/min (same as in 1 variable)
![[Pasted image 20260401113950.png]]
![[Pasted image 20260401114008.png]]

to find local extrema
1. find all critical points
2. determine whether they are local max, min or saddle points
- need to solve systematically

**2nd Derivative Test**
in 1 variable:
- ![[Pasted image 20260401121308.png]]

**Quadratic Forms**
![[Pasted image 20260401121341.png]]
![[Pasted image 20260401121444.png]]![[Pasted image 20260401122640.png]]
- this is easier, use from now on
![[Pasted image 20260401123927.png]]
**2nd Derivative Test for 2 variables**
![[Pasted image 20260401123122.png]]
- can also find eigenvalues of hessian matrix 
	- pos definite if all eigenvalues are positive
	- negative definite if all eigenvalues are negative
	- indefinite if both
- **if Hf(a,b) is semidefinite: the critical point may be local max, min or saddle point**
	- the critical point is **degenerate**
		- must investigate sign of f(x,y) - f(a,b) in small neighbourhood of (a,b)
			- try f(x,x) - f(a,b)
			- f(x,0) - f(a,b)

**We can Generalize all of these definitions**
![[Pasted image 20260401130752.png]]
**Summary**
![[Pasted image 20260401130836.png]]

**Convex Functions**
in 1 variable (concave up)
![[Pasted image 20260401130929.png]]
![[Pasted image 20260401131111.png]]
1. the graph of f lies above any tangent line
2. any secant line lies above the graph of f 

in 2 variables:
![[Pasted image 20260401131400.png]]![[Pasted image 20260401132756.png]]
- same property as 1 variable version
1. graph of f lies above  tangent plane
2. cross section of graph of f above line segment from (a1,a2) to (b1,b2) lies below secant line
![[Pasted image 20260401132850.png]]
3. if f is convex every critical point <= f(x,y)
4. if f is strictly convex there is only 1 critical point and < f(x,y)
	