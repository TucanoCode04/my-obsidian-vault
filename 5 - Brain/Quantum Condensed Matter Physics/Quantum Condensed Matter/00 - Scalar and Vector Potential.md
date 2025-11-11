
2025-09-29 19:07

Status: 

Tags: [[Electric Field]] [[Magnetic Field]] [[Schrodinger Equation]]

# Scalar and Vector Potential
##### Divergence and Curl
The divergence of a vector field $\vec{A}$  is a scalar field representing the rate of change of the vector field's magnitude in all directions in a infinitesimal volume around a point. It is defined as:
$$\nabla \cdot \vec{A} = \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}$$
where $A_x$, $A_y$ and $A_z$ are the components of the vector field $\vec{A}$ in the x, y and z directions respectively.

The curl of a vector field $\vec{A}$ is another vector field representing the rotation or circulation of the vector field in all directions around a point. It is defined as:
$$\nabla \times \vec{A} = \left( \frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z} \right) \hat{i} + \left( \frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x} \right) \hat{j} + \left( \frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y} \right) \hat{k}$$
where $\hat{i}$, $\hat{j}$ and $\hat{k}$ are the unit vectors in the x, y and z directions respectively.
It is represented in this way because, for each direction, the curl component is calculated as the difference between the rate of change of the vector field's components perpendicular to that direction. 
##### Electric Field
We can express the behavior of the electric field $\vec{F}$ using Maxwell's equations:
$$\nabla \cdot \vec{F} = \frac{\rho}{\epsilon_0}$$
$$\nabla \times \vec{F} = -\frac{\partial \vec{B}}{\partial t}$$
Where $\rho$ is the charge density, which is the amount of electric charge per unit volume, so the electric field is proportional to the charge density and it diverges from positive charges and converges towards negative charges. $\epsilon_0$ is the permittivity of free space, which is a constant that describes how electric fields interact with the vacuum. $\vec{B}$ is the magnetic field, which can vary with time depending on the motion of charges. The curl of the electric field is proportional to the negative rate of change of the magnetic field, indicating that a changing magnetic field induces a circulating electric field.
We force the electric field to be conservative, meaning that the work done by the electric field on a charged particle moving between two points is independent of the path taken. Explained in simpler terms, if you move a charged particle in a closed loop in an electric field, the net work done by the electric field on the particle is zero, because the electric field is conservative.
This implies that the curl of the electric field must be zero:
$$\nabla \times \vec{F} = 0$$
We can prove that, by using Stokes' theorem:
$$\oint_C \vec{F} d\vec{l} = \int_{\epsilon} (\nabla \times \vec{F}) ds = 0$$
We said that the field is irrotational, meaning that the curl of the field is zero.
A property of a scalar field $\phi$ is that its gradient is irrotational:
$$\nabla \times (\nabla \cdot \phi) = 0$$
This property is obvious, because the gradient of a scalar field points in the direction of the maximum rate of increase of the scalar field, and it does not have any rotational component, and the curl measures the rotational component of a vector field.
So we can express the electric field as the gradient of a scalar potential:
$$\vec{F} = -\nabla \phi$$ where $\phi$ is the electric potential, which represents the electric potential energy per unit charge at a given point in space. The negative sign indicates that the electric field points in the direction of decreasing electric potential, meaning that positive charges will naturally move towards regions of lower potential energy. The higher the potential, the steeper the field, the faster the charge will fall from the high potential to the low potential.
$$\vec{F_{force}} = q\vec{F} = -q\nabla \phi$$
So that means that if my charge is positive, it will move in the direction of decreasing potential, and if my charge is negative, it will move in the direction of increasing potential.

