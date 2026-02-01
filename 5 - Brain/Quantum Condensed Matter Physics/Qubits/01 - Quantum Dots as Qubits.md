
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
To achieve vertical rotations on the Bloch Sphere, we need to induce transitions between the spin-up and spin-down states. This can be accomplished by applying an oscillating magnetic field perpendicular to the static magnetic field (DC):
$$\vec{B}_{AC} = B_1 cos(\omega_0 t) \hat{x}$$
Where $B_1$ is the amplitude of the oscillating field and $\omega_0$ is its angular frequency, which must match the Larmor frequency, which is the energy difference between the two spin energy levels, to achieve resonance.
The magnetic field will then become:
$$\vec{B} = = B_Z \hat{z} + B_1 cos(\omega_0 t) \hat{x}$$
The Hamiltonian describing the interaction of the spin with this combined magnetic field is given by:
$$\hat{H} = \frac{e}{m} \hat{S}_Z B_Z + \frac{e}{m} \hat{S}_X B_1 cos(\omega_0 t)$$
Where $\hat{S}_X$ is the x-component of the spin operator:
$$\hat{S}_X = \frac{\hbar}{2} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$$
By summing the two terms, we get:
$$\hat{H} = \frac{e \hbar}{2m} \begin{pmatrix} B_Z & B_1 cos(\omega_0 t) \\ B_1 cos(\omega_0 t) & -B_Z \end{pmatrix}$$
By remembering that the solution of the time-dependent Schrödinger equation is given by:
$$ \hat{H} |\psi(t)\rangle =i \hbar \frac{\partial}{\partial t} |\psi(t)\rangle   \quad \Rightarrow \quad |\psi(t)\rangle = a |0\rangle + b |1\rangle = \sqrt{2} \begin{pmatrix} a(t) \\ b(t) \end{pmatrix}$$
We can insert the Hamiltonian in the equation:
$$\frac{ e \hbar}{2m} \begin{pmatrix} B_Z & B_1 cos(\omega_0 t) \\ B_1 cos(\omega_0 t) & -B_Z \end{pmatrix} \begin{pmatrix} a(t) \\ b(t) \end{pmatrix} = i \hbar \frac{\partial}{\partial t} \begin{pmatrix} a(t) \\ b(t) \end{pmatrix}$$
This gives us a system of coupled differential equations for the coefficients a(t) and b(t):
$$\frac{e B_Z}{2m} a(t) + \frac{e B_1}{2m} cos(\omega_0 t) b(t) = i \frac{\partial a(t)}{\partial t}$$
$$\frac{e B_1}{2m} cos(\omega_0 t) a(t) - \frac{e B_Z}{2m} b(t) = i \frac{\partial b(t)}{\partial t}$$
We can identify that the terms $\frac{e B_Z}{2m}$ represent the energy difference between the two spin states, and we labelled it as $\omega_0$ being the Larmor frequency. The terms $\frac{e B_1}{2m}$ represent the coupling strength between the spin states induced by the oscillating magnetic field, and we labelled it as $\omega_1$ being the Rabi frequency.
$$\omega_0 a(t) + \omega_1 cos(\omega_0 t) b(t) = i \frac{\partial a(t)}{\partial t}$$
$$\omega_1 cos(\omega_0 t) a(t) - \omega_0 b(t) = i \frac{\partial b(t)}{\partial t}$$
By solving the system of equations, we get:
$$\begin{pmatrix} a(t) \\ b(t) \end{pmatrix} = \begin{pmatrix} e^{-i \frac{\omega_0}{2} t} cos(\frac{\omega_1}{2} t) \\ -i e^{i \frac{\omega_0}{2} t} sin(\frac{\omega_1}{2} t) \end{pmatrix}$$
On the Bloch Sphere representation, this solution describes a rotation of the spin state around an axis in the x-y plane at a frequency determined by the Rabi frequency $\omega_1$.
$$|\psi(t)\rangle = cos(\frac{\omega_1}{2} t) |0\rangle - i e^{i \omega_0 t} sin(\frac{\omega_1}{2} t) |1\rangle$$
As before we look only at the phase difference. The term $-i$ represents a phase shift of $\frac{\pi}{2}$, which corresponds to a rotation around the y-axis of the Bloch Sphere. This is because $1 = e^{2\pi i } \Rightarrow -i = e^{-\frac{\pi}{2} i}$, so:
$$|\psi(t)\rangle = cos(\frac{\omega_1}{2} t) |0\rangle + e^{i (\omega_0 t - \frac{\pi}{2})} sin(\frac{\omega_1}{2} t) |1\rangle$$
![[Pasted image 20260109120504.png]]
![[Pasted image 20260109122329.png]]

