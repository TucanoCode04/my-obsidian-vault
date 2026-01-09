
2025-12-29 17:36

Status: 

Tags:

# Quantum Dots as Qubits
A note on the energy diagrams
![[Pasted image 20251229185454.png]]
##### Quantum Dot Charging
![[Pasted image 20251229174124.png]]
Quantum Dots are easily controllable through electrical gating(external voltages). By adjusting these voltages, we can precisely control the number of electrons in a quantum dot. This is crucial for initializing and manipulating qubit states.
The quantum dots are described as standing wave patterns of electrons confined in all three spatial dimensions. The confinement leads to discrete energy levels, similar to those in atoms, which is why quantum dots are often referred to as "artificial atoms."
There's no electrical wiring between the dots; instead, the coupling is achieved through tunneling effects and capacitive interactions. By adjusting the gate voltages, we can control the tunneling rates and interaction strengths between adjacent quantum dots.

The model is described through two approximations:
- Coulomb interactions among the electrons in the dot, between the one in the dot and the environment, are all described by a constant capacitance.
- The single-particle energy levels are independent of the number of electrons in the dot.

We want to calculate the charge on the dot as a function of the applied voltages.$$Q_{dot} = Q_{dot,0} + C_S(V_S - V_{dot}) + C_D(V_D - V_{dot}) + C_G(V_G - V_{dot})$$ Where:
- $Q_{dot}$ is the total charge on the dot.
- $Q_{dot,0}$ is the intrinsic charge on the dot without any applied voltages.
- $C_S$, $C_D$, and $C_G$ are the capacitances between the dot and the source, drain, and gate, respectively.
- $V_S$, $V_D$, and $V_G$ are the voltages applied to the source, drain, and gate, respectively.
- $V_{dot}$ is the potential of the quantum dot.

We define the total capacitance of the dot as: $$C_{dot} =-( C_S + C_D + C_G)$$We use the negative sign to better express the accumulation of negative charge on the dot when positive voltages are applied to the surrounding electrodes.
By rearranging the equation:
$$Q_{dot} = Q_{dot,0} +(V_{dot}C_{dot} + C_SV_S + C_DV_D + C_GV_G)$$
So now can simply see that there are 2 contributions to the charge on the dot:
1. The intrinsic charge $Q_{dot,0}$, when no voltages are applied.
2. The charge induced by the applied voltages on the surrounding electrodes.

**Note:** Remember that $C=\frac{Q}{V}$

We want to extract the electrostatic potential of the isolated quantum dot, $V_{dot}$:
$$V_{dot}(Q_{dot}) = \frac{Q_{dot} - Q_{dot,0}}{C_{dot}} - \frac{C_S V_S + C_D V_D + C_G V_G}{C_{dot}}$$
The first term represents the potential due to the charge on the dot itself so it-s basically an electron-electron interaction term. The second term represents the influence of the external voltages on the dot's potential.
The potential is function of the total charge on the dot, we use this to calculate the electrostatic energy variation when adding $N_{add}$ electrons to the dot:
$$E_{elstatic}(N_{add}) = \int_{Q_{dot,0}}^{Q_{dot,0} - |e|N_{add}} V_{dot}(Q_{dot}) dQ_{dot} = \frac{e^2N_{add}^2}{2C_{dot}} + \frac{eN_{add}}{C_{dot}}(C_S V_S + C_D V_D + C_G V_G)$$
The integration limits reflect that adding electrons to the dot decreases its total charge (since electrons carry negative charge).
$Q_{dot} = -|e|N$, where N is the total number of electrons in the dot.
$N_{add} = N - N_0$, where $N_0$ is the number of electrons in the dot when no voltages are applied.
Again the first term represents the electron-electron interaction energy, while the second term captures the effect of the external voltages on the energy of the dot.
The electrostatic energy is summed to the single-particle energy levels of the electrons in the dot to get the total energy of the system:
$$E (N) = E_{elstatic}(N) + \sum_{i=1}^{N} \epsilon_i^{(0)}$$
Where $\epsilon_i^{(0)}$ are the single-particle energy levels of the electrons in the dot, basically obtained from solving the Schrödinger equation for the confined electrons (particle in a box). The $^{(0)}$ indicates that these levels are calculated without considering electron-electron interactions. We write $N$ instead of $N_{add}$ because we assume that we start from an empty dot ($N_0 = 0$).

