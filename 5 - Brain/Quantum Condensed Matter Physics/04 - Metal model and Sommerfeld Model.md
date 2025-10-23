
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
##### Schrödinger Equation for Free Electrons
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
##### Periodic Boundary Conditions
This conditions are also called Born–von Karman boundary conditions. They state that the wavefunction must be periodic in space, meaning that:
$$\psi (x, y, z) = \psi (x + L_x, y, z) = \psi (x, y + L_y, z) = \psi (x, y, z + L_z)$$
Applying these conditions to the plane wave solutions, remembering that:
$$ \vec{k} = (k_x, k_y, k_z) \quad \Rightarrow \quad \frac{1}{\sqrt{V}} e^{i (k_x x + k_y y + k_z z)} = \frac{1}{\sqrt{V}} e^{i (k_x (x + L_x) + k_y y + k_z z)} = \frac{1}{\sqrt{V}} e^{i (k_x x + k_y (y + L_y) + k_z z)} = \frac{1}{\sqrt{V}} e^{i (k_x x + k_y y + k_z (z + L_z))}$$
From the first equality, we have:
$$e^{i k_x x} = e^{i k_x (x + L_x)} \quad \Rightarrow \quad e^{i k_x L_x} = 1 \quad \Rightarrow \quad k_x L_x = 2 \pi n_x$$
Where  is an integer. Using a similar process for the second and third equalities, we find that the allowed wavevectors must satisfy:
$$k_x = \frac{2 \pi n_x}{L_x}, \quad k_y = \frac{2 \pi n_y}{L_y}, \quad k_z = \frac{2 \pi n_z}{L_z}$$
Where $n_x$, $n_y$, and $n_z$ are integers (positive, negative, or zero). This quantization of the wavevectors means that the electrons can only occupy discrete states in momentum space, which leads to a discrete energy spectrum(it's easy to see this from the energy relation we found earlier). 
But, in this particular case, the spacing between these allowed wavevectors is very small because the dimensions of the metal are macroscopic (on the order of centimeters or larger). This means that the allowed wavevectors are very closely spaced, and we can treat them as a continuous distribution for practical purposes.
We can imagine it as a parabola, where each point on the parabola represents an allowed energy state in which the electrons can exist. The electrons will fill these states starting from the lowest energy level, following the Pauli exclusion principle. The possible energy states can be referred as possible wavefunctions considering the meaning of $\vec{k}$ explained later.
All the possible wavevectors represents the lattice points in k-space, where the limit of the lattice points is determined by the maximum energy of the electrons in the metal(easily found considering the Fermi energy, the highest occupied energy level at absolute zero temperature). They create a sphere after occupying all the possible energy states up to the Fermi energy, known as the Fermi sphere.
In we consider the Hydrogen atom, the P-orbitals are an example of quantized energy levels due to the Coulomb potential. In that case, the electrons can only occupy 3 discrete energy levels corresponding to the three p-orbitals (px, py, pz). This happens because the energy levels corresponding to the p-orbitals are degenerate, meaning they have the same energy but different spatial orientations. 
##### What is $\vec{k}$?(Not important for the exam, but important for me)
The wavevector $\vec{k}$ is a vector quantity that describes the spatial variation of the electron's wavefunction. It is related to the momentum of the electron by the relation:
$$\vec{p} = \hbar \vec{k}$$
Where $\vec{p}$ is the momentum of the electron. The magnitude of the wavevector $k$ is related to the wavelength $\lambda$ of the electron wave by the relation:
$$k = \frac{2 \pi}{\lambda}$$
This means that the wavevector determines the wavelength of the electron wave, and thus its momentum and energy.
The direction of the wavevector indicates the direction of propagation of the electron wave. In three dimensions, the wavevector has components in the x, y, and z directions, which determine how the wavefunction varies in each spatial dimension.
The number of allowed wavevectors in a given volume of momentum space can be calculated by considering the spacing between the allowed wavevectors. In three dimensions, the allowed wavevectors form a cubic lattice in momentum space, with a spacing of:
$$\Delta k_x = \frac{2 \pi}{L_x}, \quad \Delta k_y = \frac{2 \pi}{L_y}, \quad \Delta k_z = \frac{2 \pi}{L_z}$$
The number $2 \pi$ comes from the periodic boundary conditions we applied earlier.
This means that the volume of each allowed state in momentum space is given by:
$$\Delta k_x \Delta k_y \Delta k_z = \frac{(2 \pi)^3}{V}$$
Where $V = L_x L_y L_z$ is the volume of the metal. Therefore, the number of allowed wavevectors in a given volume of momentum space $d^3k$ is given by:
$$\frac{V}{(2 \pi)^3} d^3k$$
This all allows us to calculate the density of states and other properties of the electron gas in the metal.
To recap, the large number of atoms influences the number of allowed wavevectors because each atom contributes electrons that can occupy these states. The periodic boundary conditions lead to quantized wavevectors, but due to the macroscopic size of the metal, the spacing between these wavevectors is very small, allowing us to treat them as a continuous distribution. This results in a high density of states in momentum space, which is crucial for understanding the electronic properties of metals.
The orbits in k-space are filled according to the Pauli exclusion principle, which states that no two electrons can occupy the same quantum state simultaneously. This means that each allowed wavevector can be occupied by at most two electrons (one with spin up and one with spin down). 
Basically two electrons can have the same energy only if they have opposite spins or they occupy different wavevectors(this are called quantum numbers). 
When two electrons have the same energy, in a continuous energy spectrum, they lie on the same energy band, but their occupation is determined by their wavevectors and spins.
##### Density of States
The density of states represents the number of available electronic states per unit energy range at a given energy level. It is a crucial concept in solid-state physics because it helps us understand how electrons are distributed among the available energy levels in a material.
Basically, if we represents the energy levels as a graph, using the results from before, the graph would be a parabola($E = \frac{\hbar^2 k^2}{2m}$). The density of states tells us how many states are available at each energy level along this graph, meaning that the density of states indicates the number of states when you take a slice of the graph at a specific energy value(y-axis) and count how many states fall within that slice. For example at $E_0$, you will hit just one point, meaning it has two states(considering spin).
The density of states is given by the formula:
$$D(E) = \frac{1}{V} \frac{dN(E)}{dE}$$
Where $D(E)$ is the density of states at energy $E$, $V$ is the volume of the metal, and $N(E)$ is the total number of states with energy less than or equal to $E$.
The volume of each lattice point in k-space is given by:
$$\frac{(2 \pi)^3}{L_xL_yL_z}=\frac{(2 \pi)^3}{V}$$
This comes from the periodic boundary conditions we applied earlier, which quantize the allowed wavevectors in momentum space.
To find $N(E)$, we can divide the total volume of the sphere in k-space (up to the wavevector corresponding to energy $E$) by the volume of each lattice point(energy state):
$$N(E) = 2 \cdot \frac{\frac{4}{3} \pi k^3}{\frac{(2 \pi)^3}{V}} = \frac{V}{3 \pi^2} k^3$$
Where the factor of 2 accounts for the two possible spin states for each wavevector.
To express $N(E)$ in terms of energy, we can use the relation between energy and wavevector:
$$E = \frac{\hbar^2 k^2}{2m} \quad \Rightarrow \quad k = \sqrt{\frac{2mE}{\hbar^2}}$$
Substituting this expression for $k$ into the equation for $N(E)$, we get:
$$N(E) = \frac{V}{3 \pi^2} \left( \sqrt{\frac{2mE}{\hbar^2}} \right)^3 = \frac{V}{3 \pi^2} \left( \frac{2mE}{\hbar^2} \right)^{3/2}$$
Now we can substitute this expression for $N(E)$ into the formula for the density of states:
$$D(E) = \frac{1}{V} \frac{d}{dE} \left( \frac{V}{3 \pi^2} \left( \frac{2mE}{\hbar^2} \right)^{3/2} \right) = \frac{1}{V} \cdot \frac{V}{3 \pi^2} \cdot \frac{3}{2} \left( \frac{2m}{\hbar^2} \right)^{3/2} E^{1/2} = \frac{1}{2 \pi^2} \left( \frac{2m}{\hbar^2} \right)^{3/2} E^{1/2}$$
This expression shows that the density of states increases with the square root of energy, meaning that there are more available states at higher energy levels. So at higher energies there will be more degenerate states. 
This results tells nothing about the occupation of these states, which is determined by the Fermi-Dirac distribution. It only tells us the probability of finding an electron at a given energy level and temperature.
##### Fermi-Dirac Distribution
The Fermi-Dirac distribution describes the probability that an electron occupies a given energy state at a specific temperature. It is given by the formula:
$$f(E, T) = \frac{1}{1 + e^{(E - E_F) / (k T)}}$$
Where $f(E, T)$ is the probability of occupation of an energy state with energy $E$ at temperature $T$, $E_F$ is the Fermi energy (the highest occupied energy level at absolute zero temperature), $k$ is the Boltzmann constant, and $T$ is the absolute temperature.
If we plot the Fermi-Dirac distribution as a function of energy for different temperatures, we observe the following behavior:
1. At absolute zero temperature (T = 0 K), the distribution is a step function. All energy states below the Fermi energy are fully occupied (f(E) = 1), while all states above the Fermi energy are empty (f(E) = 0).
2. As the temperature increases, the step function smooths out. Some electrons gain enough thermal energy to occupy states above the Fermi energy, while some states below the Fermi energy become unoccupied.
This results in a gradual transition from occupied to unoccupied states around the Fermi energy.
##### Combining Density of States and Fermi-Dirac Distribution
To find the total number of electrons in the metal at a given temperature, we can combine the graphs of the density of states and the Fermi-Dirac distribution. 
If we plot the product $D(E) f(E, T)$ as a function of energy, we obtain a curve that represents the effective number of occupied states at each energy level. The area under this curve corresponds to the total number of electrons in the metal. 
1. At low temperatures, the area under the curve is concentrated around the Fermi energy, as most electrons occupy states near this energy level.
2. As the temperature increases, the area spreads out, reflecting the increased occupation of higher energy states and the decreased occupation of lower energy states. Some states below the Fermi energy become unoccupied, while states above the Fermi energy become occupied.

There's no Bravais Lattice since the metal is considered as a free electron gas without a periodic potential from the lattice structure. 

The total number of electrons $N$ can be calculated by integrating the product of the density of states and the Fermi-Dirac distribution over all energy levels:
$$N = \int_0^\infty D(E) f(E, T) dE$$
This integral gives us the total number of electrons by summing up the contributions from all energy states, weighted by their occupation probabilities. The total number of electrons remains constant since electrons are just excited not created. 
We define Heat Capacity as the amount of heat needed to change the temperature of a substance by a certain amount in time. So a large heat capacity means that the substance can absorb a lot of heat without a significant change in temperature. It is possible to calculate the heat capacity due to the electrons in the metal, it will be little since only electrons near the Fermi energy can be excited and contribute to the heat capacity.
##### Adding an Electric Field 
At start the sphere in the k-space is centered at the origin, meaning that the average momentum of the electrons is zero. More specifically we have the same numbers of electrons with same velocity in opposite directions, so the net momentum is zero $-\hbar |\vec{k}| + \hbar |\vec{k}| = 0$. 
When we apply an electric field $\vec{E}$, the electrons experience a force $\vec{F} = -e \vec{E}$, where $e$ is the elementary charge. This force causes the electrons to accelerate in the direction opposite to the electric field (since electrons are negatively charged).
$$\vec{F} = \frac{d\vec{p}}{dt} = \hbar \frac{d\vec{k}}{dt} = -e \vec{E} \quad \Rightarrow \quad \frac{d\vec{k}}{dt} = -\frac{e \vec{E}}{\hbar}$$
This equation describes how the wavevector $\vec{k}$ of the electrons changes over time under the influence of the electric field. The negative sign indicates that the wavevector decreases in the direction of the electric field.
By integrating this equation over the k-space, we find that the entire Fermi sphere shifts in the direction opposite to the electric field. This shift represents a net momentum of the electrons in that direction, leading to a net current flow in the metal.
$$\hbar d\vec{k} = -e \vec{E} dt \quad \Rightarrow \quad \hbar (\vec{k(\epsilon)} - \vec{k(0)}) = -e \vec{E} t$$
Where $\vec{k(0)}$ is the initial wavevector and $\vec{k(\epsilon)}$ is the wavevector after a time interval $t$ under the influence of the electric field. So when we switch on the electric field, the momentum will change linearly with time(increase or decrease depending on the direction of the field).
$$\vec{k(\epsilon)} = \vec{k(0)} - \frac{e \vec{E}}{\hbar} t$$So the sphere will start to shift to higher or lower values of k infinitely(classically), but in reality, the electrons will scatter off impurities or phonons in the metal after a certain time or they will experience friction from the nuclei, which limits the maximum shift of the Fermi sphere. After a certain time, known as the collision time $\tau$, the electrons will scatter and lose their momentum, causing the Fermi sphere to reach a steady-state shift.
$$\Delta \vec{k} = -\frac{e \vec{E}}{\hbar} \tau \quad \Rightarrow \quad \Delta \vec{p} = m\Delta \vec{v} = \hbar \Delta \vec{k}$$
here $\Delta \vec{v} = \frac{\hbar}{m} \Delta \vec{k}$ is the change in velocity of the electrons due to the applied electric field.
The sphere will have a positive net flux in the direction opposite to the electric field, but only in the part of the sphere shifted out of the original sphere, while the part of the sphere that overlaps with the original sphere will have no net flux. We don't have a negative flux in the part once occupied by the sphere, so we have a positive net flux overall.
This electrons will then contribute to the electrical conductivity of the metal, as they move in response to the applied electric field. Not al electrons contribute, the ones with $- \hbar |\vec{k}|$ don't contribute since they are still in the original sphere.
So the average velocity is now greater than zero, leading to a net current flow in the metal. The new average velocity can be calculated as:
$$\Delta \vec{v} = \frac{\hbar}{m} \left()

## References
