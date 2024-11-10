# Operator Identities

## Courant-Fischer-Weyl Theorem

Let $A:\mathbb{R}^d\to \mathbb{R}^d$ be a linear operator that is self-adjoint with respect 
to some inner proudct $\langle\cdot,\cdot\rangle$. Then the $k$-th largest eigenvalue of 
$A$ is 
$$
    \lambda_k(A)=\inf_U \sup_v\langle v,Av\rangle
$$

where the infimum is taken over all $(d-k+1)$-dimensional subspaces $U\subset\mathbb{R}^d$
and the supremum is taken over all $v\in U$ with $\langle v,v\rangle=1$.

## Weyl’s Inequality

Let $A, B:\mathbb{R}^d\to \mathbb{R}^d$ be a linear operator that is self-adjoint with respect 
to some inner proudct $\langle\cdot,\cdot\rangle$. Then the greatest eigenvalue $\lambda_1(\cdot)$ satisfies 

$$
\lambda_1(A+B)\leq \lambda_1(A) + \lambda_1(B)
$$

## Cauchy’s Interlacing Theorem 

For a symmetric matrix $A\in\mathbb{R}^{n\times n}$ and vector $v\in\mathbb{R}^n$, the eigenvalues of A interlace the eigenvalues of $B=A+ vv^\top$, i.e.

$$
\lambda_n(A) \leq \lambda_n(B) \leq  \lambda_{n-1}(A) \leq \lambda_{n-1}(B) \leq \dots \lambda_{1}(A) \leq \lambda_{1}(B)
$$

## Proposition

Let $A\in\mathbb{R}^{n\times n}$ be a symmetric matrix, and let $P\in\mathbb{R}^{m\times n}$.
If $A$ has at most one positive eigenvalue, then $PAP^\top$ has at most one positive eigenvalue.