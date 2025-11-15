
2025-11-15 13:03

Status: 

Tags:

# Lumped Junctions and AC Josephson Effect
The general form of the inductance of a Josephson junction, meaning the property that relates the voltage across the junction to the time derivative of the current through it, is given by:
- rewriting the voltage-phase relationship $V(t) = \frac{\Phi_0}{2\pi} \frac{d\psi}{dt}$ as $ \frac{d\psi}{dt} = \frac{2\pi}{\Phi_0} V(t)$
- substituting this into the time derivative of the current-phase relationship $i(t) = I_c \sin(\psi(t))$, yielding:
$$\frac{di}{dt} = I_c \cos(\psi(t)) \frac{d\psi}{dt} = I_c \cos(\psi(t)) \frac{2\pi}{\Phi_0} V(t)$$
Rearranging this expression gives:
$$V(t) = \frac{\Phi_0}{2\pi I_c \cos(\psi(t))} \frac{di}{dt}$$
Which is the current-voltage relationship of an inductor with a time-varying inductance $V = L \frac{di}{dt}$, where the kinetic inductance for any time evolution of the phase difference $\psi(t)$ across the junction is:
$$L (\psi(t)) = \frac{\Phi_0}{2\pi I_c \cos(\psi(t))} = \frac{L_{J}}{\cos(\psi(t))}$$
Where $L_{J} = \frac{\Phi_0}{2\pi I_c}$ is the Josephson inductance, a characteristic constant of the junction. 
The inductance is called kinetic because it arises from the inertia(kinetic energy originated by the mass of Cooper pairs) of the superconducting carriers tunneling through the junction barrier. In normal inductors, the inductance arises from the magnetic field energy stored in the magnetic field around the conductor. 
So basically the superelectrons will store the energy in their motion through the junction, instead of in the magnetic field around it, and to change state (the current flowing through the junction) we need to overcome this inertia by either slowing down or speeding up the superelectrons, which requires a voltage across the junction.

When a constant voltage $V$ is applied across a Josephson junction, the phase difference $\psi(t)$ evolves linearly with time according to the second Josephson relation:


## References
