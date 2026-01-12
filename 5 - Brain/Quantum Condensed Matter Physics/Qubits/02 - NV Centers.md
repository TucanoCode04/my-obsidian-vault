
2026-01-12 12:11

Status: 

Tags:

# 02 - NV Centers
Nv Centers are creating by implanting $N^+$ ions into a diamond lattice, followed by annealing to form the vacancy. The negatively charged NV center (NV-) consists of a substitutional nitrogen atom adjacent to a lattice vacancy, capturing an extra electron.
This defect has a charge and spin disparity, having less charge near the vacancy and more near the nitrogen atom, creating a perfect dipole, which can be used as a two state quantum system.
![[Pasted image 20260112132311.png]]
We normally use a mask of 60nm thick resist, to get a shallow implantation, resulting in a low number of NV centers per implantation site. 
![[Pasted image 20260112132424.png]]

Advantages of NV Centers:
![[Pasted image 20260112132453.png]]
##### NV Centers Ground State
The nitrogen atom and the 3 carbon atoms surrounding the vacancy contribute 5 electrons, then an extra electron is captured to form the NV- state, giving a total of 6 electrons.
From the hybridization of the atomic orbitals, we get 4 molecular orbitals: 2 $a_1$ orbitals and 2 degenerate $e_x$ and $e_y$ orbitals.
The 2 $a_1$ orbitals are lower in energy, and fully occupied with 4 electrons, while the $e_x$ and $e_y$ orbitals are higher in energy and occupied by 2 electrons, this 2 states form a triplet state, depending on their alignment.
![[Pasted image 20260112133343.png]]
The ground state is a spin triplet state, with a zero field splitting of $D=2.87GHz$ between the $m_s=0$ and $m_s=\pm1$ states, due to spin-spin interactions. This configuration is different from the singlet-triplet qubit in quantum dots, where the singlet state is lower in energy than the triplet state.
The $m_s=0$ state is not the singlet state, but it comes out of the sum of 2 spins.
The applied magnetic field is zero, but we have a local magnetic field due to the structure of the crystal, which causes hyperfine splitting of the $m_s=\pm1$ states. 
![[Pasted image 20260112133814.png]]
##### NV Centers Excited State 
When we excite the NV center with a green laser (532nm), an electron is promoted from the $a_1$ orbital to the $e$ orbital, creating an excited triplet state.
![[Pasted image 20260112134106.png]]
It is really important to note that the optical transitions between the ground and excited states are spin-conserving, meaning that an electron in the $m_s=0$ ground state will only transition to the $m_s=0$ excited state, and similarly for the $m_s=\pm1$ states. This property is crucial for spin initialization and readout.
The excitation is non-resonant, meaning that the laser energy is higher than the energy difference between the ground and excited states, so it takes advantage of vibronic transitions to complete the excitation.
##### Relaxation (Radiative Path)
The relaxation path is spin dependent. From the $m_s=0$ excited state, the electron can relax directly back to the $m_s=0$ ground state by emitting a photon in the red region (637nm).
Radiative emission can be optically detected, allowing for optical readout of the spin state. One practical reason for using green excitation is to avoid overlap between the excitation and emission wavelengths, facilitating easier detection of the emitted photons.
![[Pasted image 20260112135519.png]]
##### Vibronic Transitions
The simultaneous excitation of electronic and vibrational states leads to vibronic transitions, which broaden (separate) the absorption and emission spectra. 
This occurs because electronic transitions are faster than nuclear motions (Franck-Condon principle). During absorption, the nuclei are in their ground vibrational state, but upon excitation, the equilibrium positions of the nuclei change, leading to transitions to higher vibrational states in the excited electronic state. Instead, during emission, the nuclei relax to lower vibrational states in the ground electronic state.
Basically, the absorption spectrum is shifted to higher energies (shorter wavelengths) compared to the emission spectrum. The Fermi Golden Rule gives the probability of these transitions, which depend on the overlap between the vibrational wavefunctions of the initial and final states. As we can see from the graph below, the 0-0 transition (no change in vibrational state) is minimal since it shifts to higher vibrational levels.
![[Pasted image 20260112140536.png]]
![[Pasted image 20260112140530.png]]
The first graph shows that inside the energy levels we have vibrational levels, and a shift $q_0$ between the equilibrium positions of the ground and excited states, leading to vibronic transitions.
So the absorption (blue) is shifted to higher vibrational levels in the excited state, while the emission (green) occurs from the excited state to lower vibrational levels in the ground state.
In the second graph we see the absorption and emission spectra of the NV center, with a minimal overlap in the 0-0 transition.
##### Relaxation (Non-Radiative Path)
The relaxation is again spin dependent. From the $m_s=\pm1$ excited state, is more likely that recombination occurs instead of photon emission. This non-radiative recombination occurs through 2 intermediate singlet states.
The final state of this non-radiative path is the $m_s=0$ ground state, meaning that the non-radiative relaxation is spin flipping.
![[Pasted image 20260112141120.png]]
##### State Measurement
If we excite the NV center with a green laser, if the electron is in the $m_s=0$ state, it will emit red photons through the radiative path, while if it is in the $m_s=\pm1$ states, it will likely relax through the non-radiative path, emitting fewer photons.
![[Pasted image 20260112141139.png]]
##### State Initialization
We can ensure that the electron is in the $m_s=0$ state by continuously exciting it with a green laser. If it starts in the $m_s=\pm1$ states, it will relax through the non-radiative path to the $m_s=0$ ground state. Once in the $m_s=0$ state, it will keep cycling between the ground and excited states through the radiative path, effectively initializing the spin state to $m_s=0$.
![[Pasted image 20260112141306.png]]
##### Zeeman Splitting on NV Centers 
By applying an external magnetic field along the NV axis, we can lift the degeneracy of the $m_s=\pm1$ states through the Zeeman effect. 
$|m_s=+1\rangle$ is antialigned with the magnetic field, so its energy increases, while $|m_s=-1\rangle$ is aligned with the magnetic field, so its energy decreases.
Since $m_s=0$ doesn't have a projection along the magnetic field, its energy remains unchanged.
So now we can define a 2 level system using the $m_s=0$ as $|0\rangle$ and $m_s=-1$ as $|1\rangle$, which can be manipulated by shining green light and waiting for the relaxation to initialize.
![[Pasted image 20260112141743.png]]

