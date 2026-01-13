
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
$$ \left[ \frac{1}{2m} \left( -\hbar^2 \frac{\partial^2}{\partial x^2} 





## References
