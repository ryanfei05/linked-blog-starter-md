**Extreme Value Theorem**
in 1 variable:
![[Pasted image 20260403151816.png]]![[Pasted image 20260403151833.png]]

in 2 variable:
![[Pasted image 20260403152316.png]]
**Topology definitions**
![[Pasted image 20260403152348.png]]

![[Pasted image 20260403152543.png]]
![[Pasted image 20260403152559.png]]
![[Pasted image 20260403152712.png]]
- a closed set in R^2 generalizes the idea of a closed interval in R
- no boundary vacuously implies consequent

**EVT on 2 variables**
![[Pasted image 20260403152945.png]]
- similar to 1 variable
- cts function **closed and bounded** has absolute max and min
- function can still have absolute max and min even if EVT not satisfied

**Algo for Extreme values**
in 1 variable:
- if f is cts, extrema occur at either critical points or interval endpoints
	- compare values at critical points with endpoints (closed interval method)
Generalize to 2 variable case:
![[Pasted image 20260403153637.png]]
- remember parametric form of circle/ ellipse

**Optimization with Constraints**
- want to find max/min of f(x,y) with constraint g(x,y) = k
algo to find max/min of f on g(x,y)  =k without having to parameterize curve
**Lagrange Multipliers**
![[Pasted image 20260403163803.png]]![[Pasted image 20260403163839.png]]![[Pasted image 20260403163919.png]]
![[Pasted image 20260403164555.png]]

- Overall summary for problem solving
	- min/max values on cts f algo on bounded region S guranteed by EVT 
	1. find critical points within bounded region, gradient = 0 or DNE -> critical point values
	2. extreme values on the boundary
		1. parameterize simple boundaries (circle, square, line segment), sub into f to find single variable function
		2. if not easily parameterizable, then we use lagrange multiplier algo for constraint to solve points on a boundary
	3. compare values found in step 1 and 2, largest is abs max, smallest is abs min

**Lagrange Multiplier Method on 3 variables**
![[Pasted image 20260405152905.png]]![[Pasted image 20260405153012.png]]
