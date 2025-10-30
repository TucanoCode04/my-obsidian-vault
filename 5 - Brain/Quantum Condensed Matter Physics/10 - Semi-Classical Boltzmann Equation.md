
2025-10-30 16:26

Status: 

Tags:

# Semi-Classical Boltzmann Equation
The semi-classical Boltzmann equation is a fundamental equation in statistical mechanics that combines the classical position and momentum of particles with quantum mechanical principles. It is used to describe the statistical behavior of a thermodynamic system out of equilibrium.
If we imagine the Fermi sphere in momentum space, where each point inside the sphere represents an occupied quantum state by an electron. Their occupation is described by the Fermi-Dirac distribution function, which gives the probability of occupation of each state at a given temperature.
$$f_0(\vec{k}, T) = \frac{1}{e^{\frac{E(\vec{k}) - \mu}{k_B T}} + 1}$$ where $E(\vec{k})$ is the energy of the state with wave vector $\vec{k}$, $\mu$ is the chemical potential, $k_B$ is the Boltzmann constant, and $T$ is the temperature. We call it $f_0$ to indicate that it is the equilibrium distribution function. 
The $\vec{k}$ vector is related to the momentum $\vec{p}$ by $\vec{p} = \hbar \vec{k}$, where $\hbar$ is the reduced Planck constant.
When an external perturbation, such as an electric field, is applied to the system, the sphere shifts in momentum space in the opposite direction of the applied field, so that the occupancy of states changes. This shift should, in theory, be infinite, but in practice, scattering events (like electron-phonon interactions) limit this shift, leading to a new steady-state distribution function $f(\vec{k}, \vec{r}, t)$ that deviates from the equilibrium distribution $f_0$.
Now the states which were previously occupied may become unoccupied, and vice versa. This change in occupancy leads to a net flow of electrons, which manifests as an electric current.
This new distribution function is dependent on $\vec{k}$, which are the new momenta of the electrons, $\vec{r}$, which is the position in real space because different regions may experience different fields or gradients, and time $t$, as the system evolves towards a new steady state. The system has then 7 variables: 3 for $\vec{k}$, 3 for $\vec{r}$, and 1 for $t$. 
$$f(\vec{k}, \vec{r}, t) \cdot d\vec{k} \cdot d\vec{r} \frac{V}{(2\pi)^3} \cdot 2 \cdot \frac{1}{V} = f(\vec{k}, \vec{r}, t) \cdot \frac{1}{4\pi^3} d\vec{k} \cdot d\vec{r}$$

gives the number of electrons in the volume element $d\vec{r}$ around position $\vec{r}$ and in the momentum space volume $d\vec{k}$ around wave vector $\vec{k}$. Here, $V$ is the total volume of the system, the factor $\frac{V}{(2\pi)^3}$ is the density of allowed states in $\vec{k}$-space per unit volume in real space, the factor 2 accounts for the spin degeneracy of electrons, and $\frac{1}{V}$ normalizes the count to per unit volume.
We now apply the electric field $\vec{E}$ to the system. The electrons experience a force $\vec{F} = -e \vec{E}$, where $e$ is the elementary charge.
The semi-classical approach describes the changes in position and momentum of the electrons:
$$\vec{r} \rightarrow \vec{r'} = \vec{r} + \vec{v} dt$$
$$\vec{k}; \quad \vec{p} = \hbar \vec{k} \rightarrow \hbar \vec{k'} = \hbar \vec{k} + \hbar d\vec{k} = \hbar \vec{k} + d\vec{p} = \hbar \vec{k} + \vec{F} dt$$
$$\vec{k'} = \vec{k} + \frac{\vec{F}}{\hbar} dt $$
where $\vec{v}$ is the group velocity of the electrons, given by $\vec{v} = \frac{1}{\hbar} \nabla_{\vec{k}} E(\vec{k})$. So our system evolves as:
$$f(\vec{r}, \vec{k}, t) \rightarrow f(\vec{r} + \vec{v} dt, \vec{k} + \frac{\vec{F}}{\hbar} dt, t + dt)$$
We define the volume element as $d\Omega$ that evolves into $d\Omega'$ after time $dt$. 
//GRAPH
The number of electrons in this volume element must be conserved if there are no scattering events, so:
$$f(\vec{r}, \vec{k}, t) = f(\vec{r} + \vec{v} dt, \vec{k} + \frac{\vec{F}}{\hbar} dt, t + dt)$$
If this was true the sphere would drift infinitely. Electrons in a periodic potential are represented by Bloch waves, which are delocalized states that extend throughout the crystal lattice, so they are not subject to localization due to scattering. However, in reality, scattering events occur due to impurities, phonons, and other electrons, which randomize the momentum of the electrons and prevent indefinite drift.
To describe an example, a particle in the volume element $d\Omega$ at time $t$ may collide with a phonon exchanging momentum and energy, and thus leave the volume element $d\Omega$ before time $t + dt$. Conversely, another particle from outside $d\Omega$ may scatter into it. These scattering events change the probability of finding particles in the volume element $d\Omega'$ over time.

## References
