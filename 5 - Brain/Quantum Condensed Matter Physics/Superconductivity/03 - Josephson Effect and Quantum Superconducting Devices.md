
2025-11-12 18:00

Status: 

Tags:

# Josephson Effect and Quantum Superconducting Devices
Tunneling is a quantum mechanical phenomenon where particles pass through a potential barrier that they classically shouldn't be able to cross. This is due to the wave-like nature of of particles, allowing them to have a non-zero probability of being found on the other side of the barrier.
For normal electrons, tunneling can occur in tunneling junctions, where two conductors are separated by a thin insulating barrier. Classically tunnel junctions have infinite impedance at zero frequency, but quantum mechanically, if the barrier is thin enough, electrons can tunnel through it, allowing a small DC(direct current) to cross the junction(It is possible even for AC(alternating current) to cross the junction due to tunneling, but the DC case is more straightforward to understand).
We now first want to analyze a junction made of one conductor, the insulator and a superconductor. 
##### S-I-N(Superconductor-Insulator-Normal metal) Junction
![[Pasted image 20251112221444.png]]
The S-I-N junction consists of a superconductor(S) and a normal metal(N) separated by a thin insulating barrier(I). A voltage V is applied across the junction, with the superconductor at a higher potential than the normal metal, so basically the current flows from the normal metal to the superconductor.
In a S-I-N junction, the superconductor has a gap in its density of states around the Fermi level, while the normal metal has a continuous density of states. When a voltage is applied across the junction, electrons from the normal metal can tunnel into the superconductor only if they have enough energy to overcome the superconducting gap. This results in a characteristic I-V(current-voltage) curve with a threshold voltage corresponding to the superconducting gap.
More specifically Cooper-pairs in the superconductor cannot tunnel into the normal metal as single electrons, they need to break up into two single electrons, each having energy at least equal to the superconducting gap $\Delta$. Therefore, no current flows until the applied voltage V exceeds $\frac{\Delta}{e}$, where e is the electron charge. Beyond this threshold, the current increases as more electrons gain enough energy to tunnel into the superconductor.
![[Pasted image 20251112221522.png]]
So figuratively, the valence band of the normal metal aligns with the conduction band of the superconductor when the voltage exceeds $\frac{\Delta}{e}$, allowing electrons to tunnel through the barrier. In the second figure we can appreciate how we see current flowing only after the voltage exceeds $\frac{\Delta}{e}$.
##### S-I-S(Superconductor-Insulator-Superconductor) Junction and the Josephson Effect
![[Pasted image 20251112222939.png]]
The S-I-S junction consists of two superconductors separated by a thin insulating barrier. In this case, Cooper pairs must be broken in both superconductors for normal electron tunneling to occur. It even requires double the energy compared to the S-I-N junction, to align the valence band of one superconductor with the conduction band of the other superconductor. Therefore, no current flows until the applied voltage V exceeds $\frac{2\Delta}{e}$.
![[Pasted image 20251112223238.png]]
However, a small zero-bias(meaning no voltage applied) current was experimentally observed in S-I-S junctions, which was unexpected based on the probability of normal electron tunneling. This phenomenon is still very unlikely since it's the joint probability of two electrons tunneling simultaneously(direct tunneling of Cooper-pair).
![[Pasted image 20251113105458.png]]
The upper part of the graph shows various regions:
1. $|I| < I_c$ and $V= 0$: A dissipationless supercurrent flows due to the tunneling of Cooper pairs. This is the DC Josephson effect. This current doesn't depend on voltage, on potential drop or on electron moving randomly, it just flows because of the phase difference between the two superconductors. So the current is described by:
$$I = I_c \sin(\phi)$$
	where $I_c$ is the critical current, the maximum supercurrent that can flow without voltage, and $\phi$ is the phase difference between the superconducting wavefunctions on either side of the junction.
2. $0 < V < \frac{2\Delta}{e}$: No quasiparticle current flows since the voltage is below the threshold for breaking Cooper pairs. However, an AC supercurrent can flow due to the AC Josephson effect, cause the phase evolves over time when a voltage is applied following the Josephson relation:
$$\frac{d\phi}{dt} = \frac{2eV}{\hbar}$$
	This produces an AC supercurrent:
$$I(t) = I_c \sin\left(\phi(t)\right) = I_c \sin\left(\phi(0) + \frac{2eV}{\hbar}t\right)$$
	The instantaneous current oscillates between $-I_c$ and $I_c$, the average DC current results then to be zero. Due to the presence of the gap, no quasiparticle current flows in this region. This is why the I-V curve shows zero average current for voltages below $\frac{2\Delta}{e}$.
