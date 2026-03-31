in 1D:
- g(x) is differentiable at x = a if g'(a) exists
- Error in Linear Approximation:
![[Pasted image 20260328115741.png]]
![[Pasted image 20260328120105.png]]
- the errror tends to zero faster than the displacement (denom)
- the tangent line is the unique line that satisfies this property
- the tangent line at (a,g(a)) is the best straight line approximation to the graph y = g(x) near (a,g(a))
in **2D:**
![[Pasted image 20260328120346.png]]
![[Pasted image 20260328120636.png|459]]
 - secondary theorem to prove that the tangent plane gives the best linear approximation to the graph z = f(x,y) near (a,b) and that the linear approximation is a good approximation if and only if f is differentiable at (a,b)
 - **partial derivatives of f existing at (a,b) is necessary, but not sufficient for differentiability**
	 - since both partial derivatives must exist for the linear approximation to exist

See Full Solution Not differentiable and differentiable example in mobius
Logical Hierarchy to save time
1. find partial derivatives
	1. if DNE -> not differentiable
	2. if CTS -> see below (differentiable)
2. if not cts:
3. calculate numerator + simplify
4. test for failure to check that the limit could be 0
	1. if not -> not differentiable
5. If all candidates are 0, apply squeeze theorem
	1. |x| <= sqrt(x^2 + y^2) to cancel out denom

**Tangent Plane**
![[Pasted image 20260328125542.png]]
- Graph of linearization/ Linear Approximation if f is differentiable

**Differentiability and Continuity**
![[Pasted image 20260328125646.png]]
- differentiable implies continuity
- contrapositive, not cts implies not differentiable
**Continuous Partial Derivatives and Differentiability**
![[Pasted image 20260328130224.png]]
![[Pasted image 20260328130214.png|532]]
- MVT used in proof
So:
**Cts Partials -> Differentiable -> Cts** Chain
In order to prove differentiability without full formula
1. **differentiate f to get partial derivatives**
2. **check if partial derivatives are cts by inspection (continuity theorems)**
3. **if so, by previous theorem then must be differentiable at (a,b)**

**Generalize Differentiability to R^n**
![[Pasted image 20260328131451.png]]- with all previous theorems holding true as well

**Linear Approximation Revisted**
If f is differentiable then the linear approximation is a good approximation of f(x,y) near (a,b) (This is equivalent to the tangent plane)
![[Pasted image 20260328132114.png]]![[Pasted image 20260328132235.png]]