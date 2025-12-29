
2025-12-28 16:02

Status: 

Tags:

# 21 - Spin Basics
#### Angular Momentum
The angular momentum of a particle is a measure of its rotational motion. It is a vector quantity, meaning it has both magnitude and direction. The angular momentum $\vec{L}$ of a particle is given by the cross product of its position vector $\vec{r}$ and its linear momentum $\vec{p}$:
$$\vec{L} = \vec{r} \times \vec{p}$$
We can divide angular momentum per components:
$$L_x = y p_z - z p_y$$
$$L_y = z p_x - x p_z$$
$$L_z = x p_y - y p_x$$
We can also express angular momentum in terms of operators in quantum mechanics:
$$\hat{L}_x = \frac{\hbar}{i} \left( y \frac{\partial}{\partial z} - z \frac{\partial}{\partial y} \right)$$
$$\hat{L}_y = \frac{\hbar}{i} \left( z \frac{\partial}{\partial x} - x \frac{\partial}{\partial z} \right)$$
$$\hat{L}_z = \frac{\hbar}{i} \left( x \frac{\partial}{\partial y} - y \frac{\partial}{\partial x} \right)$$
These operator don't commute with each other, so they cannot be simultaneously measured with arbitrary precision. The commutation relations are given by:
$$[\hat{L}_x, \hat{L}_y] = i \hbar \hat{L}_z$$
$$[\hat{L}_y, \hat{L}_z] = i \hbar \hat{L}_x$$
$$[\hat{L}_z, \hat{L}_x] = i \hbar \hat{L}_y$$
The squared angular momentum operator is instead used, the concept behind it is that we can measure the total angular momentum and one of its components simultaneously. The squared angular momentum operator is defined as:
$$\hat{L}^2 = \hat{L}_x^2 + \hat{L}_y^2 + \hat{L}_z^2$$
It commutes with each component of the angular momentum:
$$[\hat{L}^2, \hat{L}_x] = 0$$
$$[\hat{L}^2, \hat{L}_y] = 0$$
$$[\hat{L}^2, \hat{L}_z] = 0$$
And they also commute with the Hamiltonian operator $\hat{H}$ of a spherically symmetric system.

We look at the solutions of the eigenvalue equations for $\hat{L}^2$ and $\hat{L}_z$:
$$\hat{L}^2 f = \lambda f$$
$$\hat{L}_z f = \mu f$$
The eigenvalues are given by:
$$\lambda = \hbar^2 l (l + 1)$$
$$\mu = \hbar m_l$$ Where $l$ is the azimuthal quantum number (non-negative integer) ranging from $0$ to $n-1$ and $m_l$ is the magnetic quantum number (integer) ranging from $-l$ to $+l$. $n$ is the principal quantum number.
So these values are quantized, meaning they can only take specific discrete values.
The function $f$ depends on the two quantum numbers $l$ and $m_l$ and is called the spherical harmonic function $Y_{l}^{m_l}(\theta, \phi)$, where $\theta$ and $\phi$ are the polar and azimuthal angles in spherical coordinates.