By taking the modulus squared of the coefficients, we can find the probabilities of measuring the spin in either state at time t:
$$P_{\uparrow}(t) = |a(t)|^2 = cos^2(\frac{\omega_1}{2} t)$$
$$P_{\downarrow}(t) = |b(t)|^2 = sin^2(\frac{\omega_1}{2} t)$$
These probabilities oscillate over time, demonstrating Rabi oscillations between the spin-up and spin-down states induced by the resonant oscillating magnetic field, the frequency of these oscillations is determined by the Rabi frequency $\omega_1 =  \frac{e B_1}{2m}$.
![[Pasted image 20260109120735.png]]

So now we succeeded in describing both types of rotations on the Bloch Sphere:
1. Larmor Precession (horizontal rotation around z-axis) induced by a static magnetic field along z.
2. Rabi Oscillations (vertical rotation around y-axis) induced by a resonant oscillating magnetic field along x.

##### Single Spin Qubit Manipulation
We start from our two-level system, with the spin-up and spin-down states split by the Zeeman energy due to the static magnetic field $B_Z$. We change $V_G$ so that there's no possibility for the electron to escape the dot regardless of its spin state.
Then we apply a resonant oscillating magnetic field $B_{AC}$ perpendicular to $B_Z$, and we wait exactly the time needed to achieve the desired rotation on the Bloch Sphere.
![[Pasted image 20260109122240.png]]

![[Pasted image 20260109122843.png]]
As we can see from this experimental data, as time goes on the information about the initial spin state is lost due to interactions with the environment, leading to decoherence. The oscillations in the probability of measuring the spin-up state decay over time, indicating that the qubit is losing its coherence and eventually reaches a mixed state where both spin states are equally probable.

##### Single Spin Qubit Readout
To read out the state of the single spin qubit, we adjust the gate voltage $V_G$ such that only the transition corresponding to the spin-down state ($0 \rightarrow \downarrow$) is energetically allowed within the bias window. If the electron is in the spin-up state, it cannot tunnel out of the dot, and we don't measure any current.
![[Pasted image 20260109123143.png]]

If the electron is in the spin-down state, it can tunnel out of the dot and another electron from the reservoir can tunnel into the dot occupying the spin-up ground state. This results in a measurable current flow, indicating that the qubit was in the spin-down state.
![[Pasted image 20260109123217.png]]

##### Pros and Cons of Single Spin Qubits
![[Pasted image 20260109123405.png]]

#### Double Quantum Dot Qubit
![[Pasted image 20260110142745.png]]
Individual quantum dots can be coupled together to form double quantum dot systems, which can be used to implement two-qubit gates and more complex quantum operations. In a double quantum dot system, we need to consider two coupling contributions:
1. **Capacitive Coupling**: Each dot has its own capacitance to the surrounding electrodes (source, drain, gate), as well as a mutual capacitance between the two dots. This mutual capacitance allows for electrostatic interactions between the dots, enabling control over their charge states through gate voltages.
2. **Tunnel Coupling**: Electrons can tunnel between the two dots if they are close enough and the potential barrier between them is sufficiently low. This tunneling process allows for coherent exchange of electrons between the dots, which is essential for implementing two-qubit gates.

##### Capacitive Coupling
Modelled by a capacitance term $C_m$ between the two dots. 
For a large distance between the dots, $C_m = 0$, and the dots behave independently.
![[Pasted image 20260110145825.png]]
As we can understand from the graph, the two gate voltages $V_{G1}$ and $V_{G2}$ can be used to control the charge states of each dot independently when they are far apart (no mutual capacitance). Resulting in a table-like stability diagram.

When the dots are brought closer together, the mutual capacitance $C_m$ becomes significant, leading to electrostatic interactions between the dots. This interaction modifies the stability diagram, resulting in a honeycomb pattern.
![[Pasted image 20260110145956.png]]
Now each cross point in the honeycomb is split into two triple points, where three charge configurations are degenerate. Only these points allow for current flow from source to drain. The distance between the triple points is proportional to the mutual capacitance $C_m$, which quantifies the strength of the capacitive coupling between the dots.
![[Pasted image 20260110150458.png]]
The distance between the triple points in also proportional to the inter-dot Coulomb interaction energy $E_{Cm}$, which represents the energy cost of adding an electron to one dot while the other dot is occupied. 