The electrochemical potential tells us the energy required to add one more electron to the dot:
$$\mu(N) = \frac{\partial E(N)}{\partial N} = E(N) - E(N-1) = \frac{e^2 N -\frac{1}{2}}{C_{dot}} + \frac{e}{C_{dot}}(C_S V_S + C_D V_D + C_G V_G) + \epsilon_N^{(0)}$$
To manipulate the number of electrons in the dot, we adjust the gate voltage $V_G$, because if we were to change the source or drain voltages, we would create a current flow through the dot, which is not desired when we want to control the electron number precisely. The effect of the gate voltage is to shift the electrochemical potential of the dot up or down.
![[Pasted image 20260107155947.png]]
##### Coulomb Blockade 
![[Pasted image 20260107160338.png]]
Basically, Coulomb Blockade is a phenomenon observed in quantum dots and other nanoscale systems where the addition of a single electron to the system is energetically unfavorable due to strong electron-electron interactions. This leads to a suppression of electrical conductance at low temperatures and small bias voltages.
When an electron tries to enter the quantum dot, it experiences a repulsive force from the electrons already present in the dot. This repulsion creates an energy barrier that must be overcome for the electron to successfully tunnel into the dot. If the energy provided by the external voltage (bias voltage) is less than this barrier, the electron cannot enter the dot, resulting in a blockade of current flow.
So it's not enough for $\mu_{source}$ to be greater than $\mu(N)$ to have an electron tunnel into the dot, we also need to make sure that $\mu_{drain}$ is less than $\mu(N)$ to allow the electron to leave the dot. If either of these conditions is not met, the electron will be "stuck" in the dot, leading to Coulomb Blockade. To unblock the flow of electrons, we need to adjust the gate voltage $V_G$ such that the electrochemical potential of the dot $\mu(N)$ lies between the source and drain potentials.
##### Low and High Bias Regimes
![[Pasted image 20260107160624.png]]
Int he low bias regime, at most one level of the quantum dot lies within the bias window defined by the source and drain potentials. Whereas in the high bias regime, multiple levels can lie within this window.

**Low Bias Regime**
In the low bias regime, the bias voltage $V_{SD}$ applied between the source and drain is small enough that only one energy level of the quantum dot falls within the bias window. This means that only one electron can tunnel through the dot at a time, leading to discrete conductance peaks as the gate voltage is varied. Each peak corresponds to the alignment of the electrochemical potential of the dot with the source and drain potentials, allowing an electron to tunnel through.
Basically, when $\mu_{N}$ is within the bias window, an electron can tunnel from the source to the dot, obviously tunneling is a probabilistic process, so there's a certain rate at which electrons tunnel in and out of the dot. So the number of electrons in the dot fluctuates between N-1 and N.
![[Pasted image 20260107161344.png]]
The current can also flow if we operate on $V_{SD}$
![[Pasted image 20260107161424.png]]
![[Pasted image 20260107161452.png]]
This two graphs show basically the bias windows as a function of $V_G$ and $V_{SD}$. The diamond-shaped regions correspond to Coulomb Blockade, where no current flows through the dot. 
The example from before is represented by the horizontal line cut at low bias voltage $V_{SD}$. 
![[Pasted image 20260107161709.png]]
![[Pasted image 20260107161828.png]]
In the latter example we identify 3 different situations, in which all of them allow current flow.

