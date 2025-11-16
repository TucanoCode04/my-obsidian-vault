
2025-11-15 20:05

Status: 

Tags:

# SQUIDs
The Superconducting Quantum Interference Device (SQUID) is a highly sensitive magnetometer used to measure extremely subtle magnetic fields. It operates based on parallel Josephson junctions arranged in a superconducting loop. 
We consider a SQUID consisting of two identical basic lumped Josephson junctions:
$$i = i_1 + i_2 = I_c \sin(\psi_1) + I_c \sin(\psi_2)$$
where $I_c$ is the critical current of each junction, and $\psi_1$ and $\psi_2$ are the phase differences across the two junctions.
By simple trigonometry, we can rewrite the total current as:
$$i = 2 I_c \cos\left(\frac{\psi_1 - \psi_2}{2}\right) \sin\left(\frac{\psi_1 + \psi_2}{2}\right)$$
The difference in the gauge-invariant phases can be obtained from the line integral of the phase gradient around the contour $C$ enclosing the SQUID loop:
$$\oint_C \nabla \theta(\vec{r}, t) \cdot d\vec{l} = 2\pi n= (\theta_b - \theta_a) + (\theta_c - \theta_b) + (\theta_d - \theta_c) + (\theta_a - \theta_d)$$
We can divide this terms into the contributions from the two junctions and the two superconducting leads:
![[Pasted image 20251116144005.png]]
$$\begin{cases}
(\theta_b - \theta_a) \quad \text{(junction 1, red)} \\
(\theta_c - \theta_b) \quad \text{(lead 1, green)} \\
(\theta_d - \theta_c) \quad \text{(junction 2, red)} \\
(\theta_a - \theta_d) \quad \text{(lead 2, green)}
\end{cases}$$
To describe the figure:
- the magnetic field $\vec{B}$ is applied perpendicular to the SQUID loop so it's pointing out of the page
- the green arrows represent(the direction) the fact that we can just calculate the phase difference across the superconducting leads using the difference in phase of the superconducting wavefunction at the endpoints(near the junctions) since the phase gradient in the leads is negligible
- the red arrows represent the direction of the phase difference across the Josephson junctions
- the red dotted lines represents the leads of the loop where we are going to do the line integral to calculate the phase differences across the leads
We don't count the $\lambda$ surface currents, neglecting the screening effects.
The phase differences across the Josephson junctions are obtained from the gauge-invariant phase difference formula:
$$\psi(y, z, t) = \theta_1(y, z, t) - \theta_2(y, z, t) - \frac{2\pi}{\Phi_0} \int_{1}^{2} \vec{A}(\vec{r}, t) \cdot d\vec{l}$$
where $\theta_1$ and $\theta_2$ are the phases of the superconducting wavefunctions on either side of the junction, $\vec{A}$ is the vector potential, and $\Phi_0$ is the magnetic flux quantum.
In the case of the SQUID loop, we have 2 junctions, which will follow the equation above.
$$\psi_1 = \theta_a - \theta_b - \frac{2\pi}{\Phi_0} \int_{a}^{b} \vec{A}(\vec{r}, t) \cdot d\vec{l}$$
$$\psi_2 = \theta_c - \theta_d - \frac{2\pi}{\Phi_0} \int_{c}^{d} \vec{A}(\vec{r}, t) \cdot d\vec{l}$$
The 2 junctions are connected through superconducting leads, the phase differences across the leads are found by the line integral of the supercurrent density equation:
$$\vec{J}_s(\vec{r}, t) = - \frac{1}{\Lambda} \left( \vec{A}(\vec{r}, t) + \frac{\Phi_0}{2\pi} \nabla \theta(\vec{r}, t) \right)$$
Integrating along the leads, we have:
$$\int_{b}^{c} \vec{J}_s(\vec{r}, t) \cdot d\vec{l} = - \frac{1}{\Lambda} \left( \int_{b}^{c} \vec{A}(\vec{r}, t) \cdot d\vec{l} + \frac{\Phi_0}{2\pi} \int_{b}^{c} \nabla \theta(\vec{r}, t) \cdot d\vec{l} \right)$$
So we find:
$$\theta_c - \theta_b = - \frac{2\pi}{\Phi_0} \left( \int_{b}^{c} \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} + \int_{b}^{c} \vec{A}(\vec{r}, t) \cdot d\vec{l} \right)$$
Similarly, for the other lead:
$$\theta_a - \theta_d = - \frac{2\pi}{\Phi_0} \left( \int_{d}^{a} \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} + \int_{d}^{a} \vec{A}(\vec{r}, t) \cdot d\vec{l} \right)$$
The total gauge-invariant phase difference around the loop is then:
$$\oint_C \nabla \theta \cdot d\vec{l} = (\theta_b - \theta_a) + (\theta_c - \theta_b) + (\theta_d - \theta_c) + (\theta_a - \theta_d)$$
$$ = \left( - \psi_1 - \frac{2\pi}{\Phi_0} \int_{a}^{b} \vec{A} \cdot d\vec{l} \right) + \left( - \frac{2\pi}{\Phi_0} \int_{b}^{c} \Lambda \vec{J}_s \cdot d\vec{l} - \frac{2\pi}{\Phi_0} \int_{b}^{c} \vec{A} \cdot d\vec{l} \right) + \left( + \psi_2 - \frac{2\pi}{\Phi_0} \int_{c}^{d} \vec{A} \cdot d\vec{l} \right) + \left( - \frac{2\pi}{\Phi_0} \int_{d}^{a} \Lambda \vec{J}_s \cdot d\vec{l} - \frac{2\pi}{\Phi_0} \int_{d}^{a} \vec{A} \cdot d\vec{l} \right)$$
Rearranging:
$$2\pi n = \psi_2 - \psi_1 - \frac{2\pi}{\Phi_0} \oint_C \vec{A} \cdot d\vec{l} - \frac{2\pi}{\Phi_0} \int_{b}^{c} \Lambda \vec{J}_s \cdot d\vec{l} - \frac{2\pi}{\Phi_0} \int_{d}^{a} \Lambda \vec{J}_s \cdot d\vec{l}$$
If we have thick enough superconducting leads, thus we neglect the surface current, we can say that the supercurrent density in the two lead is symmetric, so the two integrals cancel out. Solving for the phase difference between the two junctions and remembering that the line integral of the vector potential around a closed loop is equal to the magnetic flux through the loop, we have:
$$\psi_2 - \psi_1 = 2\pi n + \frac{2\pi}{\Phi_0} \Phi = 2\pi \left( n + \frac{\Phi}{\Phi_0} \right)$$


## References
