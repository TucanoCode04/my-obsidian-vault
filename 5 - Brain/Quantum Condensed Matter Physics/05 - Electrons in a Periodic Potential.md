
2025-10-23 12:26

Status: 

Tags:

# Electrons in a Periodic Potential
This model aims to describe the behavior of electrons in a crystalline solid, where the atoms are arranged in a periodic lattice structure. The periodic potential arises from the regular arrangement of positively charged atomic nuclei and the negatively charged electron cloud surrounding them. This periodic potential significantly influences the motion and energy levels of electrons within the solid.
We described the lattice using primitive vectors $\vec{a_1}, \vec{a_2}, \vec{a_3}$, which define the unit cell of the crystal. The position of each lattice point can be expressed as:
$$\vec{R_n} = n_1 \vec{a_1} + n_2 \vec{a_2} + n_3 \vec{a_3}$$
where $n_1, n_2, n_3$ are integers that index the lattice points. The periodic potential $V(\vec{r})$ satisfies the condition:
$$V(\vec{r} + \vec{R_n}) = V(\vec{r})$$
We consider a solid with a given volume $V = L_x L_y L_z$, containing $N_{TOT} = N_1 N_2 N_3$ unit cells, where $N_i = \frac{L_i}{a_i}$ is the number of unit cells along the $i$-th direction. 
##### Schrödinger Equation in a Periodic Potential
We want to solve the time-independent Schrödinger equation for an electron in this periodic potential:
$$\hat{H} \psi (\vec{r}) = \left[ -\frac{\hbar^2}{2m} \nabla^2 + V(\vec{r}) \right] \psi (\vec{r}) = E \psi (\vec{r})$$
where $\hat{H}$ is the Hamiltonian operator, $\psi (\vec{r})$ is the wave function of the electron, and $E$ is the energy eigenvalue. The potential $V(\vec{r})$ is periodic, reflecting the underlying lattice structure of the solid.
##### Bloch's Theorem
Bloch's theorem states that the wave functions of electrons in a periodic potential can be expressed as:
$$\psi_{\vec{k}} (\vec{r}) = e^{i \vec{k} \cdot \vec{r}} \mu_{\vec{k}} (\vec{r})$$
where $\vec{k}$ is the wave vector (or crystal momentum) and $\mu_{\vec{k}} (\vec{r})$ is a function(can be complex, so it can add a phase) that has the same periodicity as the lattice:
$$\mu_{\vec{k}} (\vec{r} + \vec{R_n}) = \mu_{\vec{k}} (\vec{r})$$
Different values of $\vec{k}$ correspond to different eigenstates of the electron in the periodic potential, meaning different energy levels $E(\vec{k})$(we don't have an explicit formula as in the Sommerfeld model). The allowed values of $\vec{k}$ are determined by the boundary conditions imposed on the wave function. We will see that is real and it will have discrete values.
We express now the Bloch function in terms of its periodic part:
$$\psi_{\vec{k}} (\vec{r + R_n}) = e^{i \vec{k} \cdot (\vec{r} + \vec{R_n})} \mu_{\vec{k}} (\vec{r} + \vec{R_n}) = e^{i \vec{k} \cdot \vec{R_n}} e^{i \vec{k} \cdot \vec{r}} \mu_{\vec{k}} (\vec{r}) = e^{i \vec{k} \cdot \vec{R_n}} \psi_{\vec{k}} (\vec{r})$$
So the Bloch function acquires a phase factor $e^{i \vec{k} \cdot \vec{R_n}}$ when translated by a lattice vector $\vec{R_n}$. So after the translation, we see equal states up to a phase factor.
##### Boundary Conditions and Allowed Wave Vectors
To determine the allowed values of the wave vector $\vec{k}$, we impose periodic boundary conditions on the wave function over the entire solid. This means that the wave function must be the same when translated by the dimensions of the solid, for example we analyze the $x$ direction:
$$\psi_{\vec{k}} (\vec{r} + L_x) = \psi_{\vec{k}} (\vec{r} + N_1 a_1) = \psi_{\vec{k}} (\vec{r}), \quad N_1 a_1 \in \{\vec{R_n}\}$$
Where $N_1$ is the number of unit cells in the $x$ direction and one of the infinite lattice vectors $\vec{R_n}$. This needs to satisfy the Bloch condition:
$$\Psi_{\vec{k}} (\vec{r} + N_1 a_1) = e^{i \vec{k} \cdot (N_1 a_1)} \psi_{\vec{k}} (\vec{r})$$
The two condition that needs to be satisfied are the PBC and the Bloch condition, so we have: 
$$e^{i \vec{k} \cdot (N_1 a_1)} = 1 \quad \Rightarrow \quad \vec{k} \cdot (N_1 a_1) = 2 \pi m_1, \quad m_1 \in \mathbb{Z}$$
The intuition behind this condition is that the phase factor must be an an integer multiple of $2\pi$ to ensure that the wave function remains single-valued and continuous across the boundaries of the solid. 
$\vec{k}$ can't be defined as a linear combination of the primitive vectors of the lattice $\vec{a_1}, \vec{a_2}, \vec{a_3}$, because $\vec{k}$ is defined in the reciprocal space. And $\vec{g_1}, \vec{g_2}, \vec{g_3}$ can't be defined as linear combinations of $\vec{a_1}, \vec{a_2}, \vec{a_3}$, we already defined them in the section about the Reciprocal Lattice. So we can express $\vec{k}$ as a linear combination of the primitive vectors of the reciprocal lattice:
$$\vec{k} = x_1 \vec{g_1} + x_2 \vec{g_2} + x_3 \vec{g_3}$$
We can't have a continuous range of values for $x_1, x_2, x_3$, because we need to satisfy the condition derived from the PBC. We calculate $x_1$:
$$\vec{k} \cdot (N_1 a_1) = (x_1 \vec{g_1} + x_2 \vec{g_2} + x_3 \vec{g_3}) \cdot (N_1 a_1) = x_1 N_1 (\vec{g_1} \cdot \vec{a_1}) + 0 + 0 = x_1 N_1 (2 \pi) = 2 \pi m_1 \quad \Rightarrow \quad x_1 = \frac{m_1}{N_1}$$
Where we used the definition of the reciprocal lattice vectors, so $\vec{g_i} \cdot \vec{a_j} = 2 \pi \delta_{ij}$. $m_1$ is an integer, that changes 
## References
