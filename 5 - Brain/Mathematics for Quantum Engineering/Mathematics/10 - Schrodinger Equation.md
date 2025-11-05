
2025-11-05 14:58

Status: 

Tags:

# Schrodinger Equation
The Schrodinger Equation is a fundamental equation in quantum mechanics that describes how the quantum state of a physical system changes over time. It is named after the Austrian physicist Erwin Schrödinger, who formulated it in 1925.
$$i\hbar \frac{\partial}{\partial t} |\Psi_t \rangle = \hat{H} |\Psi_t \rangle$$
Where:
- $i$ is the imaginary unit. It causes some problems with interpretation, but is essential for the mathematics of quantum mechanics.
- $\hbar$ is the reduced Planck's constant. We put $\hbar = 1$ for simplicity.
- $\partial t$ is the partial derivative with respect to time.
- $|\Psi_t \rangle$ is the state vector (or wavefunction) of the quantum system at time $t$.
- $\hat{H}$ is a self adjoint operator called the Hamiltonian, which represents the total energy of the system (kinetic + potential).

**Solving Schrödinger's Equation with a given initial datum**
What mathematicians call the Cauchy problem:
$$\begin{cases}
i \partial_t |\Psi_t \rangle = \hat{H} |\Psi_t \rangle, \\
|\Psi_0 \rangle \in \mathcal{V}, \quad \text{dim} \mathcal{V} = n < +\infty
\end{cases}$$
Where $\mathcal{V}$ is a finite-dimensional complex vector space.
$\hat{H}$ is self adjoint, so it is diagonalizable with real eigenvalues:
$$\exists \mathbf{B} = \{ | \xi_1 \rangle, | \xi_2 \rangle, \ldots, | \xi_n \rangle \} \text{ orthonormal basis of } \mathcal{V}, \quad \hat{H} | \xi_j \rangle = \lambda_j | \xi_j \rangle, \quad \lambda_j \in \mathbb{R}$$
For all $t \quad \exists c_j(t) \in \mathbb{C}$ such that:
$$|\Psi_t \rangle = \sum_{j=1}^n c_j(t) | \xi_j \rangle$$
In particular, at $t=0$:
$$|\Psi_0 \rangle = \sum_{j=1}^n c_j(0) | \xi_j \rangle$$
Substituting into the Schrodinger equation:
$$i \partial_t \left( \sum_{j=1}^n c_j(t) | \xi_j \rangle \right) = \hat{H} \left( \sum_{j=1}^n c_j(t) | \xi_j \rangle \right)$$
$$i \sum_{j=1}^n \partial_t c_j(t) | \xi_j \rangle = \sum_{j=1}^n c_j(t) \hat{H} | \xi_j \rangle = \sum_{j=1}^n c_j(t) \lambda_j | \xi_j \rangle$$
For all $t$:
$$\sum_{j=1}^n \left( i \partial_t c_j(t) - \lambda_j c_j(t) \right) | \xi_j \rangle = 0$$
By linear independence of the basis vectors $| \xi_j \rangle$:
$$i c_j(t) = \lambda_j \quad \Rightarrow \quad c_j(t) ) e^{-\frac{i}{\hbar} \lambda_j t}$$
Thus, the solution to the Schrodinger equation with initial condition $|\Psi_0 \rangle$ is:
$$|\Psi_t \rangle = \sum_{j=1}^n c_j(0) e^{-\frac{i}{\hbar} \lambda_j t} | \xi_j \rangle$$
Notation:
$$|\Psi_t \rangle = e^{-\frac{i}{\hbar} \hat{H} t} |\Psi_0 \rangle = U(t) |\Psi_0 \rangle$$ Where $U(t)$ is called propagator or unitary group associated to the system.

