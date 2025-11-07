
2025-11-06 18:55

Status: 

Tags:

# The Macroscopic Quantum Model
The London brothers, beginning from classical electrodynamics and assuming that superelectrons do not scatter, derived a partial description of the electrodynamics of superconductors. However the London equations do not account for the microscopic origins of superconductivity. 
Later, they were able to show that their equations could be derived from the Schrödinger equation by describing the superelectrons fluid with a macroscopic wave function. 
They realized that superconductivity is a quantum mechanical phenomenon that manifests itself on a macroscopic scale.
This concept is similar in laser physics, where a large number of photons occupy the same quantum state, leading to coherent light emission, sharing then the same wavefunction.
The hypothesis of the Macroscopic Quantum Model is that all superelectrons in a superconductor can be described by a single macroscopic wave function $\Psi (\vec{r}, t)$, which encapsulates the collective behavior of the superelectrons.
This assumption doesn't explain the microscopic origin of superconductivity, but it places importance on the collective quantum state of the superelectrons.
Like lasers that are described by a single electromagnetic wavefunction. 
So we assume the existence of a great number of charge carriers, making it more useful to consider $\Psi (\vec{r}, t)$ as describing a fluid of superelectrons rather than individual particles.
##### Schrodinger Equation and Macroscopic Quantum Currents
Let us consider the time-dependent Schrödinger equation for a charged particle in electric and magnetic fields:
$$
i \hbar \frac{\partial}{\partial t} \Psi (\vec{r}, t) = \frac{1}{2m} \left( -i \hbar \nabla - q \vec{A} (\vec{r}, t) \right)^2 \Psi (\vec{r}, t) + q \phi (\vec{r}, t) \Psi (\vec{r}, t) $$
where $q$ is the charge of the particle, $m$ is its mass, $\vec{A} (\vec{r}, t)$ is the vector potential, and $\phi (\vec{r}, t)$ is the scalar potential. The vector potential and scalar potential are related to the magnetic field $\vec{B}$ and electric field $\vec{E}$ by:
$$
\vec{B} = \nabla \times \vec{A} $$
$$
\vec{E} = - \nabla \phi - \frac{\partial \vec{A}}{\partial t} $$
We can express the macroscopic wave function $\Psi (\vec{r}, t)$ in terms of its modulus and phase:
$$
\Psi (\vec{r}, t) = \Psi_0 (\vec{r}, t) e^{i \theta (\vec{r}, t)} $$
where $\Psi_0 (\vec{r}, t)$ is the real-valued modulus with $\Psi_0(\vec{r}, t)= n_s(\vec{r},t)$ and $\theta (\vec{r}, t)$ is the real-valued phase of the wave function. Dropping the explicit space and time dependence for simplicity, we can substitute this expression into the Schrödinger equation:
$$
i \hbar \frac{\partial \Psi_0}{\partial t} - \hbar \Psi_0 \frac{\partial \theta}{\partial t} = \frac{1}{2m} \left[- \hbar^2 \left(\nabla^2 \Psi_0 + 2 i \nabla \theta \cdot \nabla \Psi_0 + i \Psi_0 \nabla^2 \theta - \Psi_0 (\nabla \theta)^2 \right) + 2i \hbar q \vec{A} \cdot \nabla \Psi_0 - 2 \hbar q \Psi_0 \vec{A} \cdot \nabla \theta + q^2 \vec{A}^2 \Psi_0 \right] + q \phi \Psi_0 $$
We now separate the real and imaginary parts of this equation. The imaginary part gives us:
$$
\hbar \frac{\partial \Psi_0}{\partial t} = - \frac{\hbar^2}{2m} \left[ \nabla^2 \theta \Psi_0 + 2 \nabla \theta \cdot \nabla \Psi_0 - \frac{q}{\hbar} \left(2 \vec{A} \cdot \nabla \Psi_0 + \nabla \cdot \vec{A} \Psi_0 \right) \right] $$


## References
