
2026-01-13 11:46

Status: 

Tags:

# 03 - Quantum Hall Effect
##### Charge in a Uniform Magnetic Field (Classical Treatment)
We consider a uniform magnetic field along $\hat{z}$ direction. We consider a charge $-q$ moving in the $x$-$y$ plane with velocity $\vec{v}$. The Lorentz force acting on the charge is given by:
$$\vec{F_{or}} = q(\vec{F} + \vec{v} \times \vec{B})$$
where $\vec{F}$ is the electric field and $\vec{B}$ is the magnetic field. We consider the electric field to be zero, i.e., $\vec{F} = 0$, since there are no other charges present. The electron will move in a circular path int he plane perpendicular to the magnetic field at constant angular frequency.
![[Pasted image 20260113155909.png]]
The Lorentz force can also be written as:
$$\vec{F_{or}} = m \frac{\vec{v}^2}{r} $$
where $m$ is the mass of the charge and $r$ is the radius of the circular path. Equating the two expressions for the Lorentz force, we have:
$$ e vB = m \frac{v^2}{r} $$
We can also express the velocity in terms of angular frequency $\omega_C$ as:
$$ v = r_C \omega_C $$
Substituting this in the above equation, we have:
$$ eB = m \omega_C $$
Thus, the angular frequency of the circular motion of the charge in a magnetic field is given by:
$$ \omega_C = \frac{eB}{m} $$
This is also known as the cyclotron frequency. Again from the expression for velocity, we can express the radius of the circular path as:
	$$R_C= \frac{v}{\omega_C} = \frac{\sqrt{2mE}}{eB} $$
where $E=\frac{1}{2}mv^2$ is the kinetic energy of the charge, and we have that $E \propto r_C^2$. This radius is also known as the cyclotron radius. We see that the radius is dependent on the square root of the energy, similar to the case of a classical harmonic oscillator. In fact if we focus on 1D we can see that the motion of the charge in a magnetic field is equivalent to a harmonic oscillator.
![[Pasted image 20260113161412.png]]

##### Quantum Treatment of Charge in a Magnetic Field
We can see the system as a 2DEG in the $x$-$y$ plane with a uniform magnetic field along the $\hat{z}$ direction, where the electrons are confined. So in the $z$ direction the density of states presents a lot of paraboloidal subbands.
The general Schrödinger equation for a charged particle in a magnetic field is given by:
$$ \left[ \frac{1}{2m} (\vec{p} - q\vec{A(\vec{R},t))})^2 + q\phi(\vec{R},t) \right] \psi(\vec{R},t) = i\hbar \frac{\partial}{\partial t} \psi(\vec{R},t) $$
where $\vec{A}$ is the vector potential and $\phi$ is the scalar potential. We consider the scalar potential to be zero, i.e., $\phi = 0$. We choose the Landau gauge for the vector potential, which is given by:
$$ \vec{A} = (0, Bx, 0) = B_x \hat{u}_y $$
By changing gauges we would find other wavefunctions but the physical observables would remain the same. We first need to prove that our choice of vector potential gives us the correct magnetic field. 
$$ \vec{B} = \nabla \times \vec{A} = \begin{vmatrix} \hat{u}_x & \hat{u}_y & \hat{u}_z \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ 0 & Bx & 0 \end{vmatrix} = B \hat{u}_z $$
Since $\vec{A}$ does not depend on time, we can write the time-independent Schrödinger equation as:
$$ \left[ \frac{1}{2m} (\vec{p} - q\vec{A(\vec{R})})^2 + V(z) \right] \psi(\vec{R}) = E \psi(\vec{R}) $$
where $V(z)$ is the confining potential in the $z$ direction, we substituted this potential to account for the 2DEG. We can express the momentum operator as:
$$ \vec{p} = -i\hbar \nabla = -i\hbar \left( \frac{\partial}{\partial x} \hat{u}_x + \frac{\partial}{\partial y} \hat{u}_y + \frac{\partial}{\partial z} \hat{u}_z \right) $$
Substituting the expressions for $\vec{p}$ and $\vec{A}$ in the Schrödinger equation, we have:
$$ \left[ \frac{1}{2m} \left( -\hbar^2 \frac{\partial^2}{\partial x^2} \hat{u}_x + (-i\hbar \frac{\partial}{\partial y} - eBx)^2 \hat{u}_y - \hbar^2 \frac{\partial^2}{\partial z^2} \hat{u}_z \right) + V(z) \right] \psi(\vec{R}) = E \psi(\vec{R}) $$
By doing some algebraic manipulation, we can rewrite the equation as:
$$ \left[ -\frac{\hbar^2}{2m} \nabla^2 - \frac{ie\hbar Bx}{m} \frac{\partial}{\partial y} + \frac{(eBx)^2}{2m} + V(z) \right] \psi(\vec{R}) = E \psi(\vec{R}) $$
Where:
- The first term is the kinetic energy operator.
- The second term couples the $x$ and $y$ motion, and is reminiscent of the Lorentz force.
- The third term is a paraboloidal potential confining the electron in the $x$ direction, recalling the harmonic oscillator potential.
- The last term is the confining potential in the $z$ direction, depends on the specific system.