**Remark:** $e^{-\frac{i}{\hbar} \hat{H} t} = \sum_{n=0}^{\infty} \frac{1}{n!} \left( -\frac{i}{\hbar} \hat{H} t \right)^n$ is defined by the Taylor series. In infinite-dimensional spaces, the convergence of this series is not guaranteed for all operators $\hat{H}$. 
**Proof:** $$U(t) |\xi_j \rangle = e^{-\frac{i}{\hbar} \lambda_j t} |\xi_j \rangle = \sum_{n=0}^{\infty} \frac{1}{n!} \left( -\frac{i}{\hbar} \hat{H} t \right)^n |\xi_j \rangle = \sum_{n=0}^{\infty} \frac{1}{n!} \left( -\frac{i}{\hbar} \lambda_j t \right)^n |\xi_j \rangle$$
We know that $\lambda_j^n |\xi_j \rangle = \hat{H}^n | \xi_j \rangle$ by definition of eigenvalue.
Then by linearity,
$$U(t) |\Psi_0 \rangle = \sum_{j=1}^n c_j(0) U(t) |\xi_j \rangle = \sum_{j=1}^n c_j(0) \sum_{n=0}^{\infty} \frac{1}{n!} \left( -\frac{i}{\hbar} \hat{H} t \right)^n |\xi_j \rangle = \sum_{j=1}^n \frac{1}{n!} \left( -{i}{\hat{H}} t\right)^n |\Psi_0 \rangle$$
(Check it again).
#### Propagator properties
1. **Adjoint Map**: 
	 Proposition: $\mathbf{V}$ vector space, dim $\mathbf{V} = N < +\infty$. $T: \mathbf{V} \to \mathbf{V}$ linear map. $\exists$ the hermitian product defined in $\mathbf{V}$. Then exists and is unique($\exists !$) the adjoint map $T^{\dagger}: \mathbf{V} \to \mathbf{V}$ is defined by: 
	 $$\forall |v \rangle, |w \rangle \in \mathbf{V}, \quad \langle v | T w \rangle = \langle T^{\dagger} v | w \rangle$$
	 Def: The map $T$ is called adjoint of $T$.
	 Proof of the proposition: First we assume that such $T^{\dagger}$ exists and we prove its uniqueness. Let $|e_1 \rangle, |e_2 \rangle, \ldots, |e_N \rangle$ be an orthonormal basis of $\mathbf{V}$. Then, 
	 $$\langle e_j| T_{ek} \rangle = \langle T^{\dagger} e_j | e_k \rangle = \langle  e_k | T^{\dagger} e_j \rangle^*$$
	 We compute: 
	 $$T^{\dagger} |e_j \rangle = \sum_{k=1}^N |e_k \rangle \langle e_k | T^{\dagger} e_j \rangle = \sum_{k=1}^N |e_k \rangle \langle T e_k | e_j \rangle$$
	 This defines $T^{\dagger}$ uniquely on the basis. On the other hand, to prove the existence, we define $T^{\dagger}$ as above and we check that it satisfies the definition.
	 $$\forall|v \rangle, |w \rangle \in \mathbf{V}, \quad \text{with} \quad |v \rangle = \sum_{j=1}^N v_j |e_j \rangle, \quad |w \rangle = \sum_{k=1}^N w_k |e_k \rangle$$
	 $$\langle v  | T w \rangle = \sum_{j,k=1}^N v_j^* w_k \langle e_j | T e_k \rangle $$
	 Let us prove that:
	 $$\langle e_j | T e_k \rangle = \langle T^{\dagger} e_j | e_k \rangle$$
	 Indeed,
	 $$\langle T^{\dagger} e_j | e_k \rangle = \left(\sum_{l=1}^N \langle e_l | \langle e_j | T e_l \rangle \right) | e_k \rangle = \sum_{l=1}^N \delta_{l k} \langle e_j | T e_l \rangle = \langle e_j | T e_k \rangle$$
	 So,
	 $$\langle v | T w \rangle = \sum_{j,k=1}^N v_j^* w_k \langle T^{\dagger} e_j | e_k \rangle = \sum_{j,k=1}^N v_j^* w_k \langle e_k | T^{\dagger} e_j \rangle^* = \langle T^{\dagger} v | w \rangle$$
	 **Remark:** The logic of the proof is that if T† exists, it must act as defined on the basis. The map defined in this way fulfils the definition of adjoint.
	 **Remark:** $\forall S,T : \mathbf{V} \to \mathbf{V}$ linear maps, we have:
	 $(ST)^{\dagger} = S^{\dagger} T^{\dagger}$
	 Indeed, $\langle v | ST w \rangle = \langle S^{\dagger} v | T w \rangle = \langle T^{\dagger} S^{\dagger} v | w \rangle$
