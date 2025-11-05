
2025-11-05 14:58

Status: 

Tags:

# Schrodinger Equation
The Schrodinger Equation is a fundamental equation in quantum mechanics that describes how the quantum state of a physical system changes over time. It is named after the Austrian physicist Erwin Schrödinger, who formulated it in 1925.
$$i\hbar \frac{\partial}{\partial t} |\Psi_t \rangle = \hat{H} |\Psi_t \rangle$$
Where:
- $i$ is the imaginary unit. It causes some problems with interpretation, but is essential for the mathematics of quantum mechanics.
- $\hbar$ is the reduced Planck's constant.
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




## References
