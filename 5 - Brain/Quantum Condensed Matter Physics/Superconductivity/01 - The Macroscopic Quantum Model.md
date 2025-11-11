
2025-11-06 18:55

Status: 

Tags:

# The Macroscopic Quantum Model
The London brothers, beginning from classical electrodynamics and assuming that superelectrons do not scatter, derived a partial description of the electrodynamics of superconductors. However the London equations do not account for the microscopic origins of superconductivity. 
Later, they were able to show that their equations could be derived from the Schrödinger equation by describing the superelectrons fluid with a macroscopic wave function. 
They realized that superconductivity is a quantum mechanical phenomenon that manifests itself on a macroscopic scale.
This concept is similar in laser physics, where a large number of photons occupy the same quantum state, leading to coherent light emission, sharing then the same wavefunction.
The hypothesis of the Macroscopic Quantum Model is that all superelectrons in a superconductor can be described by a single macroscopic wave function $\Psi (\vec{r}, t)$, which encapsulates the collective behavior of the superelectrons.
This assumption doesn't explain the microscopic origin of superconductivity, but it places importance on the collective quantum state of the superelectrons.
Like lasers that are described by a single electromagnetic wavefunction. 
So we assume the existence of a great number of charge carriers, making it more useful to consider $\Psi (\vec{r}, t)$ as describing a fluid of superelectrons rather than individual particles.
##### Schrodinger Equation and Macroscopic Quantum Currents
Let us consider the time-dependent Schrödinger equation for a charged particle in electric and magnetic fields:
$$
i \hbar \frac{\partial}{\partial t} \Psi (\vec{r}, t) = \frac{1}{2m} \left( -i \hbar \nabla - q \vec{A} (\vec{r}, t) \right)^2 \Psi (\vec{r}, t) + q \phi (\vec{r}, t) \Psi (\vec{r}, t) $$
where $q$ is the charge of the particle, $m$ is its mass, $\vec{A} (\vec{r}, t)$ is the vector potential, and $\phi (\vec{r}, t)$ is the scalar potential. The vector potential and scalar potential are related to the magnetic field $\vec{B}$ and electric field $\vec{E}$ by:
$$
\vec{B} = \nabla \times \vec{A} $$
$$
\vec{E} = - \nabla \phi - \frac{\partial \vec{A}}{\partial t} $$
We can express the macroscopic wave function $\Psi (\vec{r}, t)$ in terms of its modulus and phase(polar form):
$$
\Psi (\vec{r}, t) = \Psi_0 (\vec{r}, t) e^{i \theta (\vec{r}, t)} $$
where $\Psi_0 (\vec{r}, t)$ is the real-valued modulus(amplitude related to the Cooper-pair density $n_s$) with $\Psi_0(\vec{r}, t)= n_s(\vec{r},t)$ and $\theta (\vec{r}, t)$ is the real-valued phase of the condensate wave function. Dropping the explicit space and time dependence for simplicity, we can substitute this expression into the Schrödinger equation:
$$
i \hbar \frac{\partial \Psi_0}{\partial t} - \hbar \Psi_0 \frac{\partial \theta}{\partial t} = \frac{1}{2m} \left[- \hbar^2 \left(\nabla^2 \Psi_0 + 2 i \nabla \theta \cdot \nabla \Psi_0 + i \Psi_0 \nabla^2 \theta - \Psi_0 (\nabla \theta)^2 \right) + 2i \hbar q \vec{A} \cdot \nabla \Psi_0 - 2 \hbar q \Psi_0 \vec{A} \cdot \nabla \theta + q^2 \vec{A}^2 \Psi_0 \right] + q \phi \Psi_0 $$
##### Macroscopic Quantum Current Density
We now separate the real and imaginary parts of this equation. The imaginary part gives us:
$$
\hbar \frac{\partial \Psi_0}{\partial t} = - \frac{\hbar^2}{2m} \left[ \nabla^2 \theta \Psi_0 + 2 \nabla \theta \cdot \nabla \Psi_0 - \frac{q}{\hbar} \left(2 \vec{A} \cdot \nabla \Psi_0 + \nabla \cdot \vec{A} \Psi_0 \right) \right] $$
By multiplying both sides by $\Psi_0$ and exploiting the identity $\nabla \cdot (\gamma\vec{C})= \gamma \nabla \cdot \vec{C} + \vec{C} \cdot \nabla \gamma$, we can rewrite this equation as a continuity equation:
$$
\frac{\partial}{\partial t} (\Psi_0^2) + \nabla \cdot \left[ \frac{\hbar}{m} \Psi_0^2 \left( \nabla \theta - \frac{q}{\hbar} \vec{A} \right) \right] = 0 $$
This equation describes the conservation of the superelectron density $\Psi_0^2 = n_s$. 
Basically we are calculating how the density of superelectrons changes over time and space, this change is governed by the flow in or out of a given region, given by the divergence of the current density in that region.
This assure us that the Cooper pairs density($n_s$) is conserved in time, meaning that they are neither created nor destroyed within the superconductor. This is the foundation for persistent currents in superconductors.
This is a continuity equation for the quantum probability current density $\vec{J}_p$:
$$
\vec{J}_p = \frac{\hbar}{m} \left( \nabla \theta - \frac{q}{\hbar} \vec{A} \right) $$
The probability current density $\vec{J}_p$ tells us how the probability density of finding superelectrons flows in space and time.
From here, we can define the macroscopic quantum current density $\vec{J}_s$ as:
$$
\vec{J}_s (\vec{r}, t) = q n_s (\vec{r}, t) \vec{J}_p (\vec{r}, t) = \frac{q \hbar}{m} n_s (\vec{r}, t) \left( \nabla \theta (\vec{r}, t) - \frac{q}{\hbar} \vec{A} (\vec{r}, t) \right) $$
This expression relates the macroscopic quantum current density $\vec{J}_s$ to the phase gradient of the macroscopic wave $\nabla \theta$ and the vector potential $\vec{A}$. $\vec{J}_s$ and $n_s$ are measurable quantities in superconductors, while we can't measure and separate the difference inside the parentheses.
To better explain the physical meaning of this expression:
- The term $\nabla \theta$ represents the spatial variation of the phase of the macroscopic wave function. A non-zero phase gradient indicates that there is a flow of superelectrons, leading to a current.
- The term $-\frac{q}{\hbar} \vec{A}$ represents the influence of the magnetic vector potential on the current. The presence of a magnetic field can induce currents in the superconductor, even in the absence of a phase gradient. And the minus sign indicates that the vector potential opposes the phase gradient's contribution to the current, resulting in a net current that depends on the balance between these two effects. The Meissner effect can be explained by this term, as the superconductor generates currents(known as screening currents) that in a state of equilibrium ($\nabla \theta = 0$) oppose the applied magnetic field, leading to its expulsion from the superconductor's interior. 
- The term $n_s$ is the density of superelectrons, which scales the current density. A higher density of superelectrons leads to a larger current for the same phase gradient and vector potential.
- The prefactor $\frac{q \hbar}{m}$ relates the quantum mechanical properties of the superelectrons (charge $q$ and mass $m$) to the current density.
**Note:** The same result can be obtained from the general expression of the macroscopic quantum current density:
$$
\vec{J}_s = q \mathrm{Re} \left\{ \Psi^* \left( \frac{\hbar}{i m} \nabla - \frac{q}{m} \vec{A} \right) \Psi \right\} $$
##### Gauge Invariance
The $J_s$ and $n_s$ are measurable quantities since we they alter the electromagnetic field which can be measured, while $\theta$ is only defined relatively and different $\vec{A}$ can produce the same magnetic field $\vec{B} = \nabla \times \vec{A}$. So we have to check that the expression for $\vec{J_s}$ is Gauge invariant, meaning that different choices of the potentials $\vec{A}$ and $\phi$ that yield the same physical electromagnetic fields $\vec{E}$ and $\vec{B}$ do not affect the value of $\vec{J_s}$.
Now we explain more in details the Gauge invariance of the expression.
Basically, a gauge transformation involves changing the scalar and vector potentials without altering the physical electromagnetic fields. This can be done by introducing a scalar function $\chi (\vec{r}, t)$ and transforming the potentials as follows:
$$
\vec{A}' = \vec{A} + \nabla \chi $$
$$
\phi' = \phi - \frac{\partial \chi}{\partial t} $$
To appreciate that the Gauge decision doesn't affect the electromagnetic fields, we can verify that:
$$
\vec{B}' = \nabla \times \vec{A}' = \nabla \times (\vec{A} + \nabla \chi) = \nabla \times \vec{A} = \vec{B} $$
Since the curl of a gradient is always zero. Similarly, for the electric field:
$$
\vec{E}' = - \nabla \phi' - \frac{\partial \vec{A}'}{\partial t} = - \nabla \left( \phi - \frac{\partial \chi}{\partial t} \right) - \frac{\partial}{\partial t} (\vec{A} + \nabla \chi) = - \nabla \phi - \frac{\partial \vec{A}}{\partial t} = \vec{E} $$
Since the gradient and time derivative operators commute, meaning that the order in which we apply them does not matter and the additional terms cancel out.
Under this transformation, the macroscopic wave function $\Psi$ can be written so that the Gauge invariance holds in this way:
$$
\Psi' (\vec{r}, t) = \Psi_0 e^{i \theta'}$$
We keep the modulus unchanged since the number of superelectrons must remain the same, and so it must hold that $\Psi'^*\Psi' = \Psi^* \Psi = n_s$. The phase transforms as:
$$
\vec{J_s'}= q n_s \frac{\hbar}{m} \left( \nabla \theta' - \frac{q}{\hbar} \vec{A}' \right) = q n_s \frac{\hbar}{m} \left( \nabla \theta - \frac{q}{\hbar} \vec{A} \right) = \vec{J_s} \Leftrightarrow \theta' = \theta + \frac{q}{\hbar} \chi $$
The choice of $\theta'$ is obliged since:
$$
\vec{J_s'}= q n_s \frac{\hbar}{m} \left( \nabla \theta' - \frac{q}{\hbar} \vec{A}' \right) = q n_s \frac{\hbar}{m} \left( \nabla \theta + \frac{q}{\hbar} \nabla \chi - \frac{q}{\hbar} (\vec{A} + \nabla \chi) \right) = q n_s \frac{\hbar}{m} \left( \nabla \theta - \frac{q}{\hbar} \vec{A} \right) = \vec{J_s} $$
So we have shown that under the same Gauge choice both $\vec{A}$ and $\theta$ transform in such a way that the macroscopic quantum current density $\vec{J_s}$ can be measured independently from the Gauge choice.
##### Energy-Phase Relationship and London Equations
The equation we have derived for the macroscopic quantum current density $\vec{J_s}$ is the most general form since it considers the possibility that the superelectron density $n_s$ may vary in space and time. In many practical situations, especially in uniform superconductors, $n_s$ can be treated as a constant, since matter tends towards charge neutrality and its fluctuations are minimal. Small deviations can be later considered as perturbations.
Thus, in the case of a uniform superconductor with a constant superelectron density $n_s$, the expression for the macroscopic quantum current density simplifies to:
$$
\Lambda \vec{J_s} = \frac{\hbar}{q} \nabla \theta(\vec{r}, t) - \vec{A}(\vec{r}, t) $$ where $\Lambda = \frac{m}{q^2 n_s}$ is the isotropic London coefficient.
By taking the curl of the above equation, we can examine the response of the superconductor to magnetic fields:
$$
\nabla \times (\Lambda \vec{J_s(\vec{r}, t)}) = \frac{\hbar}{q} \nabla \times \nabla \theta(\vec{r}, t) - \nabla \times \vec{A}(\vec{r}, t) \quad \Rightarrow \quad \nabla \times (\Lambda \vec{J_s(\vec{r}, t)}) = - \vec{B}(\vec{r}, t)$$
The first term on the right side vanishes because the curl of a gradient is always zero, while the curl of the vector potential $\vec{A}$ gives us the magnetic field $\vec{B}$. This is the **second London equation** and it describes the perfect diamagnetic response of superconductors, leading to the expulsion of magnetic fields from their interior (the Meissner effect).
Field expulsion can be explicitly seen by combining this equation with Maxwell's 4th equation when electric fields are varying slowly in time and by using the vector identity $\nabla \times (\nabla \times \vec{C}) = \nabla (\nabla \cdot \vec{C}) - \nabla^2 \vec{C}$:
$$
\nabla \times \vec{B} = \mu_0 \left( \vec{J_s} + \epsilon_0 \frac{\partial \vec{E}}{\partial t} \right) \approx \mu_0 \vec{J_s} $$
This is the Ampere-Maxwell law, neglecting the displacement current term for slowly varying fields.
By taking the curl of both sides and substituting the second London equation, we get:
$$
\nabla \times (\frac{\Lambda}{\mu_0} \nabla \times \vec{B}) = - \vec{B} \quad \Rightarrow \quad \frac{\Lambda}{\mu_0} \left( \nabla (\nabla \cdot \vec{B}) - \nabla^2 \vec{B} \right) = - \vec{B} $$
The divergence of the magnetic field is zero ($\nabla \cdot \vec{B} = 0$), since the magnetic field is a solenoidal field, leading to:
$$
-\frac{\Lambda}{\mu_0} \nabla^2 \vec{B} = - \vec{B} \quad \Rightarrow \quad -\nabla^2 \vec{B} = -\frac{\vec{B}}{\lambda^2} $$
where $\lambda = \sqrt{\frac{\Lambda}{\mu_0}}$ is the London penetration depth.
This differential equation describes how the magnetic field decays exponentially over a length scale of the penetration depth $\lambda$ inside the superconductor. 
By taking the curl of the expression $\nabla \times(\Lambda \vec{J_s(\vec{r}, t)})) = - \vec{B}(\vec{r}, t)$, we derive:
$$
-\nabla^2 \vec{J_s} = -\frac{\vec{J_s}}{\lambda^2} $$
This equation indicates that the supercurrent density $\vec{J_s}$ also decays exponentially over the same length scale $\lambda$ within the superconductor. 
This 2 equations combined show that any magnetic field is exponentially screened by an induced supercurrent on the surface layer of thickness $\lambda$ of the superconductor, leading to the Meissner effect.
![[Pasted image 20251111122654.png]]
Now we want to recover perfect conductivity, by using the Schrödinger equation:
$$
i\hbar \frac{\partial \Psi_0}{\partial t} - \hbar \Psi_0 \frac{\partial \theta}{\partial t} = \frac{1}{2m} \left[- \hbar^2 \left(\nabla^2 \Psi_0 + 2 i \nabla \theta \cdot \nabla \Psi_0 + i \Psi_0 \nabla^2 \theta - \Psi_0 (\nabla \theta)^2 \right) + 2i \hbar q \vec{A} \cdot \nabla \Psi_0 - 2 \hbar q \Psi_0 \vec{A} \cdot \nabla \theta + q^2 \vec{A}^2 \Psi_0 \right] + q \phi \Psi_0 $$
We take the real part of the equation, the intuition behind this is that the real part contains information about the energy of the system, while the imaginary part relates to the probability current and conservation of probability.
$$
- \hbar \Psi_0 \frac{\partial \theta}{\partial t} = \frac{1}{2m} \left[- \hbar^2 \left( \nabla^2 \Psi_0 - \Psi_0 (\nabla \theta)^2 \right) - 2 \hbar q \Psi_0 \vec{A} \cdot \nabla \theta + q^2 \vec{A}^2 \Psi_0 \right] + q \phi \Psi_0 $$
This time we also have the scalar potential $\phi$ term, which represents the electric potential energy per unit charge which will give us information about the voltage in devices.
Since we assume a uniform superconductor with constant superelectron density $n_s = \Psi_0^2$, the spatial derivatives of $\Psi_0$ vanish, leading to:
$$
- \hbar \frac{\partial \theta}{\partial t} = \frac{1}{2m} \left[ \hbar^2 (\nabla \theta)^2 - 2 \hbar q \vec{A} \cdot \nabla \theta + q^2 \vec{A}^2 \right] + q \phi = \frac{q^2}{2m} \left( \frac{\hbar}{q} \nabla \theta - \vec{A} \right)^2 + q \phi $$
Now if we combine this with the expression for the macroscopic quantum current density in a uniform superconductor:
$$
\Lambda \vec{J_s} = \frac{\hbar}{q} \nabla \theta - \vec{A} $$
We can rewrite the equation as:
$$
- \hbar \frac{\partial}{\partial t} \theta (\vec{r}, t) = \frac{1}{2n_s} \Lambda J_s^2 (\vec{r}, t) + q \phi (\vec{r}, t) $$
This equation yields the relationship between the time evolution of the phase of the macroscopic wave function and the energy contributions from the supercurrent density and the electric potential(**energy-phase relationship**).
The first term on the right side represents the kinetic energy per superelectron associated with the supercurrent density $\vec{J_s}$, while the second term represents the potential energy per superelectron due to the electric potential $\phi$.
This relationship is crucial for understanding the dynamics of superconducting systems, as it connects the phase evolution of the macroscopic wave function to measurable quantities like current density and electric potential.
If we insert this relation into the time derivative of the macroscopic quantum current density, we obtain:
$$
\frac{\partial}{\partial t} (\Lambda \vec{J_s}) = \frac{\hbar}{q} \nabla \left( \frac{\partial \theta}{\partial t} \right) - \frac{\partial \vec{A}}{\partial t} = \frac{1}{2qn_s} \nabla ( \Lambda J_s^2 ) - \nabla \phi - \frac{\partial \vec{A}}{\partial t} $$
Time derivative and space gradient operators commute, meaning that the order in which we apply them does not matter. We can also see that the last two terms correspond to the electric field $\vec{E}$:
$$
\vec{E} = - \nabla \phi - \frac{\partial \vec{A}}{\partial t} $$
So we have:
$$
\frac{\partial}{\partial t} (\Lambda \vec{J_s}) = - \frac{1}{2qn_s} \nabla ( \Lambda J_s^2 ) - \vec{E} $$
Rearranging we obtain the response of a superconductor to an applied electric field:
$$
\frac{\partial}{\partial t} \vec{J_s} = \frac{\vec{E}(\vec{r}, t)}{\Lambda} - \frac{1}{2qn_s} \nabla J_s^2 (\vec{r}, t) $$
This is the **first London equation**, which describes not only the exponential increase of the supercurrent density $\vec{J_s}$ in response to an applied electric field $\vec{E}$ due to the absence of resistance, but also includes a term proportional to the gradient of the kinetic energy of the superelectrons. (This formula can be derived also from Lorentz's law combined with the second London equation).
So in the end MQM unites together both London equations, which give a classical description of superconductors, with quantum mechanics by introducing the macroscopic wave function $\Psi (\vec{r}, t)$. 
We are now going to show that MQM allows us to analyze superconducting phenomena without 





















##### Digression on difference between real and imaginary parts
The key behind this separation is that we can express the wave function in polar form $\Psi = \Psi_0 e^{i \theta}$, where $\Psi_0$ is the amplitude (real part) and $\theta$ is the phase (imaginary part). When we substitute this into the Schrödinger equation:
$$i\hbar \frac{\partial \Psi_0}{\partial t} - \hbar \Psi_0 \frac{\partial \theta}{\partial t} = \frac{1}{2m} \left[- \hbar^2 \left(\nabla^2 \Psi_0 + 2 i \nabla \theta \cdot \nabla \Psi_0 + i \Psi_0 \nabla^2 \theta - \Psi_0 (\nabla \theta)^2 \right) + 2i \hbar q \vec{A} \cdot \nabla \Psi_0 - 2 \hbar q \Psi_0 \vec{A} \cdot \nabla \theta + q^2 \vec{A}^2 \Psi_0 \right] + q \phi \Psi_0 $$
The effect of multiplying by $e^{i\theta}$ converts the derivatives of the wave function into real and imaginary components. 
The imaginary part gives a continuity equation leading to the conservation of probability(supercurrent density):
$$
\vec{J}_s (\vec{r}, t) = \frac{q \hbar}{m} n_s (\vec{r}, t) \left( \nabla \theta (\vec{r}, t) - \frac{q}{\hbar} \vec{A} (\vec{r}, t) \right) $$
This expression means that the current is generated by gradients of the phase of the wave function, the intuition is that changes in the phase correspond to changes in momentum, leading to a flow of particles(current). So a uniform phase means no flow, while a varying phase means particles are moving.
So basically the imaginary part encodes phase dynamics and current flow.
The real part gives an evolution equation for the amplitude $\Psi_0$, which relates to the energy of the system:





## References