3. $V \geq \frac{2\Delta}{e}$: Quasiparticle(normal) tunneling occurs as the voltage exceeds the threshold for breaking Cooper pairs. Electrons(important, not Cooper pairs) can now be excited above the superconducting gap of the other superconductor, resulting in a finite quasiparticle current. The I-V curve shows a sharp increase in current beyond this voltage, following the characteristics of a normal resistor:
$$I = \frac{V}{R_N}$$
	where $R_N$ is the normal state resistance of the junction. So the total current in this region is governed by the quasiparticle tunneling current, only a remnant of the supercurrent and the AC Josephson effect is present.
4. $|I| > I_c$: When the current exceeds the critical current $I_c$, a voltage develops across the junction, leading to a resistive state. In this regime, both quasiparticle tunneling and dissipative processes occur, resulting in a finite voltage drop. The I-V curve shows a linear increase in voltage with increasing current. The phase is no longer stationary, and the junction behaves like a normal resistor with resistance $R_N$.

Brian Josephson described this tunneling of Cooper pairs in 1962, saying that the probability amplitude for a Cooper pair to tunnel is the same probability amplitude for a single electron to tunnel, due to the coherent(meaning all the electrons are in the same quantum state) nature of the superconducting state. Thus linking it with the Macroscopic Quantum Model of superconductivity, saying that it is the macroscopic wavefunction that tunnels through the barrier, not individual electrons.
This dissipationless current of Cooper pairs tunneling is limited by the critical current $I_c$.

![[Pasted image 20251113140150.png]]
We consider a current-driven Josephson junction, where a current I is applied across the junction. We want to link the supercurrent at the edges of the junction with the phase difference between the two edges, to calculate the current density distribution across the junction.
The supercurrent density at the edges of the junction is described as:
$$J_0(\pm a, y, z, t)$$
where $a$ is half the width of the insulating barrier, and y and z are the coordinates along the junction.
The phase difference across the junction is given by the difference in the superconducting wavefunction phases on either side of the barrier:
$$\theta_1 - \theta_2 = \theta(-a, y, z, t) - \theta(+a, y, z, t)$$
Before writing the supercurrent density equation, we use two simplifications:
- The are of the junction in the directions y and z is very small($wd$) meaning that the current density in those directions can be considered constant. $J_s(y,z) = J_0$
- We assume the absence of electric and magnetic fields inside the junction, due to the thinness of the insulating barrier. $\vec{A}(x,y,z,t) = 0$, so the vector potential is zero.

So that the supercurrent density:
$$J_s(\pm a, t) = - \frac{1}{\Lambda} \left[\vec{A}(\pm a, t) + \frac{\Phi_0}{2\pi} \nabla \theta(\vec{r}, t)\right]$$
Where $\Lambda$ is the London penetration depth, and $\Phi_0 = \frac{h}{2e}$ is the magnetic flux quantum, becomes:
$$J_0  = - \frac{\Phi_0}{2\pi \Lambda} \nabla \theta(\pm a, t)$$
As we said $J_0$ is constant across the junction, so the gradient of the phase must also be constant.
So even the energy-phase relation:
$$\frac{\partial}{\partial t} \theta(\pm a, t) = -\frac{1}{\hbar} \left[\frac{\Lambda}{2n_s}J_s^2(\pm a, t) + q\phi(\pm a, t)\right]$$
Where $n_s$ is the density of superconducting electrons, and q is the charge of the Cooper pair(2e), becomes:
$$\frac{\partial}{\partial t} \theta(\pm a, t) = -\frac{1}{\hbar} (\frac{\Lambda}{2n_s}J_0^2) = - \frac{\epsilon_0}{\hbar}$$
Where $\epsilon_0 = \frac{mv_s^2}{2}$ is the constant kinetic energy of the superconducting electrons, with $v_s$ being their velocity. Since the phase evolution is completely determined by the kinetic energy of the superconducting electrons, the wavefunction is simply:
$$\Psi(\vec{r}, t) = \Psi(\vec{r})e^{-i \frac{\epsilon_0}{\hbar} t}$$
This is the polar representation of the wavefunction, where the amplitude $\Psi(\vec{r})$ is time-independent and all the time dependence is in the phase factor $e^{-i \frac{\epsilon_0}{\hbar} t}$, but since the change in phase is linear with time(since $\epsilon_0$ is constant) with a rate determined by the kinetic energy of the superconducting electrons, the only term that is now left to determine is the spatial dependence $\Psi(\vec{r})$.
![[Pasted image 20251113181241.png]]
$\Psi(\vec{r})$ is constant in each superconductor. The insulator can be modeled as a potential barrier of height $V_0 > \epsilon_0$ of width $2a$. From the simplifications we made earlier, we can consider a one-dimensional model along the x-axis, perpendicular to the junction $\Psi(x)$.
In the superconductors, the wavefunction satisfies the time-independent Schrödinger equation:
$$-\frac{\hbar^2}{2m} \nabla^2 \Psi(x) = (\epsilon_0 - V(0)) \Psi(x)$$


## References
