
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
In f


## References