From here we can derive the orbital angular momentum of an electron in an atom, which is quantized and can take only specific discrete values determined by the quantum numbers $l$ and $m_l$.
![[Pasted image 20251228175041.png]]
Basically the quantum number $n$ determines the energy level of the electron, where higher $n$ means higher energy. The quantum number $l$ determines the shape of the orbital, with higher $l$ values corresponding to more complex shapes. The quantum number $m_l$ determines the orientation of the orbital in space.
We can analyze for example the case of $n=3$, which means the electron is in the third energy level. The possible values of $l$ are $0$, $1$, and $2$, as shown in the picture above. We focus on the case where $l=2$, which corresponds to the "d" orbitals. For $l=2$, the possible values of $m_l$ are $-2$, $-1$, $0$, $+1$, and $+2$. Each of these values corresponds to a different orientation of the "d" orbital in space, as shown in the picture above.
$$L^2 = \hbar^2 l (l + 1) = \hbar^2 2 (2 + 1) = 6 \hbar^2$$
$$L_z = \hbar m_l \quad \Rightarrow \begin{cases} L_z = -2 \hbar \\ L_z = -1 \hbar \\ L_z = 0 \\ L_z = +1 \hbar \\ L_z = +2 \hbar \end{cases}$$
These values of $L_z$ show the quantization of the angular momentum states along the z-axis for an electron in a "d" orbital.
![[Pasted image 20251228181025.png]]
#### Spin
Spin is an intrinsic rotation of particles on themselves, classically we can think of it as a particle spinning around its own axis, and it's described by:
$$\vec{S} = I \vec{\omega}$$
Where $I$ is the moment of inertia and $\vec{\omega}$ is the angular velocity. However, in quantum mechanics, spin is not due to any physical rotation of the particle, but rather a fundamental property of particles and it shares some similarities with angular momentum.
Spin is quantized, meaning it can only take specific discrete values. The spin quantum number $s$ determines the magnitude of the spin angular momentum, while the spin magnetic quantum number $m_s$ determines the orientation of the spin angular momentum along a chosen axis (usually the z-axis).
$$\hat{S}^2 \chi = \hbar^2 s (s + 1) \chi$$
$$\hat{S}_z \chi = \hbar m_s \chi$$ Where $\chi = |s, m_s \rangle$ is the spin wavefunction. It shares the same commutation relations as angular momentum:
$$[\hat{S}_x, \hat{S}_y] = i \hbar \hat{S}_z$$
$$[\hat{S}_y, \hat{S}_z] = i \hbar \hat{S}_x$$
$$[\hat{S}_z, \hat{S}_x] = i \hbar \hat{S}_y$$
The main difference between spin and angular momentum is that the spin quantum number $s$ can take half-integer values (e.g., $1/2$, $3/2$, etc.) in addition to integer values (e.g., $0$, $1$, $2$, etc.). For example, electrons, protons, and neutrons all have a spin quantum number of $s = 1/2$, resulting in two possible spin states: "spin-up" ($m_s = +1/2$) and "spin-down" ($m_s = -1/2$).
So for the system $|\frac{1}{2}, m_s \rangle$ we have:
$$|\frac{1}{2}, +\frac{1}{2} \rangle = |\uparrow \rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$$
$$|\frac{1}{2}, -\frac{1}{2} \rangle = |\downarrow \rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$$
So that:
$$S^2 |\uparrow \rangle = \hbar^2 \frac{1}{2} \left( \frac{1}{2} + 1 \right) |\uparrow \rangle = \frac{3}{4} \hbar^2 |\uparrow \rangle$$
$$S^2 |\downarrow \rangle = \hbar^2 \frac{1}{2} \left( \frac{1}{2} + 1 \right) |\downarrow \rangle = \frac{3}{4} \hbar^2 |\downarrow \rangle$$
$$S_z |\uparrow \rangle = \hbar \left( +\frac{1}{2} \right) |\uparrow \rangle = +\frac{\hbar}{2} |\uparrow \rangle$$
$$S_z |\downarrow \rangle = \hbar \left( -\frac{1}{2} \right) |\downarrow \rangle = -\frac{\hbar}{2} |\downarrow \rangle$$
A generic state, called a spinor, can be expressed as a linear combination of the two basis states:
$$|\chi \rangle = a |\uparrow \rangle + b |\downarrow \rangle = \begin{pmatrix} a \\ b \end{pmatrix}$$
Where $a$ and $b$ are complex coefficients satisfying the normalization condition:
$$|a|^2 + |b|^2 = 1$$
Example for $\hat{S}^2$ operator:
$$\hat{S}^2 = \begin{pmatrix} \langle \uparrow | \hat{S}^2 | \uparrow \rangle & \langle \uparrow | \hat{S}^2 | \downarrow \rangle \\ \langle \downarrow | \hat{S}^2 | \uparrow \rangle & \langle \downarrow | \hat{S}^2 | \downarrow \rangle \end{pmatrix} = \begin{pmatrix} \frac{3}{4} \hbar^2 & 0 \\ 0 & \frac{3}{4} \hbar^2 \end{pmatrix} = \frac{3}{4} \hbar^2 I$$
Where $I$ is the identity matrix.
Likewise for the other operators:
$$\hat{S}_x = \frac{\hbar}{2} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$$
$$\hat{S}_y = \frac{\hbar}{2} \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}$$
$$\hat{S}_z = \frac{\hbar}{2} \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$
Where the matrices above are known as the Pauli matrices, which are fundamental in describing spin-1/2 particles in quantum mechanics. So that:
$$\hat{S}_x = \frac{\hbar}{2} \sigma_x$$
$$\hat{S}_y = \frac{\hbar}{2} \sigma_y$$
$$\hat{S}_z = \frac{\hbar}{2} \sigma_z$$
Where $\sigma_x$, $\sigma_y$, and $\sigma_z$ are the Pauli matrices.
##### Particle in a magnetic field
A spin-1/2 particle, such as an electron, possesses a magnetic moment $\vec{\mu}$ due to its spin. 
Classically this is:$$\vec{\mu}_s= \gamma \vec{S}$$ Where $\gamma$ is the gyromagnetic ratio. 
For electrons the gyromagnetic ratio is given by:
$$\gamma = -g_e e \frac{\mu_B}{\hbar}$$ Where $g_e \approx 2.002319$ is the electron g-factor and $\mu_B = \frac{e \hbar}{2 m_e}$ is the Bohr magneton, which represents the natural unit of the magnetic moment for an electron.
In quantum mechanics, the magnetic moment operator $\hat{\mu}$ is related to the spin operator $\hat{S}$ by:
$$\hat{\mu}_s = -g_e e \frac{\mu_B}{\hbar} \hat{S} = -\frac{e}{m} \hat{S}$$
![[Pasted image 20251229164141.png]]
If we place the spin-1/2 particle in a uniform magnetic field $\vec{B}$, the classical potential energy that arises from the interaction between the magnetic moment and the magnetic field is given by:S$$E = -\vec{\mu} \cdot \vec{B} = - |\vec{\mu}| |\vec{B}| \cos \theta$$ Where $\theta$ is the angle between the magnetic moment and the magnetic field, meaning that if they are aligned ($\theta = 0$), the energy is minimized, while if they are anti-aligned ($\theta = \pi$), the energy is maximized.
![[Pasted image 20251229164602.png]]
In quantum mechanics, this interaction is described by the Hamiltonian operator $\hat{H}$:
$$\hat{H} = -\hat{\mu}_s \cdot \vec{B} = \frac{e}{m} \hat{S} \cdot \vec{B}$$
The latter part is for the case of an electron. 

