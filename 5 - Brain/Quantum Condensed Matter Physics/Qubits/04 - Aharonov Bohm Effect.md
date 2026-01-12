
2026-01-12 16:44

Status: 

Tags:

# 04 - Aharonov Bohm Effect
The Aharonov Bohm Effect is a quantum mechanical phenomenon that demonstrates how the vector potential affects the transmittance of electrons even in regions where the magnetic field is zero. Basically, it shows that the potentials in quantum mechanics have physical significance, unlike in classical mechanics where only fields matter.
Let's suppose we have a solenoid that generates a magnetic field confined within a loop, but in the ring arms the magnetic field is zero. We need to find an $A$ vector potential suitable for this configuration.
![[Pasted image 20260112173657.png]]
We notice that any close line of $A$ that includes the solenoid span an area that contains the entire magnetic flux $\Phi_M$. 
$$\int_{\Sigma} \vec{B} \cdot d\vec{S} = \int_{\Sigma} (\nabla \times \vec{A}) \cdot d\vec{S} = \Phi_M$$
Therefore, by applying Stokes' theorem, we have:
$$\oint A \cdot d\vec{l} = \int_{\Sigma} (\nabla \times \vec{A}) \cdot d\vec{S} = \Phi_M$$
So any $A$ we choose that exists on the arms of the ring must be non zero (where we need to calculate Schrödinger's equation).
We use Coulomb gauge, so $\nabla \cdot A = 0$. 
Assuming a solenoid generating a uniform magnetic field $B$ inside, we can find $A$ in cylindrical coordinates:
$$\begin{cases}
2 \pi r A(r) = \pi r^2 B \Rightarrow A(r) = \frac{B r}{2} & r < a \\
2 \pi r A(r) = \pi a^2 B \Rightarrow A(r) = \frac{B a^2}{2 r} & r > a
\end{cases}$$
Where $a$ is the radius of the solenoid.
![[Pasted image 20260112174833.png]]
If we plot $A(r)$, we see that electron moving outside the solenoid (where $B=0$) still experiences a non-zero vector potential $A$.
![[Pasted image 20260112175013.png]]
We start from the general Schrödinger equation with a vector potential:
$$\left[ \frac{1}{2m} \left[ \hat{p} - q \vec{A}(\vec{r},t) + q \phi(\vec{r},t) \right]^2 \right] \psi(\vec{r},t) = i \hbar \frac{\partial}{\partial t} \psi(\vec{r},t)$$
In our case, we have a static situation with $\phi = 0$. It is possible to simplify the equation by transforming the wavefunction(instead of substituting $A$ directly):
$$\psi = e^{i g} \psi', \quad \text{with} \quad g(\vec{r}) = \frac{q}{\hbar} \int_{\vec{r}_0}^{\vec{r}} \vec{A}(\vec{r}') \cdot d\vec{r}'$$
![[Pasted image 20260112175436.png]]
By knowing:
$$\nabla \psi = e^{i g} \left( i \nabla g \psi' + \nabla \psi' \right)$$
And:
$$\nabla g = \frac{q}{\hbar} \vec{A}$$
We can substitute in the kinetic term:
$$\left( \hat{p} - q \vec{A} \right) \psi = \left( \frac{\hbar}{i} \nabla - q \vec{A} \right) \psi = -i \hbar e^{i g} \nabla \psi'$$
In the Schrödinger equation the term is squared, so we have:
$$\left( \hat{p} - q \vec{A} \right)^2 \psi = - \hbar^2 e^{i g} \nabla^2 \psi'$$
Finally, substituting back in the Schrödinger equation:
$$-\frac{\hbar^2}{2m} \nabla^2 \psi' = i \hbar \frac{\partial}{\partial t} \psi'$$
With:
$$\psi(\vec{r}, t) = \psi'(\vec{r}, t) e^{i \frac{q}{\hbar} \int_{\vec{r}_0}^{\vec{r}} \vec{A}(\vec{r}') \cdot d\vec{r}'}$$
We see that $\psi'$ satisfies the free particle Schrödinger equation. Therefore, the effect of the vector potential is to introduce a phase factor in the wavefunction.
Since $A$ and $B$ do not depend on time, we can use the time independent Schrödinger equation:
$$-\frac{\hbar^2}{2m} \nabla^2 \psi' = E \psi'$$
We recognize that the total phase of a wavefunction is given by:$$\psi (\vec{r}) = |\psi'(\vec{r})| e^{i \phi^{(0)}(\vec{r})} e^{i \frac{q}{\hbar} \int_{\vec{r}_0}^{\vec{r}} \vec{A}(\vec{r}') \cdot d\vec{r}'}$$ Where $\phi^{(0)}$ is the phase in the absence of the vector potential.

We treat the ring as a barrier problem with propagating, reflected and transmitted waves. 
## References
