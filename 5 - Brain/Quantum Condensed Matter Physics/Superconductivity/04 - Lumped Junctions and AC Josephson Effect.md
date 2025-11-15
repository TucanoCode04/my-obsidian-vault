
2025-11-15 13:03

Status: 

Tags:

# Lumped Junctions and AC Josephson Effect
Many technical applications are based on Josephson junctions where both the gauge-invariant phase difference $\psi(t)$ across the junction and the current density $J_s(t)$ through the junction can be considered uniform over the junction area. These are called lumped junctions. 
From the spatial integral of the current-phase relationship we obtain the total supercurrent $i(t)$ flowing through the junction:
$$i(t) = \int_S J_s(t) dS = I_c \sin(\psi(t))$$
We get this result because $J_s(t) = J_c \sin(\psi(t))$ is constant over the junction area $S$, so we can take it out of the integral, and the critical current $I_c = J_c S$(density multiplied by area) is the maximum supercurrent that can flow through the junction without voltage appearing across it.
From the gauge-invariant phase relationship we have that the gauge-invariant phase difference $\psi(t)$ is:
$$\psi(t) = \theta_1(t) - \theta_2(t) - \frac{2\pi}{\Phi_0} \int_{1}^{2} \vec{A}(t) \cdot d\vec{l}$$
Where $\theta_1(t)$ and $\theta_2(t)$ are the phases of the superconducting order parameters in the two electrodes forming the junction, and the integral accounts for the effect of any magnetic field present in the junction region.
From the voltage-phase relationship we have that the voltage drop $V(t)$ across the junction is related to the time derivative of the phase difference $\psi(t)$ by:
$$\frac{d\psi(t)}{dt} = \frac{2\pi}{\Phi_0} \int_{1}^{2} \vec{E}(\vec{r},t) \cdot d\vec{l} \quad \Rightarrow \quad V(t) = \frac{\Phi_0}{2\pi} \frac{d\psi(t)}{dt}$$
Where we have used that the voltage is the line integral of the electric field across the junction
The general form of the inductance of a Josephson junction, meaning the property that relates the voltage across the junction to the time derivative of the current through it, is given by:
- rewriting the voltage-phase relationship $V(t) = \frac{\Phi_0}{2\pi} \frac{d\psi}{dt}$ as $\frac{d\psi}{dt} = \frac{2\pi}{\Phi_0} V(t)$
- substituting this into the time derivative of the current-phase relationship $i(t) = I_c \sin(\psi(t))$, yielding:
$$\frac{di}{dt} = I_c \cos(\psi(t)) \frac{d\psi}{dt} = I_c \cos(\psi(t)) \frac{2\pi}{\Phi_0} V(t)$$
Rearranging this expression gives:
$$V(t) = \frac{\Phi_0}{2\pi I_c \cos(\psi(t))} \frac{di}{dt}$$
Which is the current-voltage relationship of an inductor with a time-varying inductance $V = L \frac{di}{dt}$, where the kinetic inductance for any time evolution of the phase difference $\psi(t)$ across the junction is:
$$L (\psi(t)) = \frac{\Phi_0}{2\pi I_c \cos(\psi(t))} = \frac{L_{J}}{\cos(\psi(t))}$$
Where $L_{J} = \frac{\Phi_0}{2\pi I_c}$ is the Josephson inductance, a characteristic constant of the junction. 
The inductance is called kinetic because it arises from the inertia(kinetic energy originated by the mass of Cooper pairs) of the superconducting carriers tunneling through the junction barrier. In normal inductors, the inductance arises from the magnetic field energy stored in the magnetic field around the conductor. 
So basically the superelectrons will store the energy in their motion through the junction, instead of in the magnetic field around it, and to change state (the current flowing through the junction) we need to overcome this inertia by either slowing down or speeding up the superelectrons, which requires a voltage across the junction.

**Summary of what we have learned so far:**
The state of the junction is described by two quantities:
- The supercurrent $i(t) = I_c \sin(\psi(t))$ flowing through it
- The phase difference $\psi(t)$ across it, that determines the supercurrent
So basically changing the current requires changing the phase difference.
The Josephson relation connects the phase difference to the voltage across the junction:
$$\frac{d\psi}{dt} = \frac{2\pi}{\Phi_0} V(t)$$
Meaning that to change the phase difference we need to apply a voltage across the junction.
Before changing the voltage we must know how the voltage relates to the current, which is given by the kinetic inductance:
$$V(t) = L(\psi(t)) \frac{di}{dt} = \frac{\Phi_0}{2\pi I_c \cos(\psi(t))} \frac{di}{dt}$$
This means that to change the current we need to apply a voltage across the junction, and the amount of voltage required depends on the current state of the junction (the phase difference $\psi(t)$).
- $\frac{\Phi_0}{2\pi I_c }$ is the Josephson inductance, this is the intrinsic inertia of the Cooper pairs tunneling through the junction, this value sets the scale for how much voltage is needed to change the current.
- $\frac{1}{\cos(\psi(t))}$ is a state-dependent factor that increases the effective inductance as the phase difference approaches $\pm \frac{\pi}{2}$, where the supercurrent reaches its maximum value $I_c$. This means that as we approach the critical current, it becomes increasingly difficult to change the current, requiring larger voltages.
- $\frac{di}{dt}$ is the rate of change of the current, meaning that faster changes in current require larger voltages.
To show the dependence of the inductance on the phase difference, we have seen that the kinetic inductance can be expressed as:
$$L (\psi(t)) = \frac{L_{J}}{\cos(\psi(t))}$$
- When $\psi(t) = 0$, $\cos(0) = 1$, so $L(0) = L_J$. This is the minimum inductance, corresponding to the junction being at rest with no supercurrent flowing.
- As $\psi(t)$ approaches $\pm \frac{\pi}{2}$, $\cos(\psi(t))$ approaches 0, causing $L(\psi(t))$ to increase towards infinity. This indicates that the junction becomes increasingly inductive as it approaches the critical current, making it harder to change the current.
- When $\psi(t) = \pm \pi$, $\cos(\pm \pi) = -1$, so $L(\pm \pi) = -L_J$. This negative inductance indicates a phase inversion, where the junction can support a supercurrent in the opposite direction.



## References
