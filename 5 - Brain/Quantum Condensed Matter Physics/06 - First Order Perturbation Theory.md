
2025-10-22 12:43

Status: 

Tags:

# First Order Perturbation Theory
From previous lectures: $\vec{k}$ is quantum number used to label the momentum of a particle in a periodic potential. 
##### Parabolic Band Approximation
The Parabolic Band Approximation assumes that near the band edges (conduction band minimum and (conduction band maximum), the energy-momentum relationship can be approximated as parabolic. This is useful for simplifying calculations of electronic properties in semiconductors. This can be done because electrons behave like free particles with an effective mass that differs from the free electron mass due to the periodic potential of the crystal lattice.
The effective mass is not a scalar quantity, but rather a tensor, because the response of an electron to an applied force can vary depending on the direction of the force relative to the crystal lattice. In anisotropic materials, the effective mass can differ along different crystallographic directions, leading to a tensor representation. 
For example, if we take and asymptote of the band structure near the valence band maximum, putting the energy at the maximum to be zero, an other asymptote near the conduction band minimum, putting the energy at the minimum to be $E_g$, we can write the energy in the conduction and valence bands as:
$$\begin{cases}
E_C = E_g + \frac{\hbar^2 k^2}{2 m_e^*} \\
E_V = - \frac{\hbar^2 k^2}{2 m_h^*}
\end{cases}$$
where $m_e^*$ and $m_h^*$ are the effective masses of electrons and holes, respectively.

In semiconductors, we have 3 band in the valence band: heavy hole band, light hole band and split-off band. The heavy hole and light hole bands are degenerate at the $\Gamma$ point (k=0), while the split-off band is separated by a small energy gap due to spin-orbit coupling. The effective masses of holes in these bands differ, with heavy holes having a larger effective mass compared to light holes.
#### Absorption of a Photon by a Semiconductor 
When a photon is absorbed by a semiconductor, it can excite an electron from the valence band to the conduction band, creating an electron-hole pair. The energy of the photon must be at least equal to the bandgap energy ($E_g$) of the semiconductor for this transition to occur, if this was not a solid-state material, the energy should have been equal to the difference in energy levels for the transition to occur, because in a solid-state material we have bands of energy levels rather than discrete energy levels.
We consider a flux of photons $I$ with energy $E = h \nu = \hbar \omega$ incident on the semiconductor. We position our coordinate system such that the z-axis starts at the surface of the semiconductor and goes into the material. The photons are absorbed as they penetrate the material, leading to an exponential decrease in intensity with depth $z$:
$$I(z) = I_0 e^{-\alpha z}$$ where $I_0$ is the incident intensity at the surface ($z=0$) and $\alpha$ is the absorption coefficient of of the material, which depends on the material properties and the photon energy. For larger $\alpha$, the material is more absorptive, so the intensity decreases more rapidly with depth. it varies depending on the band structure and the frequency of the incident light. At low frequencies (below the bandgap), $\alpha = 0$ because photons do not have enough energy to excite electrons across the bandgap, so there is no absorption. As the frequency increases and exceeds the bandgap energy, $\alpha$ increases, indicating that photons can now be absorbed to create electron-hole pairs.
We want to study how this external perturbation (the incident photons) perturbs the ground state of the semiconductor. We can use first-order perturbation theory to calculate the transition rates from the ground state to excited states due to the interaction with the electromagnetic field of the photons.
##### First-Order Perturbation Theory
We focus on an unperturbed system with quantized energy levels described by the Hamiltonian $H_0$. The Hamiltonian describes how electrons behave in the periodic potential of the crystal lattice. 
We want to study how this system responds to an external perturbation, such as a photon flux incident on the semiconductor. The system can be described as:
$$\hat{H_0} \Phi_n (\vec{r},t) = E_n \Phi_n (\vec{r},t)$$
where $\Phi_n (\vec{r},t)$ are the eigenfunctions of the unperturbed Hamiltonian and $E_n$ are the corresponding energy eigenvalues. Here $\hat{H_0}$ is time independent, because the energy levels do not change with time. The time dependence of the wave functions can be easily factorized as:
$$\Phi_n (\vec{r},t) = \psi_n (\vec{r}) e^{-i E_n t / \hbar}$$
where $\psi_n (\vec{r})$ are the spatial part of the wave functions. They are called stationary states because their probability density does not change with time and the energy is well defined. They are eigenfunctions of the time-independent Hamiltonian $\hat{H_0}$, normalized and orthogonal to each other, $\braket{\psi_i | \psi_j} = \delta_{ij}$.
The probability is also time-independent because:
$$|\Phi_n (\vec{r},t)|^2 = |\psi_n (\vec{r})|^2$$
So time can be considered as a phase factor that does not affect the probability density. 
The electromagnetic wave perturbs the system, so we introduce a time-dependent perturbation cause it heats the solid and makes the atoms vibrate. The total Hamiltonian becomes:
$$\hat{H} = \hat{H_0} + \hat{V}(t)$$
where $\hat{V}(t)$ is the time-dependent perturbation, it is still $\vec{r}$ dependent, but we drop it for simplicity.
The formula that we are about to derive is generalized for all types of perturbations, but we will later apply it to the case of photon absorption in semiconductors.
We want to solve the time-dependent Schrödinger equation:
$$\hat{H} \Psi (\vec{r},t) = i \hbar \frac{\partial}{\partial t} \Psi (\vec{r},t)$$where $\Psi (\vec{r},t)$ is the wave function of the perturbed system at time $t > 0$. 
We can express $\Psi (\vec{r},t)$ as a linear combination of the unperturbed eigenfunctions:
$$\Psi (\vec{r},t) = \sum_j c_j(t) \Phi_j (\vec{r},t) $$where $c_j(t)$ are time-dependent coefficients that represent the contribution of each unperturbed state to the perturbed wave function. The probability of finding the system in state $j$ at time $t$ is given by $|c_j(t)|^2$.
Substituting this expansion into the time-dependent Schrödinger equation, we get:
$$\left( \hat{H_0} + \hat{V}(t) \right) \sum_j c_j(t) \Phi_j (\vec{r},t) = i \hbar \frac{\partial}{\partial t} \sum_j c_j(t) \Phi_j (\vec{r},t) $$
$\hat{V}(t)$ commutes cause it doesn't contain derivatives with respect to $\vec{r}$, so we can write: 
$$\sum_j c_j(t) E_j \Phi_j (\vec{r},t) + \sum_j c_j(t) \hat{V}(t) \Phi_j (\vec{r},t) = i \hbar \sum_j  \frac{\partial c_j (t)}{\partial t} \Phi_j (\vec{r},t) + \sum_j c_j(t)E_j \Phi_j (\vec{r},t) $$


## References