The difference with the previous types of qubit are that now the measurement is optical, and no more electrical.

##### Operations on NV Centers
We want again to be able to perform single qubit operations.
**Horizontal Motion:**
![[Pasted image 20260112141934.png]]
**Vertical Motion:**
![[Pasted image 20260112142005.png]]
Now the difference is that the vertical manipulation can only be done with optical means. Microwaves have a magnetic component.

##### Spin Resonance
As for the single spin qubit, the manipulation of the NV center qubit is done by applying both a DC magnetic field and an AC magnetic field (microwaves).
The DC field is applied along the NV axis to create the Zeeman splitting, while the AC field is applied perpendicular to the DC field to induce transitions between the $|0\rangle$ and $|1\rangle$ states. 
When the frequency of the AC field matches the energy difference between the two states $\Delta E = \hbar \omega_T$, we achieve resonance, allowing for efficient manipulation of the qubit state.
![[Pasted image 20260112143344.png]]
The main difference with the single spin qubit is that in the single spin qubit we had a doublet, while here we have a triplet, so our two level system will be represented by>
![[Pasted image 20260112143523.png]]
The difference in the $|0\rangle$ is that in the single spin qubit it correspond to a net spin of 1/2, while here it correspond to a total spin of 0.

##### Operations
**$\frac{\pi}{2}$ Pulse:**
If a magnetic field is applied for $\omega_1 t=\frac{\pi}{2}$, the state will evolve:
$$|\psi\rangle = |0\rangle \rightarrow \frac{1}{\sqrt{2}}(|0\rangle +|1\rangle)$$
![[Pasted image 20260112144259.png]]
**$\pi$ Pulse:**
If a magnetic field is applied for $\omega_1 t=\pi$, the state will evolve:
$$|\psi\rangle = |0\rangle \rightarrow |1\rangle$$
![[Pasted image 20260112144316.png]]
Corresponding to a NOT gate.

So by applying microwaves at the resonance frequency, we can perform arbitrary single qubit rotations on the NV center qubit. Unlike the spin qubit, the Rabi oscillations here are constant, so we don't lose information over time. For a full rotation on the Bloch Sphere we need 7 ns which is several times smaller than the coherence time of 1.8 ms.
![[Pasted image 20260112144609.png]]

The only problem is that it is exposed to surrounding magnetic fields induced by magnetic elements in the diamond lattice with non-zero nuclear spins, which can cause decoherence.
![[Pasted image 20260112144743.png]]

#### Quantum Sensing
Quantum sensing refers to the use of quantum systems, such as NV centers in diamond, to measure physical quantities with high sensitivity and precision. 
##### DC Magnetic Field
![[Pasted image 20260112161531.png]]
The NV center can be used to sense DC magnetic fields by measuring the Zeeman splitting of the $m_s=\pm1$ states. By applying a known microwave frequency with laser excitation, we can determine the magnetic field strength based on the resonance condition.
Basically, starting from $|m_S=0\rangle$, we apply microwaves at a specific frequency and measure the fluorescence intensity. When the microwave frequency matches the energy difference between $|m_S=0\rangle$ and $|m_S=-1\rangle$, we observe a dip in fluorescence due to increased population in the $|m_S=-1\rangle$ state, which relaxes non-radiatively. We do the same for $|m_S=+1\rangle$. By measuring the frequencies at which these dips occur, we can calculate the magnetic field strength using the Zeeman splitting formula.
##### AC Magnetic Field

















## References
