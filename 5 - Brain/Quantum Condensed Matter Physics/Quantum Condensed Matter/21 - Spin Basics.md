
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
$$\mu = \hbar m_l$$ Where $l$ is the azimuthal quantum 



## References
