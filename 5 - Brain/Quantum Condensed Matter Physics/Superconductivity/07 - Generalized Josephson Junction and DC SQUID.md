
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





## References
