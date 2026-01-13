
2026-01-12 18:58

Status: 

Tags:

# 05 - Flying Electron Qubit
Flying electron qubits are realized in high mobility, doped GaAs/AlGaAs heterostructures.  
By placing metallic Schottky gates on the surface of the heterostructure, one can model the geometry of the 2DEG. The application of a negative voltage to the gate depletes the 2DEG, due to the repulsion of electrons by the gate generating an electric field. This method allows for the alteration of the 2DEG geometry, which is crucial for the manipulation of quantum states.
#### Flying electron qubits 
In its most basic form, the flying electron qubit is a propagating electron within 2 identical waveguides. 
The qubit states $|0\rangle$ and $|1\rangle$ are represented by the electron propagating in either of the waveguides. The waveguides are brought close together and a tuneable barrier is placed between them. By tuning the barrier with an applied gate voltage, one can control the superposition of the qubit states, changing effectively the tunneling rate between the waveguides.
![[Pasted image 20260113111349.png]]
![[Pasted image 20260113111513.png]]
The exchange process resembles the one occurring in charge qubits, where tunnelling coupling occurs between the two quantum dots. Basically, when the waveguides are far apart, $t_C = 0$, the electrons are described by the wavefunctions of each waveguide. $t_C$ is function of the distance between the waveguides and the applied gate voltage $V_{ext}$.

![[Pasted image 20260113111524.png]]
When the waveguides are brought close together, the tunneling coupling $t_C$ is non-zero and the electron can tunnel between the two waveguides, effectively creating a superposition of the two states, since the electrons are now described by a linear combination of the wavefunctions of each waveguide. So now we will have the bonding and antibonding states, which are the symmetric and antisymmetric combinations of the wavefunctions of each waveguide.
$$|B\rangle = \frac{1}{\sqrt{2}} (|0\rangle + |1\rangle) \quad \text{with energy} \quad -|t_C|$$
$$|A\rangle = \frac{1}{\sqrt{2}} (|0\rangle - |1\rangle) \quad \text{with energy} \quad +|t_C|$$
Now $|B\rangle$ and $|A\rangle$ are the eigenstates of the system, with an energy splitting of $\Delta E = 2|t_C|$.
![[Pasted image 20260113111855.png]]
![[Pasted image 20260113111902.png]]

##### Bloch Sphere for Flying Electron Qubit
The state of the flying electron qubit can be represented on on a Bloch sphere, where the north pole represents the state $|0\rangle$ (upper waveguide) and the south pole represents the state $|1\rangle$ (lower waveguide). While the bonding and antibonding states lie on the equator of the sphere. Any point on the surface of the sphere represents a superposition of the two states.
![[Pasted image 20260113112042.png]]
##### Free Oscillation of the Electron
The initial state $|0\rangle$ (electron in the upper waveguide) can be expressed as a superposition of the bonding and antibonding states:
$$|\psi(t=0)\rangle = |0\rangle = \frac{1}{\sqrt{2}} (|B\rangle + |A\rangle)$$
By remembering that the time evolution of an eigenstate (stationary state) is given by:
$$|\psi(R,t)\rangle = \psi(R)e^{-i E t / \hbar} $$
We can write the time evolution of the initial state as:
$$|\psi(t)\rangle = \frac{1}{\sqrt{2}} (|B\rangle e^{-i \frac{\Delta E}{2\hbar} t} + |A\rangle e^{i \frac{\Delta E}{2\hbar} t})$$




## References