![[Pasted image 20260110150352.png]]
This image shows that if we increase the bias window enough, we can have multiple energy levels within the bias window, allowing for more complex transport phenomena between the dots.

##### Tunneling Coupling 
When the two quantum dots are brought very close together, electrons can tunnel between them, leading to coherent coupling. This configuration resembles that of molecular orbitals in diatomic molecules, where the individual atomic orbitals combine to form bonding and antibonding states.
So basically from the individual energy levels of each dot $\phi_1$ and $\phi_2$, we get the formation of new hybridized energy levels: bonding $\psi_B$ and antibonding $\psi_A$ states:
$$\psi_B = \alpha \phi_1 + \beta \phi_2 \quad \text{with energy} \quad -|t_C|$$
$$\psi_A = \alpha \phi_1 - \beta \phi_2 \quad \text{with energy} \quad +|t_C|$$
Where $t_C$ is the tunnel coupling strength between the dots, and $\alpha$ and $\beta$ are coefficients that depend on the specific system parameters.
We call detuning $\epsilon$ the the energy difference between the individual dot levels, and it measure the degree of mixing between the two dot states. 
![[Pasted image 20260110153548.png]]
The solution of the system will start bending when we change the detuning, which can be controlled through the gate voltages. So basically when we increase the detuning, the bonding and antibonding energy levels will deviate more from the original dot levels, indicating stronger hybridization between the states.
![[Pasted image 20260110153827.png]]
We can visualize the detuning as a line in the stability diagram, representing the energy difference between the two dots as we vary the gate voltages. As we can see the effect of detuning is that it modifies the energy levels of the coupled quantum dot system, leading to the formation of bonding and antibonding states, which allow for coherent electron tunneling between the dots even before and after the two triple points.

![[Pasted image 20260110154141.png]]

![[Pasted image 20260110154007.png]]
Basically what we to do by increasing the detuning is to move from a configuration where both electrons are in dot 1 ($N(2,0)$), to a configuration where each dot has one electron ($N(1,1)$), and finally to a configuration where both electrons are in dot 2 ($N(0,2)$), this is achieved by effectively lowering the energy levels of dot 2 relative to dot 1.
We see 2 energy levels, which correspond to the bonding and antibonding states formed due to the tunnel coupling between the dots. The energy difference between these levels is determined by the tunnel coupling strength $t_C$. 

##### Spin States in Double Quantum Dots
If only one of the dots is occupied by a single electron, the situation is similar to that of a single quantum dot qubit, with spin-up and spin-down states split by the Zeeman energy.
![[Pasted image 20260112104549.png]]

If both dots are occupied by one one electron each, the combined spin states of the two electrons can form either a singlet state or one of three triplet states, but it is a little more complicated than the single dot case, since the energy ladder now strongly depends on the detuning between the two dots.
We have four possible spin configurations:
1. **Singlet State (S)**: The two electrons have opposite spins, resulting in a total spin of 0. The singlet state is symmetric in space and antisymmetric in spin:
	 $$|S\rangle = \frac{1}{\sqrt{2}}(|\uparrow_1\downarrow_2\rangle - |\downarrow_1\uparrow_2\rangle)$$
	![[Pasted image 20260112110409.png]]
2. **Triplet State with Zero Spin Projection (T0)**: The two electrons have opposite spins, resulting in a total spin of 1 but with zero spin projection along the quantization axis $S_Z = 0$, the state is symmetric in spin and antisymmetric in space:
	 $$|T_0\rangle = \frac{1}{\sqrt{2}}(|\uparrow_1\downarrow_2\rangle + |\downarrow_1\uparrow_2\rangle)$$
	Unlike the $N(0,2)$ configuration, in the $T_0(1,1)$ configuration the electrons are in different dots, so the Pauli exclusion principle doesn't prevent the electrons from staying in the same orbital state, they are already spatially separated. This results in a not so marked energy difference between the singlet and triplet state $T_0$ in the (1,1) configuration. But this difference $J$ highly depends on the detuning between the two dots.
	![[Pasted image 20260112110819.png]]
	![[Pasted image 20260112110826.png]]
3. **Triplet State with Positive Spin Projection(T+)**: Both electrons have spin-up, resulting in a total spin of 1 with a spin projection of -1 along the quantization axis $S_Z = -1$, since both electrons lie in the ground state orbital of their respective dots, this state is lower in energy than the triplet and singlet states where one electron occupies an excited orbital:
	 $$|T_+\rangle = |\uparrow_1\uparrow_2\rangle$$
	![[Pasted image 20260112111041.png]]
