
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
To manipulate the number of electrons in the dot, we adjust the gate voltage $V_G$, because if we were to change the source or drain voltages, we would create a current flow through the dot, which is not desired when we want to control the electron number precisely. The effect of 
## References
