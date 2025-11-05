
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
2. i). 	
	 



## References
