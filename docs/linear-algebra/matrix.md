# Matrix Calculus

## Matrix Calculus: Derivative 

A function $f: \mathbb{R}^{d\times d}\to\mathbb{R}$ is said to be **differentiable** at
$A\in\mathbb{R}^{d\times d}$ if there exists $B\in\mathbb{R}^{d\times d}$ such that 
$$
    \lim_{M\to 0} \frac{f(M+A)-f(A)-\text{Tr}(B^\top M)}{||M||} = 0
$$
We say that $B$ is the gradient of $f$ at $A$ and write 
$$
\nabla_X f(X) |_{X=A} = B
$$


### Example
Define the Voronoi cell of a lattice $\mathcal{L}\subset \mathbb{R}^d$

$$
\mathcal{V}(\mathcal{L})=\{x\in\mathbb{R}^d:\, \forall y\in \mathcal{L},\, ||x||\leq ||x-y||\}
$$ 

let $g: \mathbb{R}_{\geq 0}\to \mathbb{R}$ be a continuously differentiable function, and put

$$
f(A) = \frac{1}{|\text{det}(A)|}\cdot \int_{\mathcal{V}(A\mathcal{L})} g(||x||^2)\, dx
$$

for an invertible matrix $A\in\mathbb{R}^{d\times d}$. Then $f$ is differentiable at the identify matrix and $I_d$

$$
\nabla_X f(X)|_{X=I_d} = 2\int_{\mathcal{V}(\mathcal{L})} g'(||x||^2)xx^\top \,dx
$$

## Convexity

Let $K\subset\mathbb{R}^d$ be a symmetric convex body. We can define a norm 
$$
||x||_K = \inf \{s \geq 0 :\, x\in sK\}
$$
We can define the **matrix norm** on $$\mathbb{R}^{d\times d}$$
$$
\ell_K(A) = \left(\int_{\mathbb{R}^d}||Ax||_K^2\, d\gamma(x)\right)^{1/2}
$$
where $d\gamma(x)=e^{-\pi||x||^2}\,dx$. 

The **polar body** of a symmetric convex body $K$ is defined as 
$$
K^\circ = \{x\in\mathbb{R}^d: \, \forall y\in K,\, \langle x,y\rangle\leq 1\}
$$

### Theorem
For any symmetric convex body $K\subset \mathbb{R}^d$ there exists $A\in \text{SL}_n(\mathbb{R})$ such that 
$$
\ell_K(A)\cdot\ell_{K^\circ}((A^T)^{-1}) \leq \frac{d}{\pi}(\log_2 d +2 ) 
$$

## Matrix Calculus: Laplacian

Let $X$ be the space of $\mathbb{R}^{d\times d}$ matrices with zero trace. The **Laplacian**
of a twice differentiable function $g:X\to\mathbb{R}$ is defined by 
$$
\Delta_X g(A) = \sum_i \frac{\partial^2}{\partial E_i^2} g(A)
$$
where $E_i$ is an orthonormal basis of $X$ under the inner product $\langle A,B\rangle=\text{Tr}(A^\top B)$. The second **directional derivative** is define by 
$$
    \frac{\partial^2}{\partial E_i^2} g(A) = \frac{\partial^2}{\partial r^2} g(A+r E_i)\Bigg|_{r=0}
$$
