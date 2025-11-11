
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
$$\oint_C \Lambda \vec{J}_s(\vec{r}, t) \cdot d\vec{l} + \int_S \vec{B}(\vec{r}, t) \cdot d\vec{S} = n \Phi_0$$ where $\Phi_0 = \frac{2\pi \hbar}{|q|} = \frac{h}{q}$ is the magnetic flux quantum.


## References
