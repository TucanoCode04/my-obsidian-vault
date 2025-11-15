
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
Where we have used that the voltage is the line integral of the electric field across the junction since there's no dependence on $y$ and $z$ coordinates in a lumped junction.(Look this up better)
We will always only consider current restricted to be supercurrent, so less than the critical current $I_c$.
##### Dynamics when driven by a current source
Let's now consider the dynamics of the lumped Josephson junction when driven by a current source.
The source will slowly increase the current $i(t)$ flowing through the junction from zero to some steady state value.
![[Pasted image 20251115172957.png]]
The phase varies according to the current-phase relationship:
$$i(t) = I_c \sin(\psi(t)) \quad \Rightarrow \quad \psi(t) = \arcsin\left(\frac{i(t)}{I_c}\right)$$
![[Pasted image 20251115173140.png]]
The time-dependent phase creates a finite voltage across the junction according to the voltage-phase relationship:
$$V(t) = \frac{\Phi_0}{2\pi} \frac{d\psi(t)}{dt} = \frac{\Phi_0}{2\pi} \frac{1}{\sqrt{1 - \left(\frac{i(t)}{I_c}\right)^2}} \frac{1}{I_c} \frac{di(t)}{dt}$$
![[Pasted image 20251115173315.png]]
As long as the current varies in time, then both current(so the phase) and voltage will be non-zero.
The lumped Josephson junction behaves like a non-linear inductor, meaning that the voltage across the junction is proportional to the time derivative of the current through it, with a proportionality factor that depends on the current state of the junction.
##### Kinetic Inductance of a Josephson Junction
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

The kinetic inductance of a Josephson junction enables it to store energy when a supercurrent flows through it, and this energy can be released when the current is changed. 
We have seen that when a Josephson junction is driven by a time-varying current  there exist a finite time where both current and voltage are non-zero.
The energy stored in the junction can be calculated by integrating the power(the product of voltage and current) over time:
$$W_J = \int_0^{t_0} i(t) V(t) dt = \int_0^{t_0} I_c \sin(\psi(t)) \cdot \frac{\Phi_0}{2\pi} \frac{d\psi(t)}{dt} dt = \frac{\Phi_0 I_c}{2\pi} \int_0^{\psi} \sin(\psi) d\psi$$
$$ \Rightarrow W_J = W_J(0)\left[1 - \cos \psi(t) \right] \quad \text{where} \quad W_J(0) = \frac{\Phi_0 I_c}{2\pi}$$
This expression shows that the energy stored in the junction depends sinusoidally and is bond by the critical current $I_c$ and it lags behind the time evolution of the phase difference $\psi(t)$. In other words, the energy stored in the junction increases as the phase difference increases, reaching a maximum when the phase difference is $\pi$, and then decreases as the phase difference continues to increase.
![[Pasted image 20251115180305.png]]
The sinusoid dotted line shows the energy stored in the junction as a function of the phase difference $\psi(t)$, while the solid line shows the current as a function of the phase difference.(Look it up better)
So again the crucial difference between a Josephson junction and a normal inductor is that:
- a magnetic-coil inductor stores energy in the magnetic field created around the conductor when current flows through it.
- a Josephson junction stores energy in the kinetic energy of the Cooper pairs tunneling through the junction barrier when supercurrent flows through it, and no magnetic field is created around it.
##### Dynamics when driven by a constant voltage source
Now let's consider the dynamics of the lumped Josephson junction when driven by a voltage source.
The source will apply a constant voltage $V(t) = V_0$ across the junction.
![[Pasted image 20251115183128.png]]
From the voltage-phase relationship we have that the phase difference $\psi(t)$ across the junction evolves linearly in time with a rate proportional to the applied voltage:
$$\frac{d\psi(t)}{dt} = \frac{2\pi}{\Phi_0} V_0 \quad \Rightarrow \quad \psi(t) = \psi(0) + \frac{2\pi}{\Phi_0} V_0 t$$
![[Pasted image 20251115183208.png]]
From the current-phase relationship we have that the supercurrent $i(t)$ flowing through the junction oscillates sinusoidally in time with a frequency proportional to the applied voltage and the magnetic flux quantum(that is the smallest unit of magnetic flux(which is the surface integral of the magnetic field over an area) that can exist in a superconductor):
$$i(t) = I_c \sin\left(\psi(0) + \frac{2\pi}{\Phi_0} V_0 t\right)$$
![[Pasted image 20251115183406.png]]
Resulting in an AC(since it oscillates in time) supercurrent flowing through the junction even though the applied voltage is constant in time. This is called the AC Josephson effect.

