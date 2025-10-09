
2025-09-29 19:07

Status: 

Tags: [[Electric Field]] [[Magnetic Field]] [[Schrodinger Equation]]

# Scalar and Vector Potential
##### Divergence and Curl
The divergence of a vector field $\vec{A}$  is a scalar field representing the rate of change of the vector field's magnitude in all directions in a infinitezimal volume around a point. It is defined as:
$$\nabla \cdot \vec{A} = \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}$$
where $A_x$, $A_y$ and $A_z$ are the components of the vector field $\vec{A}$ in the x, y and z directions respectively.

The curl of a vector field $\vec{A}$ is another vector field representing the rotation or circulation of the vector field in all directions around a point. It is defined as:
$$\nabla \times \vec{A} = \left( \frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z} \right) \hat{i} + \left( \frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x} \right) \hat{j} + \left( \frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y} \right) \hat{k}$$
where $\hat{i}$, $\hat{j}$ and $\hat{k}$ are the unit vectors in the x, y and z directions respectively.
It is represented in this way because, for each direction, the curl component is calculated as the difference between the rate of change of the vector field's components perpendicular to that direction. 
##### Electric Field
We can express the behavior of the electric field $\vec{F}$ using Maxwell's equations:
$$\nabla \cdot \vec{E} = \frac{\rho}{\epsilon_0}$$
$$\nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}$$
Where $\rho$ is the charge density, which is the amount of electric charge per unit volume, so the electric field is proportional to the charge density and it diverges from positive charges and converges towards negative charges. $\epsilon_0$ is the permittivity of free space, which is a constant that describes how electric fields interact with the vacuum. $\vec{B}$ is the magnetic field, which can vary with time depending on the motion of charges. The curl of the electric field is proportional to the negative rate of change of the magnetic field, indicating that a changing magnetic field induces a circulating electric field. 
We force the electric field to be conservative, meaning that the work done by the electric field on a charged particle moving between two points is independent of the path taken. Explained in simpler terms, if you move a charged particle in a closed loop in an electric field, the net work done by the electric field on the particle is zero, because the electric field is conservative.
This implies that the curl of the electric field must be zero:
$$\nabla \times \vec{F} = 0$$
We can prove that, by using Stokes' theorem:
$$\oint_C \vec{F} d\vec{l} = \int_{\epsilon} (\nabla \times \vec{F}) ds = 0$$
We said that the field is irrotational, meaning that the curl of the field is zero.
A property of a scalar field $\phi$ is that its gradient is irrotational:
$$\nabla \times (\nabla \phi) = 0$$
This property is obvious, because the gradient of a scalar field points in the direction of the maximum rate of increase of the scalar field, and it does not have any rotational component, and the curl measures the rotational component of a vector field.
So we can express the electric field as the gradient of a scalar potential:
$$\vec{F} = -\nabla \phi$$ where $\phi$ is the electric potential, which represents the electric potential energy per unit charge at a given point in space. The negative sign indicates that the electric field points in the direction of decreasing electric potential, meaning that positive charges will naturally move towards regions of lower potential energy. The higher the potential, the faster the charge will move. 

## References