Assuming that the magnetic field is oriented along the z-axis:
$$\hat{H} = \frac{e B_z}{m} \hat{S}_z$$
We know that the two operators $\hat{H}$ and $\hat{S}_z$ commute, so the solutions are the same as before:
$$\hat{S}_z \chi = \hbar m_s \chi$$
So we can easily find the energy eigenvalues to be:
$$\begin{cases} |\downarrow \rangle : E_{\downarrow} = \frac{e B_z}{m} \left( -\frac{\hbar}{2} \right) \\ |\uparrow \rangle : E_{\uparrow} = \frac{e B_z}{m} \left( +\frac{\hbar}{2} \right) \end{cases}$$
So the energy contributions due to the interaction between the magnetic moment and the magnetic field are quantized, and they depend on the orientation of the spin relative to the magnetic field, resulting in two distinct energy levels for the spin-1/2 particle in the magnetic field.
Basically we observe the Zeeman effect, which is the splitting of energy levels in the presence of a magnetic field.
![[Pasted image 20251229165606.png]]
For $B_z = 0$ the two energy levels are degenerate, meaning they have the same energy. When we apply a magnetic field ($B_z > 0$), the degeneracy is lifted, and the energy levels split into two distinct levels corresponding to the spin-up and spin-down states.
#### Wavefunction of two identical spin-1/2 particles 
The wavefunction of a system of two identical 



## References