The characteristic frequency(number of oscillations in a second, while the period is the time it takes for a single cycle) of the oscillations can be obtained from the argument of the sine function:
$$i(t) = I_c \sin\left(\psi(0) + \frac{2\pi}{\Phi_0} V_0 t\right) = I_c \sin\left(2\pi f_J t + \psi(0)\right)$$
Where the Josephson frequency $f_J$ is given by:
$$f_J = \frac{V_0}{\Phi_0} = \frac{2e}{h} V_0 = 483.6 \times 10^{12} V_0 \text{Hz}$$
This means that for every microvolt of applied voltage across the junction, the supercurrent oscillates at a frequency of approximately 483.6 GHz.
So the Josephson frequency depends on the applied voltage only through fundamental constants, making it a very precise and stable frequency standard.
This implies that Josephson junctions are perfect voltage-to-frequency converters, which is exploited in applications such as voltage standards and superconducting qubits.
The AC Josephson effect gives a direct path for high precision measurements of the $\frac{e}{h}$ ratio, which is important in quantum metrology.
Since the typical driving voltages are in the order of 10 $\mu$V to 1 mV, the resulting Josephson frequencies are in the range of 5 GHz, hence microwave frequencies. 
So circuits based on Josephson junctions must consider non-lumped effects, since the wavelengths of microwaves are comparable to the dimensions of typical circuits.

The direct application of the AC Josephson effect is used in little applications, since the detection of microwave radiation emitted by a single junction is difficult due to its very low power, typically $1 \mu W$ or less and the mismatch between the junction impedance and free space(meaning the junction does not efficiently radiate into free space).
![[Pasted image 20251115185930.png]]
But the inverse AC Josephson effect is widely used in voltage standards. When a Josephson junction is irradiated with microwave radiation of frequency $f$, the junction generates a DC voltage across it.
![[Pasted image 20251115190100.png]]
The inverse AC Josephson effect is exploited in quantum metrology to create highly accurate and stable over time primary voltage standards, by linking them to the primary standard of time(frequency) based on atomic clocks. 
##### Dynamics when driven by a time-varying voltage source 
The source applies a time-varying voltage $V(t)$ across the junction.
$$V(t) = V_0 + V_S \cos(\omega_S t)$$
$V_0$ is a constant DC voltage offset, while $V_S \cos(\omega_S t)$ is an AC voltage oscillating at frequency $\omega_S$ with amplitude $V_S$.
![[Pasted image 20251115191207.png]]
From the voltage-phase relationship we have that the phase difference $\psi(t)$ across the junction evolves according to:
$$\frac{d\psi(t)}{dt} = \frac{2\pi}{\Phi_0} \left[V_0 + V_S \cos(\omega_S t)\right] \quad \Rightarrow \quad \psi(t) = \psi(0) + \frac{2\pi}{\Phi_0} \left[V_0 t + \frac{V_S}{\omega_S} \sin(\omega_S t)\right]$$
So the phase difference has a linear time evolution modulated by an oscillating term.
![[Pasted image 20251115191310.png]]
From the current-phase relationship we have that the supercurrent $i(t)$ flowing through the junction is:
$$i(t) = I_c \sin\left(\psi(0) + \frac{2\pi}{\Phi_0} \left[V_0 t + \frac{V_S}{\omega_S} \sin(\omega_S t)\right]\right)$$
So the supercurrent oscillates in time following a composition between two oscillations: a linear oscillation at the Josephson frequency determined by the DC voltage offset $V_0$, and a modulation at the driving frequency $\omega_S$ determined by the AC voltage amplitude $V_S$.
![[Pasted image 20251115191509.png]]
The current frequency become a superposition of the constant frequency $f_J = \frac{V_0}{\Phi_0}$, depending on the DC voltage offset, and a sinusoidal modulation at the driving frequency $f_S = \frac{\omega_S}{2\pi}$, depending on the AC voltage amplitude.
The non-linearity of the current-phase relationship allows coupling different frequencies with single frequency sources. In simpler words, by applying a voltage that varies in time at a single frequency, we can generate supercurrents that oscillate at multiple frequencies simultaneously. Because non-linear means that the output is not directly proportional to the input, allowing for mixing and generation of new frequencies.




## References
