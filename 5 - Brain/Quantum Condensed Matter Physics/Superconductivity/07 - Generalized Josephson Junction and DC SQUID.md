
2025-11-18 13:05

Status: 

Tags:

# Generalized Josephson Junction and DC SQUID
Again, the mechanisms that allow electric current to flow through a superconducting tunnel junction are:
- **Coherent**: Tunneling of Cooper pairs(inductive) for $i < I_c$ and $V < 2\frac{\Delta}{e}$.(Josephson Tunneling)
- **Incoherent**: Quasiparticle tunneling(resistive) for $i \geq I_c$ and $V \geq 2\frac{\Delta}{e}$.(Giaever Tunneling)
- **Capacitive**: Coupling between the two superconductor leads across the insulating barrier where $C = \epsilon \frac{wd}{2a}$. Relevant in AC regime.
In a generalized Josephson junction, all three mechanisms are considered.

We studied the coherent Josephson tunneling in basic Junctions to be: $$i = I_c \sin(\varphi)$$
For an ideal tunnel junction the capacitive channel is simply that of a capacitor: $$i = C \frac{dV}{dt}$$
The resistive channel stems from the breaking of Cooper pairs into quasiparticles(normal electrons)(we need microscopic BCS theory to fully understand this process). To give a quantitative understanding:
- Superconducting Junction: superelectrons do not scatter since they are in a collective ground state. The phase function is well defined since all superelectrons are in the same quantum state. $$\frac{di}{dt} = \frac{2\pi I_c}{\Phi_0} V(t) \cos(\varphi)$$Where $\frac{2\pi I_c}{\Phi_0}$ is the Josephson inductance(kinetic inductance) of the junction.
- Normal Junction: normal electrons scatter off impurities and phonons, these collisions lead to an exchange of energy and momentum. Thus, the phase coherence is lost and we utilize a damping time $\tau_i$ to describe the average time between collisions. $$\frac{di}{dt} + \frac{i}{\tau_i} = \frac{2\pi I_c}{\Phi_0} V(t) $$Meaning that in case of no voltage we will have no current. The $\cos(\varphi) = 1$ since the phase is randomized due to scattering leaving and average value of zero $\langle \cos(\varphi) \rangle = 0$.(So $\cos(0) = 1$)

If we consider the normal junction to be driven by a DC voltage $V(t) = V$ constant:$$\frac{di}{dt} + \frac{i}{\tau_i} = \frac{2\pi I_c}{\Phi_0} V(t) $$ The solution is: $$\frac{i}{\tau_i} = \frac{2\pi I_c}{\Phi_0} V $$
Thus, the junction conductance is: $$(R_n)^{-1} = \frac{i}{V} = \frac{2\pi I_c \tau_i}{\Phi_0} $$Where $R_n$ is the normal state resistance of the junction. This implies that:
$$I_c R_n = \frac{\Phi_0}{2 \pi \tau_i} = \text{constant}$$

We found that the normal state resistance $R_n$ is inversely proportional to the critical current $I_c$. One finds experimentally that:$$I_c R_n = \frac{\pi \Delta_0}{2 e} $$
Where $\Delta_0$ is the superconducting gap at $T = 0K$. 
The time dependent non linear resistive conductance is given by: 
$$G(V) = \begin{cases}
0 \quad \text{if} \quad |V| < 2\frac{\Delta}{e} \\
\frac{1}{R_n} \quad \text{if} \quad |V| \geq 2\frac{\Delta}{e}
\end{cases}$$
![[Pasted image 20251119121732.png]]
The graph show in the x-axis the microvolts representing the voltage across the junction and in the y-axis the current through the junction in microamperes. The different curves(for different temperatures) show the I-V characteristics, where the gap $2\frac{\Delta}{e}$ decreases with increasing temperature until it vanishes at $T_c = 1.250K$ for Aluminum. We can see the tunneling of Cooper pairs at low voltages and the onset of quasiparticle tunneling at voltages above the gap.

The generalized Josephson junction can thus be modeled as the parallel combination the three channels.
![[Pasted image 20251119122305.png]]
The total current through the junction is given by: $$i = I_c \sin(\varphi) + V G(V) + C \frac{dV}{dt} $$
Exploiting the phase-voltage relation: $$i = I_c \sin(\varphi) + G(V) \frac{\Phi_0}{2\pi} \frac{d\varphi}{dt} + C \frac{\Phi_0}{2\pi} \frac{d^2 \varphi}{dt^2} $$This is a non linear equation of non linear coefficients(since $G(V)$ is non linear) that describes the dynamics of a generalized Josephson junction. Numerical solution are then required to study the behavior of the junction in different regimes.

A simplified version RSCJ model replaces the non linear conductance $G(V)$ with a constant resistance $R$:
![[Pasted image 20251119123244.png]]
The total current through the junction is given by: $$i = I_c \sin(\varphi) + \frac{\Phi_0}{2\pi R} \frac{d\varphi}{dt} + C \frac{\Phi_0}{2\pi} \frac{d^2 \varphi}{dt^2} $$This constant is e



## References