**High Bias Regime**
The energy levels seen so far were all ground states (GS). However, quantum dots also have excited states (ES) that can participate in transport when the bias voltage is sufficiently high. They can arise from various sources, for example if a magnetic field is applied, the spin degeneracy of the energy levels is lifted, leading to spin-split excited states, Zeeman splitting.
![[Pasted image 20260107162933.png]]
From the image we can analyze three different transitions showed by the chemical potentials:
1. $ES(N) \rightarrow GS(N+1)$: One more electron is added to the dot, occupying the ground state of the N+1 electron system.
2. $GS(N) \rightarrow GS(N+1)$: One more electron is added to the dot, occupying the ground state of the N+1 electron system.
3. $GS(N) \rightarrow ES(N+1)$: One more electron is added to the dot, occupying the excited state of the N+1 electron system.

(Remember this are transitions of the system, not of the single particle levels)
We can describe again the bias windows as a function of $V_G$ and $V_{SD}$, but now including the excited states.
![[Pasted image 20260107163755.png]]
![[Pasted image 20260107163806.png]]
![[Pasted image 20260107163816.png]]
![[Pasted image 20260107163824.png]]
In the dotted lines there would be enough energy to allow tunneling, but it is not enough to overcome the Coulomb Blockade.

#### Spin in Single Quantum Dots
By applying a magnetic field, we can lift the spin degeneracy of the energy levels in the quantum dot through the Zeeman effect. This results in two distinct energy levels for each orbital state: one for spin-up electrons and another for spin-down electrons. 
![[Pasted image 20260107164539.png]]

In the case in which the quantum dot is occupied by a single electron, the lowest orbital can be occupied in two ways: 
1. The electron can occupy the spin-up state ($\uparrow$), or ground state. $E_{tot} = E_{\uparrow, 0}$
2. The electron can occupy the spin-down state ($\downarrow$), or excited state. $E_{tot} = E_{\downarrow, 0} = E_{\uparrow, 0} + \Delta E_Z$
![[Pasted image 20260107164915.png]]

In the high bias regime the single dot qubit can be charged with one electron through two different transitions:
1. $0 \rightarrow \uparrow$: The dot is initially empty, and an electron tunnels into the dot occupying the spin-up ground state.
2. $0 \rightarrow \downarrow$: The dot is initially empty, and an electron tunnels into the dot occupying the spin-down excited state.
![[Pasted image 20260107165134.png]]
As seen from the image, there are two important things to consider:
- If I lower the bias window enough, I can reach a point where only the ground state transition $0 \rightarrow \uparrow$ is allowed. This is useful for initializing the qubit in a known spin state. Imagine cutting the graph with an horizontal line at low bias voltage.
- Over a certain gate voltage, even though the transition $0 \rightarrow \downarrow$ is energetically allowed, there no current flow because the electron in the excited state can relax to the ground state before it has a chance to tunnel out of the dot. This phenomenon is known as spin blockade and is crucial for spin qubit readout(double check this).

If we add a second electron to the dot, there are many different possible configurations:
1. Both electrons occupy the spin-up and spin-down states of the lowest orbital, forming a singlet state (S). $E_{tot} = E_{\uparrow, 0} + E_{\downarrow, 0} + E_C$ (where $E_C$ is the energy due to electron-electron repulsion). $|S\rangle = \frac{1}{\sqrt{2}}(|\uparrow\downarrow\rangle - |\downarrow\uparrow\rangle)$ 
![[Pasted image 20260107170235.png]]
2. One electron occupies the lowest orbital, while the other occupies the first excited orbital. When they have different spins, they form the triple state ($T_0$). $E_{tot} = E_{\uparrow, 0} + E_{\downarrow, 1} + E_C = E_{\uparrow, 1} + E_{\downarrow, 0} + E_C$. $|T_0\rangle = \frac{1}{\sqrt{2}}(|\uparrow\downarrow\rangle + |\downarrow\uparrow\rangle)$ 
![[Pasted image 20260107170455.png]]
3. Both electrons occupy the $\uparrow$ states of the lowest and first excited orbitals, forming the triple state ($T_+$). $E_{tot} = E_{\uparrow, 0} + E_{\uparrow, 1} + E_C$. $|T_+\rangle = |\uparrow\uparrow\rangle$ 
![[Pasted image 20260107170555.png]]
4. Both electrons occupy the $\downarrow$ states of the lowest and first excited orbitals, forming the triple state ($T_-$). $E_{tot} = E_{\downarrow, 0} + E_{\downarrow, 1} + E_C$. $|T_-\rangle = |\downarrow\downarrow\rangle$
![[Pasted image 20260107170606.png]]

