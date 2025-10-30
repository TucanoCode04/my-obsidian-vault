
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
$$f(\vec{k}, \vec{r}, t) \cdot d\vec{k} \cdot d\vec{r} \frac{V}{(2\pi)^3} \cdot 2 \cdot \frac{1}{V}$$ gives the number of electrons in the volume element $d\vec{r}$ around position $\vec{r}$ and in the momentum space volume $d\vec{k}$ around wave vector $\vec{k}$. Here, $V$ is the total volume of the system, the factor $\frac{V}{(2\pi)^3}$ is the density of allowed states in $\vec{k}$-space per unit volume in real space, the factor 2 accounts for the spin degeneracy of electrons, and $\frac{1}{V}$ normalizes the count to per unit volume.




## References
