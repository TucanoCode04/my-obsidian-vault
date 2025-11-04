
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
To describe an example, a particle in the volume element $d\Omega$ at time $t$ may collide with a phonon exchanging momentum and energy, and thus leave the volume element $d\Omega$ before time $t + dt$. Conversely, another particle from outside $d\Omega$ may scatter into it. These scattering events change the number of particles in $d\Omega$ over time. Changing the probability distribution function $f$ over time due to scattering can be expressed as:
$$f(\vec{r} + \vec{v} dt, \vec{k} + \frac{\vec{F}}{\hbar} dt, t + dt) - f(\vec{r}, \vec{k}, t) = \left( \frac{\partial f}{\partial t} \right)_{collision} dt$$
where:
$$\left( \frac{\partial f}{\partial t} \right)_{collision} = \left( \frac{\partial f}{\partial t} \right)_{collision}^{in} - \left( \frac{\partial f}{\partial t} \right)_{collision}^{out}$$
Combining all together, we get:
$$df = f(\vec{r} + \vec{v} dt, \vec{k} + \frac{\vec{F}}{\hbar} dt, t + dt) - f(\vec{r}, \vec{k}, t) = \frac{\partial f}{\partial \vec{r}} \cdot d\vec{r} + \frac{\partial f}{\partial \vec{k}} \cdot d\vec{k} + \frac{\partial f}{\partial t} dt$$
Dividing by $dt$ and substituting $d\vec{r} = \vec{v} dt$ and $d\vec{k} = \frac{\vec{F}}{\hbar} dt$, we obtain the semi-classical Boltzmann equation:
$$\frac{\partial f}{\partial t} + \vec{v} \cdot \nabla_{\vec{r}} f + \frac{\vec{F}}{\hbar} \cdot \nabla_{\vec{k}} f = \left( \frac{\partial f}{\partial t} \right)_{collision}$$
This equation describes how the distribution function $f$ evolves over time due to the combined effects of particle motion in real space, changes in momentum space due to external forces, and scattering events. It is a powerful tool for analyzing transport phenomena in materials, such as electrical conductivity, thermal conductivity, and more. It is called Boltzmann Transport Equation (BTE).
This is a integral differential equation, as the collision term on the right-hand side is an integral and we want to integrate the other side to know the distribution function $f$.
##### Electron-Phonon Collision Out Term
We can use the Fermi Golden Rule to calculate the collision term, which gives the transition rate describing how electrons in a quantum state identified by the wave vector $\vec{k}$ scatter into a quantum state identified by $\vec{k'}$ due to a perturbation, such as electron-phonon interaction.
$$W_{\vec{k} \rightarrow \vec{k'}} \cdot dt \cdot d\vec{k'} \cdot \frac{V}{(2\pi)^3} \cdot \frac{1}{V} = W_{\vec{k} \rightarrow \vec{k'}} \cdot \frac{1}{4\pi^3} dt \cdot d\vec{k'}$$
gives the probability that electrons in state $\vec{k}$ will scatter into a state within the volume element $d\vec{k'}$ around $\vec{k'}$ during time $dt$. We don't multiply by 2 because during scattering the spin is conserved.
I need to integrate over all possible final states $\vec{k'}$ because I don't know where the electrons will scatter to, additionally I need also to check if $\vec{k}$ is filled and $\vec{k'}$ is empty to check the occupation:
$$- \int d\vec{k'} \cdot W_{\vec{k} \rightarrow \vec{k'}} \cdot f(\vec{k}) \cdot (1 - f(\vec{k'})) \cdot \frac{1}{(2\pi)^3} = \left( \frac{\partial f}{\partial t} \right)_{collision}^{out} $$
This term represents the rate at which electrons leave the state $\vec{k}$ due to scattering into other states $\vec{k'}$. The factor $f(\vec{k})$ ensures that there is an electron in the initial state, while $(1 - f(\vec{k'}))$ ensures that the final state is unoccupied. The minus sign indicates that we are only counting electrons leaving the state $\vec{k}$, so collision out.
##### Electron-Phonon Collision In Term
To calculate the collision in term, we consider electrons that scatter from other states $\vec{k'}$ into the state $\vec{k}$. 
$$+ \int d\vec{k'} \cdot W_{\vec{k'} \rightarrow \vec{k}} \cdot f(\vec{k'}) \cdot (1 - f(\vec{k})) \cdot \frac{1}{(2\pi)^3} = \left( \frac{\partial f}{\partial t} \right)_{collision}^{in} $$
This term represents the rate at which electrons enter the state $\vec{k}$ from other states $\vec{k'}$. The factor $f(\vec{k'})$ ensures that there is an electron in the initial state $\vec{k'}$, while $(1 - f(\vec{k}))$ ensures that the final state $\vec{k}$ is unoccupied. The plus sign indicates that we are counting electrons entering the state $\vec{k}$, so collision in.

To put it all together, the total collision term is:
$$\left( \frac{\partial f}{\partial t} \right)_{collision} = \int d\vec{k'} \cdot \left[ W_{\vec{k'} \rightarrow \vec{k}} \cdot f(\vec{k'}) \cdot (1 - f(\vec{k})) - W_{\vec{k} \rightarrow \vec{k'}} \cdot f(\vec{k}) \cdot (1 - f(\vec{k'})) \right] \cdot \frac{1}{(2\pi)^3}$$
It is hard to solve the BTE because the collision term is an integral over all possible final states, making it an integro-differential equation. Additionally, the transition rates $W_{\vec{k} \rightarrow \vec{k'}}$ depend on the specific scattering mechanisms involved, which can be complex and material-dependent. We then introduce approximations to make it solvable.
**Independent Electron Approximation**: We assume that electrons scatter independently, ignoring electron-electron interaction(Coulomb interaction). We only look at scattering events due to deviations from the strict periodic potential of the crystal lattice, such as:
- Defects(vacancies, impurities): We can have a localized perturbation $\vec{R}_i$ in the crystal potential. This is normally time independent, since defects don't move.
- Phonons: Lattice vibrations that can absorb or emit energy and momentum during scattering events. Waves that propagate through the crystal. They are time dependent. For lower temperatures 

The scattering rate due to defects can be calculated using Fermi's Golden Rule, considering the perturbation introduced by the defects. 
$$W_{\vec{k} \rightarrow \vec{k'}}^{defects} = \frac{2\pi}{\hbar} | \langle \vec{k'} | U_{defects} | \vec{k} \rangle |^2 \delta(E(\vec{k'}) - E(\vec{k}))$$
where $U_{defects}$ is the potential due to defects, and the delta function ensures energy conservation during scattering. We now that the scattering is elastic because defects are static, so the energy before and after scattering is the same $E(\vec{k'}) = E(\vec{k})$, it only changes momentum.
$U_{defects}$ can be modeled as an integral of localized perturbations due to defects:
$$| \langle \vec{k'} | U_{defects} | \vec{k} \rangle = \int d\vec{r} \cdot \psi_{\vec{k'}}^*(\vec{r}) U_{defects}(\vec{r} - \vec{R}_i) \psi_{\vec{k}}(\vec{r})$$
where $\psi_{\vec{k}}(\vec{r})$ are the Bloch wavefunctions of the electrons. $\vec{R}_i$ are the positions of the defects in the crystal lattice. 
The scattering rate due to phonons can also be calculated using Fermi's Golden Rule. Phonons can be seen as sound waves propagating through the crystal lattice, which are described as:
$$\mu = A e^{i(\vec{q} \cdot \vec{r} - \omega t)}$$ where $\vec{q}$ is the phonon wave vector, $\omega$ is the angular frequency, and $A$ is the amplitude of the wave. 
$$W_{\vec{k} \rightarrow \vec{k'}}^{phonons} \propto \delta(E(\vec{k'}) - E(\vec{k}) + \hbar \omega \cdot | \langle \vec{k'} | e^{i \vec{q} \cdot \vec{r}} | \vec{k} \rangle |^2 $$
where $\hbar \omega$ is the energy of the phonon involved in the scattering process. The term which included $t$ is lost while calculating the derivative of the Fermi Golden Rule, it is now represented in the delta function. The scattering, this time, is not elastic because the phonon can be either absorbed or emitted, so $E(\vec{k'}) - E(\vec{k}) = \pm \hbar \omega$. 
##### Relaxation Time Approximation
To simplify the collision term, we can use the relaxation time approximation (RTA). This approximation assumes that the distribution function $f$ relaxes towards the equilibrium distribution function $f_0$, from the state of non-equilibrium $f$, over a characteristic time scale known as the relaxation time $\tau$. The RTA expresses the collision term as:
$$\left( \frac{\partial f}{\partial t} \right)_{collision} = -  \frac{f(\vec{k}) - f_0(\vec{k})}{\tau(\vec{k})} $$
We can now rewrite the semi-classical Boltzmann equation using the RTA:
$$\frac{\partial f}{\partial t} + \vec{v} \cdot \nabla_{\vec{r}} f + \frac{\vec{F}}{\hbar} \cdot \nabla_{\vec{k}} f = -  \frac{f(\vec{k}) - f_0(\vec{k})}{\tau(\vec{k})} $$
We will later see that $\vec{F} = -e \vec{E}$, where $\vec{E}$ is the applied electric field. We expect that by removing the perturbation, the system will return to equilibrium, so $f \rightarrow f_0$ as $t \rightarrow \tau$.
The perturbation will induce our system to be in a non-equilibrium stationary state, meaning that the state does not change with time. We further assume that the system is homogeneous, so there are no spatial variations in the distribution function.





## References
