
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





## References