2. (i) Time evolution preserves the Hermitian product: $$\forall |\phi_0 \rangle, |\psi\rangle \in V \Rightarrow \langle U(t) \phi_0 | U(t) \psi_0 \rangle = \langle \phi_0 | \psi_0 \rangle$$ (ii) The norm is preserved: $$\forall |\psi_0 \rangle \in V \Rightarrow || U(t) \psi_0 || = || \psi_0 ||$$ (iii) $U(t)$ maps orthonormal bases into orthonormal bases.
	(iv) $U(t)$ is a unitary operator: $$U(t)^{\dagger} U(t) = I$$ Where $I$ is the identity operator.
	(v) $U(t)^{\dagger} U(t) = U(t) U(t)^{\dagger}$
	**Proof:** (i) $\Rightarrow$ (ii) is immediate by definition of norm. 
	(ii) $\Rightarrow$ (i): By polarization identity:
	$$\langle v | w \rangle = \frac{1}{4} \left( || v + w ||^2 - || v - w ||^2 + i || v + i w ||^2 - i || v - i w ||^2 \right)$$
	$$\langle U(t) v | U(t) w \rangle = \frac{1}{4} \left( || U(t) v + U(t) w ||^2 - || U(t) v - U(t) w ||^2 + i || U(t) v + i U(t) w ||^2 - i || U(t) v - i U(t) w ||^2 \right) = \langle v | w \rangle$$
	(i) $\Rightarrow$ (iii) is immediate by definition of orthonormal basis.
	(iii) $\Rightarrow$ (i): Consider an orthonormal basis $\{ | \xi_1\rangle, | \xi_2 \rangle, \ldots, | \xi_n \rangle \}$. Then, $\{|\eta_1 \rangle = U(t) |\xi_1 \rangle, |\eta_2 \rangle, \ldots, |\eta_n \rangle \}$ is also an orthonormal basis. Where $|\eta_i\rangle = U(t) |\xi_i U(t) |\xi_i \rangle$. Then, for $v = \sum_{j=1}^n v_j |\xi_j \rangle$ and $w = \sum_{k=1}^n w_k |\xi_k \rangle$:
	$$\langle U(t) v | U(t) w \rangle = \sum_{j,k=1}^n v_j^* w_k \langle U(t) \xi_j | U(t) \xi_k \rangle = \sum_{j,k=1}^n v_j^* w_k \delta_{jk} = \langle v | w \rangle$$
	(i) $\Rightarrow$ (iv): By definition of adjoint map:
	$$\langle U(t) v | U(t) w \rangle = \langle v| U(t)^{\dagger} U(t) w \rangle$$
	Choose an orthonormal basis $\{ |e_1 \rangle, |e_2 \rangle, \ldots, |e_n \rangle \}$ and compute the matric that in the basis represents $U(t)^{\dagger} U(t)$. Let $M$ be this matrix. Then,
	$$M_{ij} = \langle e_i | U(t)^{\dagger} U(t) | e_j \rangle = \langle e_i | e_j \rangle = \delta_{ij}$$
	So, $M = I$ and thus $U(t)^{\dagger} U(t) = I$.
	(iv) $\Rightarrow$ (i): By definition of adjoint map:
	Assume that $U(t)^{\dagger} U(t) = I$. Let $|v \rangle, |w \rangle \in V$. Then,
	$$\langle U(t) v | U(t) w \rangle = \langle v | U(t)^{\dagger} U(t) w \rangle = \langle v | w \rangle$$
	(iv) $\Rightarrow$ (v): Taking the adjoint of both sides of $U(t)U(t)^{\dagger} = I$, we get:
	$$U(t) U(t)^{\dagger} U(t) = U(t) \Rightarrow U(t) U(t)^{\dagger} U(t) - U(t) = 0 \Rightarrow U(t) (U(t)^{\dagger} U(t) - I) = 0$$
	Let $|\xi_1\rangle, |\xi_2 \rangle, \ldots, |\xi_n \rangle$ be an be orthonormal basis. $|\eta_j \rangle = U(t) |\xi_j \rangle$. Then,
	$$U(t) (U(t)^{\dagger} U(t) - I) |\xi_j \rangle = U(t) (U(t)^{\dagger} |\eta_j \rangle - |\xi_j \rangle) = |\eta_j \rangle - |\eta_j \rangle = 0$$
	Thus, $U(t)^{\dagger} U(t) = I$.
	(v) $\Rightarrow$ (iv): The same as above.
	 **Definition:** A linear map in finite dimension that satisfies the equivalent properties (i)-(v) is called a unitary operator.
	 **Remark:** The Schrödinger propagators U(t) are unitary operators for all t.
	 **Remark:** In infinite-dimension unitary is more delicate. Consider the space $l^2= \{ |e_1\rangle, |e_2\rangle, \ldots) \}$ dim $= +\infty$. $\langle e_j | e_k e_k \rangle = \delta_{jk}$. 
	 $\forall|v\rangle \in l^2, \quad \exists c_j \in \mathbb{C}$ such that $$|v \rangle = \sum_{j=1}^{\infty} c_j |e_j \rangle, \quad \langle v | v \rangle = \sum_{j=1}^{\infty} |c_j|^2 < +\infty$$
	 $$W: l^2 \to l^2, \quad W |e_j \rangle = |e_{2j} \rangle$$
	 Then, 
	$$\langle W u | W v \rangle = \sum_{j=1}^{\infty} u_j^* v_j = \langle u | v \rangle$$So, W preserves the Hermitian product. But for example (iii) is not true, because the image of the basis $\{ |e_1 \rangle, |e_2 \rangle, \ldots \}$ is $\{ |e_2 \rangle, |e_4 \rangle, \ldots \}$ which is not a basis of $l^2$.
	**Remark:** to proved that $|e_1 \rangle$ cannot be generated by $\{ W|e_1 \rangle, W |e_2 \rangle, \ldots \}$, one can show that:
	$$\langle e_1 | W|e_j \rangle = \langle_1 | \sum_{k=1}^{\infty} v_k |e_k \rangle = \sum_{k=1}^{\infty} v_k \langle e_1 | e_{2k} \rangle = 0, \quad \forall |v\rangle \in l^2 $$
	On the other hand we can prove (iii) $\Rightarrow$ (i). If dim V = +$\infty$, one defines unitary operators as those that satisfy (iii). $U(t) = U(t)^{\dagger} U(t) = I$.
	**Remark:** $U(t) U(t)^{\dagger} = U(t)^{\dagger} U(t) = I \Rightarrow [U(t), U(t)^{\dagger}] = 0$
	For Schrodinger propagators, if $\{|\xi_1\rangle, |\xi_2 \rangle, \ldots, \xi_n \rangle \}$ is an orthonormal basis of eigenvectors of $\hat{H}$, then }



## References