Conservative means that:
$$\int_{A_{path1}}^B \vec{F} d\vec{l} = \int_{A_{path2}}^B \vec{F} d\vec{l}$$
##### Magnetic Field
The magnetic field $\vec{B}$ is described by Maxwell's equations:
$$\nabla \cdot \vec{B} = 0$$
$$\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}$$ 
Where $\mu_0$ is the permeability of free space, which is a constant that describes how magnetic fields interact with the vacuum. $\vec{J}$ is the current density, which is the amount of electric current per unit area. The divergence of the magnetic field is zero, indicating that there are no magnetic monopoles; magnetic field lines always form closed loops and do not begin or end at any point. The curl of the magnetic field is proportional to the current density and the rate of change of the electric field, indicating that electric currents and changing electric fields induce circulating magnetic fields.
This implies that the magnetic field is solenoidal, meaning that the divergence is zero. 
A property of a vector field $\vec{A}$ is that its curl is solenoidal:
$$\nabla \cdot (\nabla \times \vec{A}) = 0$$
This property is obvious, because the curl of a vector field represents the rotation or circulation of the field, and it does not have any divergence component, and the divergence measures the rate of change of the field's magnitude in all directions.
So we can express the magnetic field as the curl of a vector potential:
$$\vec{B} = \nabla \times \vec{A}$$ where $\vec{A}$ is the magnetic vector potential, which is a vector field whose curl gives the magnetic field. The vector potential is not unique; different choices of $\vec{A}$ can lead to the same magnetic field $\vec{B}$, as adding the gradient of any scalar function to $\vec{A}$ does not change its curl.
##### Properties of the potentials
Definition of potential: a potential is a scalar or vector field from which a force field(physical field you can observe) can be derived(spatial or temporal rate of change).
Why do we use potentials? They are powerful tools to express and analyze physical fields, for example the allow us to express conservation laws in a more intuitive way, they simplify Maxwell's equations, and they can encode fields into a simpler, more fundamental form.

For the electric field:
$$\vec{F} = -\nabla \phi \quad \Rightarrow \quad \phi(\vec{x}, t)) = -\int_{- \infty}^{\vec{x}} \vec{F}(\vec{x'}, t) d\vec{x'}$$
$\phi$ is defined up to an additive constant, because the integration of a constant is zero, so adding a constant to the potential does not change the electric field. So we can choose the potential such that $\vec{F}$ does not change as long as:
$$\phi' = \phi + C$$ Where $C$ is a constant.
$$\vec{F} = -\nabla \phi = -\nabla \phi' = \vec{F'}$$