This is the charging of the quantum dot with two electrons, showing the different possible spin and orbital configurations.
![[Pasted image 20260107170633.png]]

#### Digression on Bloch Sphere

#### Single Spin Qubit
The single spin qubit is the simplest implementation of a quantum bit using the spin degree of freedom of an electron confined in a quantum dot. A quantum dot is connected to a gate and a reservoir of electrons, a large static magnetic field is applied to lift the spin degeneracy through the Zeeman effect.
The qubit is functioning when there are either 0 or 1 electron in the dot.
![[Pasted image 20260107184246.png]]

The operation of the single spin qubit involves several key steps:

1.**Initialization**: After the quantum dot is emptied, the gate voltage is adjusted so that only the ground state transition $0 \rightarrow \uparrow$ is energetically allowed. An electron tunnels into the dot occupying the spin-up ground state, thus initializing the qubit in a known state $|\uparrow\rangle$.
![[Pasted image 20260107184719.png]]

The Quantum Dot is the optimal system for a qubit, since we have:
- a two-level system (spin up and spin down)
- a confined environment (the dot), with no perturbations from external atoms
- easy initialization (by controlling the gate voltage)
- whose state can be measured electrically, basically whenever there's tunneling we can measure the current with an electrometer.

A qubit is generally represented with the Bloch Sphere, with a general state $|\psi\rangle = cos \frac{\theta}{2} |0\rangle + e^{i\phi} sin \frac{\theta}{2} |1\rangle$, where $|0\rangle = |\uparrow\rangle$ and $|1\rangle = |\downarrow\rangle$.
![[Pasted image 20260107185629.png]]

There are then 2 main types of operations that can be performed on the single spin qubit:
1. Horizontal Rotation ($\phi$ rotation): Induced by applying an oscillating magnetic field (microwave frequency) perpendicular to the static magnetic field. This causes the spin to precess around the axis defined by the oscillating field, allowing for precise control of the qubit state. It keeps the same relative probability between the two states but changes the phase of the wavefunction. It's achieved through Larmor precession.
![[Pasted image 20260107185914.png]]
2. Vertical Rotation ($\theta$ rotation): Achieved by applying resonant magnetic field pulses that cause transitions between the spin-up and spin-down states. This changes the relative probabilities of measuring the qubit in either state. It's achieved through Rabi oscillations.
![[Pasted image 20260107190127.png]]

##### Physics of a Spin Particle in a Uniform Magnetic Field
![[Pasted image 20260109105528.png]]
When a static magnetic field is applied, for example along the z-axis, the particles with spin (like electrons) experience a torque that causes their magnetic moments to precess around the direction of the magnetic field. This phenomenon is known as Larmor precession.
It basically happens because the magnetic moment $\vec{\mu}$ of the particle interacts with the external magnetic field $\vec{B}$, leading to a torque $\vec{\tau}$ given by:
$$\vec{\tau} = \vec{\mu}_S \times \vec{B}$$
This torque causes the magnetic moment to precess around the direction of the magnetic field at a frequency called the Larmor frequency. There's not enough energy to flip the spin, so it just precesses, cause the particle's spin is trying to align with the magnetic field.

