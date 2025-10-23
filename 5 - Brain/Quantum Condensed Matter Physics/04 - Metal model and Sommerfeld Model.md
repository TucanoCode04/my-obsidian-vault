
2025-10-22 18:17

Status: 

Tags:

# Metal Model
We want to understand the behavior of electrons in metals. A common approach is to model the electrons as a free electron gas, where they move freely within the metal lattice, only occasionally scattering off impurities or lattice vibrations (phonons). 
This model is based on two main assumptions:
1. There's no Coulomb repulsion between electrons, meaning they don't interact with each other so we can treat them as independent particles.
2. The nuclei are considered fixed in place, providing a flat and constant potential background for the electrons, meaning we ignore any potential variations caused by the lattice structure and electrons are free to move.

The electrons are kept inside the metal by an infinite potential barrier at the surface, which prevents them from escaping. This is a simplification, but it allows us to focus on the behavior of electrons within the metal. 
The metal contains a large number of atoms, which we denote as $N \approx N_A$, where $N_A$ is Avogadro's number. 
So we describe the potential as:
$$V(x, y, z) =\begin{cases} 0 & 0< x < L_x, 0 < y < L_y, 0 < z < L_z \\ \infty & x \leq 0, x \geq L_x, y \leq 0, y \geq L_y, z \leq 0, z \geq L_z \end{cases}$$
Where $L_x$, $L_y$, and $L_z$ are the dimensions of the metal in the x, y, and z directions respectively.
The Schrödinger equation for a single electron in this potential is given by:
$$-\frac{\hbar^2}{2m} \nabla^2 \psi(\vec{r}) = E \psi(\vec{r})$$
Where $\hbar$ is the reduced Planck's constant, $m$ is the mass of the electron, $\psi(\vec{r})$ is the wavefunction of the electron, and $E$ is the energy of the electron. We don't include the potential term since it's zero inside the metal., and the kinetic energy operator for a free particle is $-\frac{\hbar^2}{2m} \nabla^2$.  
We look for the eigenfunctions and eigenvalues of this equation, which describe the allowed states and energies of the electrons in the metal.
The solutions to this equation are plane waves, meaning the electrons can be described as waves that propagate freely within the metal, with wavefunctions of the form:
$$\psi (\vec{r}) = \frac{1}{\sqrt{V}} e^{i \vec{k} \cdot \vec{r}}$$ Where $V = L_x L_y L_z$ is the volume of the metal used to normalize over the whole volume since the probabilities of each state must sum up to 1, and $\vec{k}$ is the wavevector of the electron, which determines its momentum and energy. To better explain what a wavevector is, we can look at the one-dimensional case:
$$\psi (x) = \frac{1}{\sqrt{L}} e^{i k x}$$
Where $k$ is the wavevector in the x-direction. The wavevector is related to the wavelength $\lambda$ of the electron wave by the relation:
$$k = \frac{2 \pi}{\lambda}$$
We can see that the wavevector determines the wavelength of the electron wave, and thus its momentum and energy.  
We can extract the energy of the electron from the Schrödinger equation:
$$E = \frac{\hbar^2 k^2}{2m}$$This relation shows that the energy of the electron is proportional to the square of its wavevector, which means that higher wavevectors correspond to higher energies. 
The plane wave are eigenfunctions of the momentum operator $\hat{p} = -i \hbar \nabla$, with eigenvalues given by:
$$\hat{p} \psi (\vec{r}) = \hbar \vec{k} \psi (\vec{r})$$
This means that the momentum of the electron is given by its wavevector, with a proportionality constant of $\hbar$. 
In free particle, we can, then, easily find the momentum and energy of the electron from its wavevector. This is possible because we assumed that the electrons are free and non-interacting, so by excluding a spatially varying potential, the Hamiltonian commutes with the momentum operator, allowing us to use plane waves as eigenfunctions.
$$[\hat{H}, \hat{p}] = 0 \quad \Rightarrow \quad \hat{H}= \frac{\hat{p}^2}{2m}$$
Again, this is possible only because we have no potential term in the Hamiltonian.

We will use boundary conditions, a mathematical constraint that represents a physical condition, to determine the allowed wavevectors of the electrons in the metal. In particular, we will assume that when the particle is at one end of the metal, it reappears at the other end. This is known as Periodic Boundary Conditions, and it is a common approximation used in solid-state physics to simplify calculations.


## References
