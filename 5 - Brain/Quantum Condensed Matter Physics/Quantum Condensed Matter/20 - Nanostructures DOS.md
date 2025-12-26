
2025-12-23 19:28

Status: 

Tags:

# Nanostructures DOS
The size at which materials exhibit quantum mechanical properties can be estimated by considering that the Heisenberg uncertainty describes that if we confine a particle in a region of length $\Delta x$, the uncertainty in momentum $\Delta p$ is given by:
$$\Delta p_x \approx \frac{\hbar}{\Delta x}$$ If the confinement is restricted to the x direction, this will give rise to an additional kinetic energy term:
$$E_{conf} \approx \frac{(\Delta p_x)^2}{2m} \approx \frac{\hbar^2}{2m(\Delta x)^2}$$ where $m$ is the effective mass of the particle. We can easily see from the formula that when $\Delta x$ becomes large, the confinement energy becomes negligible. 
This energy, will then become relevant when it is comparable to the thermal energy at room temperature, $k_BT \approx 25meV$, because at this point the thermal fluctuations will not be able to mask the quantum confinement effects. By equating both energies, we can estimate the critical critical size $\Delta x$ at which quantum confinement effects become relevant:
$$E_{conf} \approx \frac{\hbar^2}{2m(\Delta x)^2} > \frac{1}{2}k_BT \quad \Rightarrow \quad \Delta x < \sqrt{\frac{\hbar^2}{m k_B T}}$$ For an electron in a semiconductor, we can use the effective mass $m^* = 0.1 m_e$, so at $T = 300K$, we get $\Delta x \approx 5nm$. 
Intuitively, when the confinement energy is greater than the kinetic energy given by thermal fluctuations, the particle will "feel" the boundaries of the region it is confined in, and quantum mechanical effects will become significant.
We can get the same results starting from the De Broglie wavelength of the particle:
$$\lambda = \frac{h}{p} = \frac{h}{\sqrt{2mE}}$$ If we consider the thermal energy at room temperature $E \approx k_B T$, we can estimate the wavelength of the particle:
$$\lambda \approx \frac{h}{\sqrt{mk_B T}}$$ When the size of the system becomes comparable to this wavelength, quantum confinement effects will become relevant, leading to discrete energy levels and altered electronic properties.
#### Quantum Wells - 2D Nanostructures
![[Pasted image 20251226143039.png]]




## References
