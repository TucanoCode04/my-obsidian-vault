
2025-10-30 12:10

Status: 

Tags:

# Color Centers
F-centers are defects in a crystal lattice where an anion has left its position, and an electron occupies the vacancy. These centers can absorb and emit light, making them important in various optical applications.
We can perceive the electron as trapped in a potential well created by the surrounding positive ions, this space is approximately of radius $2a$, where $a$ is the lattice constant. The energy levels of the electron in this well determine the wavelengths of light that can be absorbed or emitted.
The Schrödinger equation for an electron in a box of width $2a$ can be solved to find the quantized energy levels(eigenvalues). So the eigenfunctions are discrete, regulated by the boundary conditions of the well, given by $L=2a$:
$$\begin{cases}
x, y,z  > 0,\quad x, y,z < 2a \Rightarrow V(x,y,z) = 0 \\
x, y,z \leq 0,\quad x, y,z \geq 2a \Rightarrow V(x,y,z) = \infty
\end{cases}$$
The energy levels for a particle in a three-dimensional box are given by:
$$E = \frac{h^2 n_x^2}{8m(2a)^2} + \frac{h^2 n_y^2}{8m(2a)^2} + \frac{h^2 n_z^2}{8m(2a)^2} = \frac{h^2}{8m(2a)^2}(n_x^2 + n_y^2 + n_z^2)$$
where $n_x, n_y, n_z$ are quantum numbers corresponding to each dimension, integers $>0$, otherwise the wavefunction would be zero. $h$ is Planck's constant, and $m$ is the mass of the electron.
The lowest energy state (ground state) occurs when $n_x = n_y = n_z = 1$:
$$E_{111} = \frac{h^2}{8m(2a)^2}(1^2 + 1^2 + 1^2) = \frac{3h^2}{32ma^2}$$
The second lowest energy state is degenerate, occurring for the combinations (1,1,2), (1,2,1), and (2,1,1). If we imagine the electron transitioning from the second lowest energy state to the ground state, the energy difference $\Delta E$ is:
$$\Delta E = \hbar \omega = E_{211} - E_{111} = \frac{h^2}{8m(2a)^2}(2^2 + 1^2 + 1^2 - (1^2 + 1^2 + 1^2)) = \frac{3h^2}{32ma^2}$$
This energy difference corresponds to the energy of the photon absorbed or emitted during the transition. $2a$ is related to the lattice constant, which is related to the mass of the atom, so different materials will have different lattice constants and thus different energy levels for their F-centers.  
This energy falls within the visible spectrum for many ionic crystals, because the lattice constants are typically on the order of a few angstroms, leading to energy differences that correspond to visible light wavelengths. 
The crystal, otherwise transparent since the energy gap is larger than the energy of visible light($1.5-3 eV$), becomes colored because the F-centers absorb specific wavelengths of light corresponding to these energy transitions, while other wavelengths are transmitted or reflected, giving rise to the observed color. This defects make it so less energy is required to excite the electron, because the F-center introduces energy levels within the band gap of the crystal and the energy is lower than the band gap energy. 
The photon is not emitted, but the electron relaxes back to the ground state non-radiatively, transferring its energy to the lattice as vibrations(phonons). This process can lead to heating of the material rather than light emission. The F-center stays colored only while the electron is in the excited state; once it relaxes back to the ground state, the material returns to its original transparent state unless other photons are absorbed to re-excite the electron.
Note: fluorescence and luminescence can also occur when the electron relaxes back to the ground state, emitting light at a longer wavelength than the absorbed light due to non-radiative relaxation processes.






## References