An energy is associated with this interaction, given by the Hamiltonian:
$$\hat{H} = -\hat{\mu}_S \cdot \vec{B}$$Where $\hat{\mu}_S$ is the magnetic moment operator of the spin. For an electron, the magnetic moment is related to its spin operator $\hat{S}$ by:
$$\hat{\mu}_S = -\frac{e}{m} \hat{S}$$So, if we substitute this into the Hamiltonian and we consider a magnetic field applied along the z-axis ($\vec{B} = B_Z \hat{z}$), we get:
$$\hat{H} = \frac{e}{m} \hat{S}_Z B_Z$$
Where $\hat{S}_Z$ is the z-component of the spin operator:
$$\hat{S}_Z = \frac{\hbar}{2} \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$
![[Pasted image 20260109110606.png]]
In the graph we see the precession angle $\theta$ as a function of the applied magnetic field $B_Z$. 

The eigenstates of $\hat{H}$ are just the ones of of $\hat{S}_Z$, which are the spin-up $|\uparrow\rangle$ and spin-down $|\downarrow\rangle$ states, so the general solution would be:
$$|\psi(t = 0)\rangle = a |0\rangle + b |1\rangle$$ 
Where $|0\rangle = |\uparrow\rangle$ and $|1\rangle = |\downarrow\rangle$. But, because of the presence of the magnetic field, their energy will no longer be degenerate:
$$E_{\uparrow} = \frac{e \hbar}{2m} B_Z$$
$$E_{\downarrow} = -\frac{e \hbar}{2m} B_Z$$
![[Pasted image 20260109111050.png]]
In the graph $B_Z$ is along the z-axis but is negative, so the spin-up state has lower energy, since the magnetic moment of the electron is opposite to its spin (meaning that when the spin is up, the magnetic moment is down and viceversa). And if the magnetic moment is aligned with the magnetic field, the energy is minimized. 

##### Digression on Time Evolution of Stationary States

##### Larmor Precession
The time evolution of stationary states is given by:
$$|\psi(t)\rangle = e^{-i \frac{\hat{H}}{\hbar} t} |\psi(0)\rangle$$
So if we insert it in our general solution found before:
$$|\psi(t)\rangle = a e^{-i \frac{E_{\uparrow}}{\hbar} t} |\uparrow\rangle + b e^{-i \frac{E_{\downarrow}}{\hbar} t} |\downarrow\rangle = a e^{-i \frac{e B_Z}{2m} t} |\uparrow\rangle + b e^{i \frac{e B_Z}{2m} t} |\downarrow\rangle$$
We can factor out a global phase $e^{-i \frac{E_{\uparrow}}{\hbar} t}$, which doesn't affect the physical properties of the state:
$$|\psi(t)\rangle = e^{-i \frac{eB_Z}{2m} t} \left( a |\uparrow\rangle + b e^{i \frac{e B_Z}{m} t} |\downarrow\rangle \right) = a|\uparrow\rangle + b e^{i \frac{ e B_Z}{m} t} |\downarrow\rangle$$
The relative phase between the two spin states evolves over time, leading to a precession of the spin state around the z-axis.
IF we see it on the Bloch Sphere:
$$|\psi(t)\rangle = cos \frac{\theta}{2} |0\rangle + e^{i(\frac{e B_Z}{m} t)} sin \frac{\theta}{2} |1\rangle$$
Larmor precession leads to an horizontal rotation around the z-axis of the Bloch Sphere, so we a constant magnetic field is applied along the z-axis, the state will naturally move around the equator of the Bloch Sphere.
![[Pasted image 20260109113503.png]]
To complete the full cycle:
$$\frac{e B_Z}{m} t = 2 \pi$$
Which gives us the Larmor Frequency:
$$\omega_0 = \frac{2 \pi}{T} = \frac{e B_Z}{m}$$
The Larmor rotation direction depends on the sign of the magnetic field applied and the precession speed is proportional to the magnetic field strength.

##### Spin Resonance 


## References
