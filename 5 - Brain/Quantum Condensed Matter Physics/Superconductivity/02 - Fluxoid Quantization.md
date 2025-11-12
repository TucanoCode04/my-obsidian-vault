
2025-11-11 13:32

Status: 

Tags:

# Fluxoid Quantization
Fluxoid quantization requires a full quantum mechanical treatment of the superconducting state. 
If we consider the supercurrent of a homogeneous(so that the density of Cooper pairs $n_s$ is constant) isotropic(the effective mass of Cooper pairs $m^*$ is a scalar, and not a tensor since in each direction the effective mass is the same) superconductor, then the supercurrent density $\mathbf{J}_s$ is given by:
$$\Lambda \vec{J}_s = \frac{\hbar}{q} \nabla\theta - \vec{A}$$
where $\Lambda = m^*/(n_s q^2)$ is the London parameter, $\phi$ is the phase of the macroscopic wavefunction describing the superconducting state, $\vec{A}$ is the magnetic vector potential, and $q$ is the charge of a Cooper pair($q = -2e$).
We want to see what happens when we integrate this equation around a closed path $C$ that encloses a surface $S$:
$$\oint_C \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} = \frac{\hbar}{q} \oint_C \nabla\theta(\vec{r}, t) \cdot d\vec{l} - \oint_C \vec{A}(\vec{r}, t) \cdot d\vec{l}$$
Using Stokes' theorem, we can convert the line integral of the vector potential into a surface integral of the magnetic field $\vec{B}$:
$$\oint_C \vec{A}(\vec{r}, t) \cdot d\vec{l} = \int_S (\nabla \times \vec{A}(\vec{r}, t)) \cdot d\vec{S} = \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} $$
We can now link the integral of the phase gradient to that of the supercurrent density and the magnetic flux across the surface:
$$\oint_C \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} + \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} = \frac{\hbar}{q} \oint_C \nabla\theta(\vec{r}, t) \cdot d\vec{l}$$
The line integral of the gradient of any scalar function is the difference between the same function evaluated at the endpoints of the path. Since our path is closed, the endpoints are the same, and thus the line integral must be zero unless the function is multivalued. The phase of a wavefunction is multivalued, since adding any integer multiple of $2\pi$ to the phase results in the same physical state. Therefore, we can write:
$$\theta(\vec{r}, t) = \theta(\vec{r}, t) + 2\pi n, \quad n \in \mathbb{Z} \quad \Rightarrow \quad \frac{\hbar}{q} \oint_C \nabla\theta(\vec{r}, t)\cdot d\vec{l} = \Delta \theta = 2\pi n $$
The presence of $n$ indicates that the phase can wind around the closed path multiple times, meaning that the fluxoid is quantized. 
The wavefunction is coherent over the entire superconductor(meaning that it is unique and described by the same phase in any point), so $n$ must be the same for any closed path within the superconductor.
Therefore, we can rewrite the previous equation as:
$$\oint_C \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} + \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} = n \Phi_0$$ where $\Phi_0 = \frac{2\pi \hbar}{|q|} = \frac{h}{q}$ is the magnetic flux quantum. The first part of the left-hand side is called the supercurrent contribution to the fluxoid, while the second part is the magnetic flux through the surface. The sum of these two contributions is called the fluxoid $\Phi_f$ and is quantized in units of the flux quantum. By flux quantum we mean the smallest possible unit of magnetic flux that can exist in a superconductor, meaning that the fluxoid can only take on magnetic flux values that are integer multiples of this fundamental unit.

**Summary:** Imagine we have a superconducting ring. Inside the superconductor the electrons form a single quantum state described by a macroscopic wavefunction with a well-defined phase. When we consider a closed loop around the ring, the phase of the wavefunction must return to its original value after going around the loop, like the ends of a circle must meet smoothly. However, since the phase is defined modulo $2\pi$, it can change by integer multiples of $2\pi$ as we go around the loop.  This leads to the quantization of the fluxoid, which is the sum of the magnetic flux through the ring and a term related to the supercurrent circulating around the ring. The total fluxoid must equal an integer multiple of the flux quantum $\Phi_0 = h/2e$. This means that only certain discrete values of magnetic flux can exist in the superconducting ring, leading to phenomena such as quantized magnetic flux vortices in type-II superconductors. So the magnetic flux, basically influences the phase of the superconducting wavefunction, that will compensate to ensure the total fluxoid remains quantized, and the requirement for the phase to be single-valued around a closed loop leads to the quantization of the fluxoid.

