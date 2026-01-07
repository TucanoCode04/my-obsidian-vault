
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

We define the total capacitance of the dot as: $$C_{dot} =-( C_S + C_D + C_G)$$

## References