4. **Triplet State with Negative Spin Projection(T-)**: Both electrons have spin-down, resulting in a total spin of 1 with a spin projection of +1 along the quantization axis $S_Z = +1$, since both electrons lie in the excited state orbital of their respective dots, this state is higher in energy than the triplet and singlet states where one electron occupies the ground orbital:
	 $$|T_-\rangle = |\downarrow_1\downarrow_2\rangle$$
	![[Pasted image 20260112111123.png]]

##### Comparing $N(0,2)$ and $N(1,1)$ Configurations in Terms of Total Energy
![[Pasted image 20260112111450.png]]
In the energy-detuning diagram, we can compare the total energies of the singlet and triplet states in both the (0,2) and (1,1) charge configurations as a function of detuning $\epsilon$.
As the detuning $\epsilon$ increases, we start from a $N(2,0)$ configuration where both electrons are in dot 1, then we move to a $N(1,1)$ configuration where each dot has one electron, and finally we reach a $N(0,2)$ configuration where both electrons are in dot 2. 
This happens because by increasing the detuning, we are effectively lowering the energy levels of dot 2 relative to dot 1, making it energetically favorable for both electrons to occupy dot 2 at high detuning values.
As we introduce a magnetic field, the states start to hybridize, meaning that they mix together due to the tunnel coupling between the dots, this results in the formation of bonding and antibonding states for both the singlet and triplet configurations. 
Before applying the magnetic field, the singlet and triplet states are degenerate at zero detuning, but after applying the field, they split into separate energy levels due to the Zeeman effect.
![[Pasted image 20260112112251.png]]
Only the singlets hybridize with the singlet, and the triplets with the triplet, since they have different spin magnetic moments.
![[Pasted image 20260112112502.png]]
The energy difference $J$ increases with detuning, because as we move towards the (0,2) configuration, the electrons are forced to occupy the same dot, leading to a stronger exchange interaction between their spins. This results in a larger energy splitting between the singlet and triplet states.
![[Pasted image 20260112112602.png]]
In this last slide we focus on the zone where the next qubit (singlet-triplet qubit) will operate.