The equation holds for any shape of the closed contour $C$. If $C$ is simply-connected(like a circle), the contour can be continuously shrunk to a point without leaving the superconductor, and thus $n$, since the superconductor is coherent over its entire volume, must be zero. 
$$\begin{cases}
\oint_C \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} = 0 \\
\int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} = 0
\end{cases} \quad \Rightarrow \quad n = 0$$
Since the line integral of the supercurrent density is zero, the magnetic flux through any simply-connected surface within the superconductor must also be zero. This is consistent with the Meissner effect, which states that magnetic fields are expelled from the interior of a superconductor.
If $C$ is multiply-connected(like a ring), the contour cannot be shrunk to a point without breaking the superconductor, and thus $n$ can't be zero.
The total amount of flux(both generated by external fields and internal induced supercurrents) that can pass through the superconductor is quantized in integer multiples of the flux quantum $\Phi_0$.

The flux quantization principle can be easily demonstrated by flux trapping experiments, we consider an hollow superconducting cylinder. 
We consider it to have thick walls, so that we neglect the surface effects and the penetration of magnetic fields into the superconductor($t \gg \lambda$).
We apply the integral form of Faraday's law of induction around a closed path $C$ that lies within the walls of the superconductor:
$$\oint_C \vec{E}(\vec{r}, t) \cdot d\vec{l} = - \frac{d}{dt} \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} \quad \Rightarrow \quad \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} = \text{constant}$$
This is true because the electric field $\vec{E}$ inside a superconductor is zero since we don't have any resistive losses, so the line integral of $\vec{E}$ around any closed path within the superconductor must also be zero. 
![[Pasted image 20251112172817.png]]
Shielding currents may flow in the walls of the superconductor, either the inner or outer surface, to ensure that the magnetic field inside the superconductor remains zero. 
![[Pasted image 20251112172938.png]]
1. We start with the cylinder above the critical temperature $T_c$ so that it is in the normal state. We apply an external magnetic field $\vec{H_{app}}$, which will uniformly penetrate the cylinder and the hollow core.
2. We cool down the cylinder below $T_c$ while keeping the external magnetic field constant. As the cylinder becomes superconducting, an outer wall current is induced, due to Meissner effect, to expel the magnetic field from the superconductor. To maintain the flux constant inside the hollow core, an inner wall inner wall current is is induced to keep the magnetic field inside the hollow core unchanged. This effects occurs because Faraday's law requires that any change in magnetic flux through a surface induces an electric field that opposes that change. But since in the superconductor no electric field can exist, the superconductor responds adjusting the phase of its wavefunction, inducing inducing supercurrents that maintain the magnetic flux inside the hollow core constant.
3. We turn off the external magnetic field $\vec{H_{app}} = 0$. The outer wall current will disappear since there is no external magnetic field to expel, but the inner wall current will persist to maintain the magnetic flux inside the hollow core constant.
Since there are no losses in the superconductor, the inner wall current will persist indefinitely and the magnetic flux trapped inside the hollow core will remain constant.

Int he classical model any amount of magnetic flux could be trapped inside the hollow core. However, experimentally it is observed that the trapped magnetic flux is quantized in integer multiples of the flux quantum $\Phi_0$. This is a direct consequence of the fluxoid quantization principle. If we evaluate the fluxoid quantization equation around a closed path $C$ that lies within the walls of the superconductor where $\vec{J}_s \approx 0$ because we are inside the bulk with thick walls, we get:
$$\oint_C \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} + \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} = n \Phi_0 \quad \Rightarrow \quad \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} = n \Phi_0 $$
This shows that the magnetic flux trapped inside the hollow core of the superconducting cylinder must be quantized in integer multiples of the flux quantum $\Phi_0$.

An experiment from 1961 by Deaver and Fairbank provided direct evidence of flux quantization in superconducting rings. They measured the magnetic flux trapped in a superconducting ring cooled below its critical temperature in the presence of an external magnetic field. They observed that the trapped flux was quantized in units of $\Phi_0 = \frac{h}{2e}$, confirming the theoretical predictions of fluxoid quantization. 
This was also the first experimental evidence that the charge carriers in a superconductor are Cooper pairs with charge $2e$. 
![[Pasted image 20251112175607.png]]
In the imagine we can appreciate the quantization of the magnetic flux trapped in the hollow core in function of the applied magnetic field before cooling the superconductor. As we increase the applied magnetic field, the trapped flux increases in discrete steps of size $\Phi_0$.
## References