The potential is additive, so the motion along $z$ is separable from the motion in the $x$-$y$ plane and is not influenced by the magnetic field. So, we will solve the equation for the $x$-$y$ plane only and our final wavefunction will be multiplied by the wavefunction along $z$. 
The vector potential does not depend on $y$, which suggests that the wavefunction can be expressed as a plane wave along $y$ with some unknown function along $x$: 
$$ \psi(\vec{R}) = u(x) e^{ik_y y} $$
Substituting this expression in the Schrödinger equation, we have:
$$ \left[ -\frac{\hbar^2}{2m} \left( \frac{\partial^2}{\partial x^2} - k_y^2 \right) + \frac{e\hbar Bx k_y}{m} + \frac{(eBx)^2}{2m} \right] u(x) e^{ik_y y} = E u(x) e^{ik_y y} $$
Dividing both sides by $e^{ik_y y}$, we have:
$$ \left[ -\frac{\hbar^2}{2m} \frac{d^2}{dx^2} + \frac{1}{2} m \omega_C^2 \left( x + \frac{\hbar k_y}{eB} \right)^2 \right] u(x) = E  u(x) $$
where we have completed the square and recognized the cyclotron frequency $\omega_C = \frac{eB}{m}$. We can see that this equation is equivalent to the quantum harmonic oscillator centered at $x_k = -\frac{\hbar k_y}{eB}$ with energy eigenvalues given by:
$$ E_n = \hbar \omega_C \left( n + \frac{1}{2} \right) $$
where $n = 0, 1, 2, ...$ is the Landau level index. The corresponding wavefunctions are given by:
$$ \phi_{nk} (x,y) \propto H_{n-1} \left( \frac{x - x_k}{l_B} \right) e^{-\frac{(x - x_k)^2}{2l_B^2}} e^{ik_y y} $$
where $H_n$ are the Hermite polynomials and $l_B = \sqrt{\frac{\hbar}{eB}}$ is the extension of the wavefunction in the $x$ direction, also known as the magnetic length, $x_k$ can be rewritten as $x_k = -k_y l_B^2$. The wavefunctions are plane waves along the $y$ direction and localized Gaussians along the $x$ direction, centered at $x_k$. The magnetic length gives us an idea of how spread out the wavefunction is in the $x$ direction, and it decreases with increasing magnetic field strength.
![[Pasted image 20260113164843.png]]
![[Pasted image 20260113170018.png]]
There isn't only one oscillator, since $x_k$ depends on the wavevector $k_y$, which can take multiple values. To find the allowed values of $k_y$, we consider a finite sample of length $L_y$ along the $y$ direction with periodic boundary conditions. The allowed values of $k_y$ are given by:
$$ k_y = \frac{2\pi}{L_y} n_{k_y}$$
where $n_{k_y}$ is an integer. $k_y$ is discrete with a spacing of $\Delta k_y = \frac{2\pi}{L_y}$. The 





## References
