
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
We consider a structure that is confined in one dimension $z$, so that the Schrödinger equation will describe a potential $V(z)$ in that direction, while in the other two directions $x$ and $y$ the particle is free in a macroscopic region of size $L_x$ and $L_y$. 
$$\begin{cases} 
V(x,y) = 0 & 0 < x < L_x, \quad 0 < y < L_y \\
V(z) = \text{some confining potential} & 0 < z < L_z \\
\end{cases}$$
The Schrödinger equation will be:
$$-\frac{\hbar^2}{2m} \nabla^2 \psi(x,y,z) + V(z) \psi(x,y,z) = E \psi(x,y,z)$$ We can factorize the solutions:
$$\psi(x,y,z) = \theta(z) \cdot \varphi(x,y)$$ Thus we get:
$$-\frac{\hbar^2}{2m} \theta(z) \left( \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} \right) \varphi(x,y) - \frac{\hbar^2}{2m} \varphi(x,y) \frac{d^2}{dz^2} \theta(z) + V(z) \theta(z) \varphi(x,y) = E \theta(z) \varphi(x,y)$$ Dividing by $\theta(z) \varphi(x,y)$ we get:
$$-\frac{\hbar^2}{2m} \frac{1}{\varphi(x,y)} \left( \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} \right) \varphi(x,y) - \frac{\hbar^2}{2m} \frac{1}{\theta(z)} \frac{d^2}{dz^2} \theta(z) + V(z) = E$$ Since the left side depends on different variables, each term must be equal to a constant $E_{xy}$ and $E_z$ such that:
$$\begin{cases}
-\frac{\hbar^2}{2m} \frac{1}{\varphi(x,y)} \left( \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} \right) \varphi(x,y) = E_{xy} \\
-\frac{\hbar^2}{2m} \frac{1}{\theta(z)} \frac{d^2}{dz^2} \theta(z) + V(z) = E_z \\
E = E_{xy} + E_z
\end{cases} \quad \Rightarrow \quad \begin{cases}
-\frac{\hbar^2}{2m} \left( \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} \right) \varphi(x,y) = E_{xy} \varphi(x,y) \\
-\frac{\hbar^2}{2m} \frac{d^2}{dz^2} \theta(z) + V(z) \theta(z) = E_z \theta(z) \\
E = E_{xy} + E_z
\end{cases}$$ The first equation describes a free particle in two dimensions, while the second equation describes a particle in a potential well in one dimension.
The solutions for the free particle in 2D are plane waves:
$$\varphi(x,y) = \frac{1}{\sqrt{L_x L_y}} e^{i(k_x x + k_y y)}$$ with energy:
$$E_{xy} = \frac{\hbar^2}{2m} (k_x^2 + k_y^2)$$ The solutions must satisfy periodic boundary conditions:
$$\begin{cases}
\varphi(x + L_x, y) = \varphi(x,y) \\
\varphi(x, y + L_y) = \varphi(x,y)
\end{cases} \quad \Rightarrow \quad \begin{cases}
k_x = \frac{2 \pi n_x}{L_x}, \quad n_x \in \mathbb{Z} \\
k_y = \frac{2 \pi n_y}{L_y}, \quad n_y \in \mathbb{Z}
\end{cases}$$ Since $L_x$ and $L_y$ are macroscopic, the allowed values of $k_x$ and $k_y$ are very close together, and we can approximate them as continuous variables.

The second equation depends on the specific form of the potential $V(z)$. We can have for example a potential well with infinite barriers. In this case the potential is:
$$\begin{cases}
V(z) = 0 & -\frac{L_z}{2} < z < \frac{L_z}{2} \\
V(z) = \infty & \text{elsewhere}
\end{cases}$$ Where in this case $L_z$ is microscopic. Other well-known cases are the triangular well and the harmonic oscillator potential.
![[Pasted image 20251226145517.png]]

We can further analyze the case of a particle in a box, the Schrödinger equation inside the well is:
$$-\frac{\hbar^2}{2m} \frac{d^2}{dz^2} \theta(z) = E_z \theta(z)$$ The boundary conditions impose that the wavefunction must be continuous and go to zero at the edges of the well, so the solutions are:
$$\begin{cases}
\theta (z) = \sqrt{\frac{2}{L_z}} \sin\left( n_z \frac{\pi}{L_z} \cdot z\right) & n_z = \text{even} \\
\theta (z) = \sqrt{\frac{2}{L_z}} \cos\left( n_z \frac{\pi}{L_z} \cdot z\right) & n_z = \text{odd}
\end{cases}$$ with energy levels:
$$E_z = \frac{\hbar^2 n_z^2 }{8m L_z^2} \quad n_z = 1, 2, 3, ...$$ Where $n_z$ is the quantum number associated with the confinement in the $z$ direction. This time we can't say that the allowed values of $n_z$ are continuous, since $L_z$ is microscopic, so the energy levels are quantized.
![[Pasted image 20251226152145.png]]
The distance between energy levels increases for higher energy levels, since it goes as $n_z^2$. 
In the figure above we can see that for odd $n_z$ the wavefunction has a maximum at the center of the well, meaning it's more likely to find the particle there and it's an even function. For even $n_z$ the wavefunction has a node at the center of the well, meaning it's less likely to find the particle there and it's an odd function.
We can also see that for $n_z = 1$, the the wavefunction has no nodes inside the well, and the number of nodes increases with $n_z$, at a certain point we will have an infinite number of nodes resulting in a continuous energy spectrum, which is the case of a free particle.

Now we can combine both results to get the total energy of the particle in the quantum well:
$$E = E_{xy} + E_z = \frac{\hbar^2}{2m} (k_x^2 + k_y^2) + \frac{\hbar^2 n_z^2 }{8m L_z^2}$$ We can see that the energy spectrum consists of a series of paraboloids in the $k_x-k_y$ plane, each one corresponding to a different quantized energy level $E_z$ associated with the confinement in the $z$ direction. In fact to each value of $n_z$ corresponds infinite number of paraboloids shifted in energy by the quantized term.
![[Pasted image 20251226152858.png]]
The quantization of levels depends on the structure of the well:
- the harmonic oscillator potential gives evenly spaced levels
- the triangular well gives levels that get closer together at higher energies
- the infinite potential well gives levels that get further apart at higher energies

But the subband structure remains the paraboloids in the $k_x-k_y$ plane shifted in energy by the quantized term. So the only difference is the specific energy values of each subband and the distance between them.

If we look back at the total energy expression we see that each paraboloid is the same, so they all have the same density of states, what differs is the offset in energy given by the quantized term $\frac{\hbar^2 n_z^2 }{8m L_z^2}$.
So we can calculate the density of states for a single subband, putting the offset energy to zero.
##### Density of States in 2D
![[Pasted image 20251226160755.png]]
As we said before, we focus on a single subband with offset energy equal to zero, the density of states is defined as:
$$D(E) = \frac{1}{A} \frac{dN}{dE}$$ where $A = L_x L_y$ is the area of the system and $N$ is the number of states from 0 to a given energy $E$.
For a bulk 3D system, we calculated the number of states in the reciprocal space as points inside a sphere of radius $k$, but now we have a 2D system, so the states will be points inside a circle of radius $k$ in the $k_x-k_y$ plane.
![[Pasted image 20251226161847.png]]
As we said $k_x = \frac{2 \pi n_x}{L_x}$ and $k_y = \frac{2 \pi n_y}{L_y}$, so we calculate the area of the circle in the $n_x-n_y$ plane:



## References