For the magnetic field: 
$$\vec{B} = \nabla \times \vec{A}$$
The curl operation allows for more functions to fulfill the same equation, because the curl of a gradient is zero:
$$\nabla \times (\nabla \chi) = 0$$
So we can add the gradient of any scalar function $\chi$ to the vector potential without changing the magnetic field:
$$\vec{A} \rightarrow \vec{A'} = \vec{A} + \nabla \chi \quad \Rightarrow \quad \vec{B} = \nabla \times \vec{A} = \nabla \times \vec{A'} = \vec{B'}$$
So $\vec{A}$ is defined up to the gradient of a scalar function, so we have the freedom to choose the form of $\vec{A}$ that is most convenient for our calculations, as long as it satisfies the equation for $\vec{B}$.

$\vec{B}$ and $\vec{F}$ are connected and so are their potentials.
General case for $\vec{B}$ varying with time:
$$\nabla \times \vec{F} = -\frac{\partial \vec{B}}{\partial t} = -\frac{\partial}{\partial t} (\nabla \times \vec{A}) = -\nabla \times \left( \frac{\partial \vec{A}}{\partial t} \right)$$
$$\nabla \times \left( \vec{F} + \frac{\partial \vec{A}}{\partial t} \right) = 0$$
Remember that a field with zero curl can be expressed as the gradient of a scalar potential:
$$\nabla \times \left( \nabla \cdot \phi \right) = 0 \quad \Rightarrow \quad \vec{F} = -\nabla \phi - \frac{\partial \vec{A}}{\partial t}$$
 The minus sign in front of the time derivative is a convention, to symbolize the external work done on the charge and not from the charge.
$\vec{F}$ has not to change as we change $\vec{A}$ so something has to compensate the change in $\vec{A}$:
$$\vec{A} \rightarrow \vec{A'} = \vec{A} + \nabla \chi$$
$$- \nabla \phi - \frac{\partial \vec{A}}{\partial t} = -\nabla \phi' - \frac{\partial \vec{A'}}{\partial t} = - \nabla \phi' - \frac{\partial}{\partial t} (\vec{A} + \nabla \chi)$$
We get rid of $\vec{A}$ on both sides:
$$\nabla \left(\phi' - \phi + \frac{\partial \chi}{\partial t}\right) = 0 \quad \Rightarrow \quad \phi' = \phi - \frac{\partial \chi}{\partial t}$$
So the potentials transform as:
$$\vec{A} \rightarrow \vec{A'} = \vec{A} + \nabla \chi$$
$$\phi \rightarrow \phi' = \phi - \frac{\partial \chi}{\partial t}$$
These are called gauge transformations, and they reflect the freedom we have in choosing the potentials without changing the physical fields $\vec{F}$ and $\vec{B}$(Gauge Invariance).
The freedom in choosing $\vec{A}$ could led us to believe that $\vec{A}$ is not physical, but it is not true.
##### Physical meaning of the potentials
**Electric potential $\phi$:**
Assuming no variation in $\vec{B}$ :
$$\vec{F} = -\nabla \phi$$
$\vec{F}$ is a conservative field, so for a charge $q$:
$$\phi(\vec{x}, t) = -\int_{- \infty}^{\vec{x}} \vec{F}(\vec{x'}, t) d\vec{x'}$$
Is symmetric to the work done by the field to move a charge $q$ from infinity to the point $\vec{x}$
$$U = - \int_{- \infty}^{\vec{x}} q\vec{F}(\vec{x'}, t) d\vec{x'}$$
So the electric potential represents the energy per unit charge at a given point in space.

**Magnetic vector potential $\vec{A}$:
Assume a $\vec{B}$ slowly generated by some current from the value 0 to $\vec{B}$. 
Assume a charge $q$ in position $\vec{r}$.
The varying magnetic field affects the charge, by pushing or pulling it, because it generates an electric field. The charge would like to change its momentum as a result of the force from the electric field, but it is constrained by something that keeps it in position $\vec{r}$. We calculate the impulse necessary to keep the charge in position $\vec{r}$:
$$\vec{F_{ext}} = q\left(\vec{F} + \vec{v} \times \vec{B}\right)$$
$$\vec{F} = -\frac{\partial \vec{A}}{\partial t}, \quad \text{there's no static charges so }\nabla \phi = 0$$
$$I = \Delta \vec{p} = \vec{F_{ext}} \Delta t = - \int_{0}^{t} \vec{F_{ext}} dt = = - \int_{0}^{t} q \vec{F} dt = - \int_{0}^{t} q \left(-\frac{\partial \vec{A}}{\partial t}\right) dt = q \vec{A}$$
So the vector potential represents the impulse per unit charge needed to keep a charge in position $\vec{r}$ when the magnetic field varies from 0 to $\vec{B}$.

**Relationship between $\vec{A}$ and the momentum $\vec{p}$ :**
$$I= \Delta \vec{p} = q \vec{A}$$ The general form related related to particle velocity and to magnetic field is:
$$\Delta\vec{p} = m\Delta\vec{v} + q\vec{A}$$ where $m\Delta\vec{v}$ is the change in momentum due to the change in velocity of the particle(mechanical momentum), and $q\vec{A}$ is the change in momentum due to the presence of the magnetic vector potential.

The formula of canonical momentum is:
$$\vec{p} = m\vec{v} + q\vec{A}$$ 
Where $\vec{p}$ is the canonical momentum, which includes both the mechanical momentum $m\vec{v}$ and the contribution from the magnetic vector potential $q\vec{A}$. The canonical momentum is a fundamental concept in quantum mechanics and plays a crucial role in the formulation of the Schrödinger equation in the presence of electromagnetic fields.
##### Expanding the equation of Schrodinger for a free electron in an electric and magnetic field
The time-dependent Schrödinger equation for a free particle is given by:
$$\hat{H} \Psi(\vec{R}, t) = i \hbar \frac{\partial}{\partial t} \Psi(\vec{R}, t)$$ Where $\hat{H}$ is the Hamiltonian operator, $\Psi(\vec{R}, t)$ is the wave function of the particle, $i$ is the imaginary unit, and $\hbar$ is the reduced Planck's constant.
The Hamiltonian operator is divided into kinetic and potential energy terms:
$$\hat{H} = \hat{T} + \hat{V}$$
In this case, we have no potential energy, so $\hat{V} = 0$ and the Hamiltonian operator is equal to the kinetic energy operator:
$$\hat{H} = \hat{T} = \frac{\hat{p}^2}{2m}$$
But since we have an electric and magnetic field the components are affected by it and we have to use the canonical momentum instead of the mechanical momentum:
$$\hat{p} = -i \hbar \nabla$$
$$\hat{p} \rightarrow \hat{p} - q\vec{A}$$
So the Hamiltonian operator becomes:
$$\hat{H} = \frac{(\hat{p} - q\vec{A})^2}{2m} + q\phi$$
Where $q\phi$ is the potential energy term due to the electric potential $\phi$(energy per unit of charge).
Now we can rewrite the Schrödinger equation:
$$\left\{ \frac{1}{2m} \left[\hat{p} - q\vec{A} \right]^2 + q\phi \right\} \Psi(\vec{R}, t) = i \hbar \frac{\partial}{\partial t} \Psi(\vec{R}, t)$$
The effect of changing gauge on the wave function is basically  a phase change:
$$\Psi \rightarrow \Psi' = \Psi e^{\frac{i q \chi}{\hbar}}$$ Where $\chi$ is the scalar function used in the gauge transformation of the potentials.
## References