#### Singlet-Triplet ($S-T_0$) Qubit
![[Pasted image 20260112113035.png]]
The singlet-triplet qubit is a type of quantum bit that utilizes the spin states of two electrons confined in a double quantum dot system. They are coupled both capacitively and through tunneling, allowing for coherent manipulation of their spin states.
The static magnetic field $B_Z$ is applied to lift the spin degeneracy through the Zeeman effect, but the effect of the magnetic field is not the same on both dots, since they can experience slightly different magnetic fields due to different locations or local magnetic field gradients. So $B_{Z1} \neq B_{Z2}$.
We will now describe different manipulations that can be performed on the singlet-triplet qubit, focusing on the key steps involved in its operation.
##### Initialization
![[Pasted image 20260112113322.png]]
The double dot is initialized in the (0,2) charge configuration, where both electrons occupy dot 2. By adjusting the gate voltages, we ensure that only the singlet state $S(0,2)$ is energetically allowed within the bias window. 
![[Pasted image 20260112113523.png]]
If we want to see the logic behind the states of the qubit we can use the Bloch Sphere representation, where the north pole represents the singlet state $|S\rangle$ and the south pole and the south pole represents the triplet state $|T_0\rangle$.  
![[Pasted image 20260112113719.png]]
##### Lowering the Detuning
![[Pasted image 20260112113803.png]]
After initialization, we lower the detuning $\epsilon$ by adjusting the gate voltages, transitioning the system from the (0,2) charge configuration to the (1,1) configuration. This allows each dot to host one electron, enabling coherent manipulation of their spin states.
By lowering the detuning, the energy difference $J$ between the singlet and triplet states decreases, allowing for coherent superpositions of these states to be formed.
![[Pasted image 20260112113911.png]]
![[Pasted image 20260112113940.png]]
On the contrary, the difference in Zeeman splitting between the two dots $\Delta E_{Z1}- \Delta E_{Z2}$ becomes more significant, so that $|\uparrow\downarrow\rangle$ and $|\downarrow\uparrow\rangle$ are no longer degenerate, so that:
$\psi(R,t)= \psi(R,0) e^{-i \frac{(\Delta E_{Z1}- \Delta E_{Z2})}{\hbar} t}$
This results in a relative phase accumulation between the singlet and triplet states over time, leading to coherent oscillations between these states.
In this step $|S\rangle$ and $|T_0\rangle$ are no longer eigenstates of the system, $|\uparrow\downarrow\rangle$ and $|\downarrow\uparrow\rangle$ are the new basis of the system.
![[Pasted image 20260112114435.png]]
![[Pasted image 20260112114440.png]]
##### Dephasing
![[Pasted image 20260112114519.png]]
A time $\tau_{S}$ is waited at low detuning, allowing the system to evolve from $S(1,1)$ in time, accumulating a relative phase between the singlet and triplet states due to the difference in Zeeman splitting between the two dots.
The initial state $|S\rangle$ in which the system is when the detuning is lowered, can be written in the new basis as:
$$\psi(t=0) = |S\rangle = \frac{1}{\sqrt{2}} (|\uparrow\downarrow\rangle - |\downarrow\uparrow\rangle)$$
This system evolves in time. Because the two new stationary states differ in energy by $\Delta E_{\uparrow\downarrow - \downarrow\uparrow} = \Delta E_{Z1}- \Delta E_{Z2}$, the time dependent wavefunction solution will be:
$$|\psi(t)\rangle = \frac{1}{\sqrt{2}} \left( e^{i \frac{\Delta E_{\uparrow\downarrow - \downarrow\uparrow}}{2 \hbar} t} |\uparrow\downarrow\rangle - e^{-i \frac{\Delta E_{\uparrow\downarrow - \downarrow\uparrow}}{2 \hbar} t} |\downarrow\uparrow\rangle \right)$$
We call $a=\frac{\Delta E_{\uparrow\downarrow - \downarrow\uparrow}}{2 \hbar}t$, and we remember that:
$$e^{i a} = cos a + i sin a$$
$$e^{-i a} = cos a - i sin a$$
So we can rewrite the wavefunction as a state of the qubit, so $|S\rangle$ and $|T_0\rangle$ basis:
$$|\psi(t)\rangle = cos (a)|S\rangle + i sin (a) |T_0\rangle$$
So basically the system is oscillating between the singlet and triplet states at a frequency determined by the energy difference between the two states, which is controlled by the difference in Zeeman splitting between the dots (very important). By waiting a time $\tau_S$, we can control the final state.
![[Pasted image 20260112115547.png]]
![[Pasted image 20260112115602.png]]
##### Increasing the Detuning
The detuning $\epsilon$ is increased so that the energy difference $J$ between the singlet and triplet states becomes significant again. On the contrary, in this regime the difference in Zeeman splitting between the two dots $\Delta E_{Z1}- \Delta E_{Z2}$ becomes negligible.
So now the eigenstates of the system are again $|S\rangle$ and $|T_0\rangle$,
![[Pasted image 20260112115834.png]]
![[Pasted image 20260112115846.png]]
![[Pasted image 20260112115908.png]]
##### Exchange
![[Pasted image 20260112115936.png]]
In this step, we wait a time $\tau_{E}$ at high detuning, allowing the system to evolve under the influence of the exchange interaction $J$ between the two electrons.
Now the final state of the system after the exchange interaction can be expressed as:
$$|\psi(t)\rangle = e^{-i \frac{J}{\hbar} t} |\psi(t = \tau_S)\rangle$$
Where $|\psi(t = \tau_S)\rangle$ is the state of the system after the dephasing step. The free oscillation results in a phase accumulation between the singlet and triplet states. So with a combination of the dephasing and exchange steps, we can achieve arbitrary rotations on the Bloch Sphere of the singlet-triplet qubit.
![[Pasted image 20260112120308.png]]
![[Pasted image 20260112120333.png]]
##### Readout
![[Pasted image 20260112120410.png]]
The detuning $\epsilon$ is significantly increased so that we find our system wither in the $S(0,2)$ or $T_0(1,1)$ configuration. The right reservoir chemical potential is lowered, so that only the transition from (0,2) to (0,1) is energetically allowed within the bias window.
![[Pasted image 20260112120552.png]]
If the state of the qubit is $S(0,2)$, one electron of the right dot can tunnel to the right reservoir, so that a current can be measured.
![[Pasted image 20260112120720.png]]
If the state of the qubit is $T_0(1,1)$, since the other triplet states $T_+(1,1)$ and $T_-(1,1)$ are higher in energy, there's no possibility for an electron to tunnel to the other dot, and so from the right dot to the reservoir, so no current is measured. And the triplet to singlet transition is forbidden by the Pauli exclusion principle.
![[Pasted image 20260112120742.png]]
![[Pasted image 20260112120954.png]]
## References
