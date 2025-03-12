


`I`.
### **What is a function?**
##### A function maps some set of values to another set of values.
- Domain
	- Set of values that a function takes as input/accepts
	- $f : X \rightarrow Y$
- Codomain/range
	- Set of values a function outputs/produces.
- Preimages
	- Set of values that produce a given image.
- Image
	- A value in the codomain
- Injection
	- A one-toone function
	- $x_{1} = /x_{2}\rightarrow f(x_{1)}= /f(x_{2})$
- Surjection
	- Every element in the codomain has a preimage
- Bijection
	- Both an injection and a surjection
- Invertibility
	- If a function $f$ is invertible, we can define a $f^-1$ such that $\forall_{x} f^{-1(f(x))}= x$   



### What is Lambda Calculus
- Can represent anything we can compute.
	- ([[Turing Complete]])
- #### Notation
	- Variable 
		- v1 | v2 | v3 | v4...
	- Expression
		- ...
	- Abstraction
		- $\lambda$ `<variable> <expression>`
	- Application
		- `(<expression> <expression>)`


* #### Definition of Terms
	* ***free variable*:** 
		* $FV(x) = \{x\}$ 
		* $FV(\lambda xM ) = FV(M) - \{x\}$
		* $FV((MN)) = FV(M) \cup FV(N)$
	* ***bound variables*:** 
		* $\lambda x.(x+1)2$
		* $(x+1)[x:=2]$
		* $(2 + 1)$
		* $(3)$
		* **Examples**
			* SQUARED:
				$\lambda x.x*x$
		* 
	* **Freshness**
	* **[[Extensional Equality]]**
	* **[[Intensional Equality]]**
	* [[Alpha Conversion]] ($\alpha$-conversion)
	* [[Beta Reduction]] ($\beta$-reduction)
	* 