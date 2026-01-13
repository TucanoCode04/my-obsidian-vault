
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
where $n_{k_y}$ is an integer. $k_y$ is discrete with a spacing of $\Delta k_y = \frac{2\pi}{L_y}$. To find the upper boundary for $k_y$, we consider that $k_y$ sets the location of the harmonic oscillators along the $x$ direction through the relation $x_k = -k_y l_B^2 = -\frac{\hbar}{eB} \frac{2\pi}{L_y}$. The harmonic oscillators can only be located within the sample, so we have the condition:
$$ 0 < x_k < L_x \quad \Rightarrow \quad 0 < -\frac{\hbar k_y}{eB} < L_x $$
So the available states in the $y$ direction are given by:
$$ -\frac{eB L_x}{\hbar} < k_y < 0 $$
So there are oscillators in the $x$ direction spaced by $-\frac{\hbar}{eB} \frac{2\pi}{L_y}$, determined by the allowed values of $k_y$, all sharing the same energy eigenvalue for a given Landau level $n$, $E_n = \hbar \omega_C (n + \frac{1}{2})$. 
![[Pasted image 20260113173641.png]]
The total number of allowed states sharing the same energy within a Landau level (which is equal to the number of harmonic oscillators that can fit within the sample) is given by:
$$ N_B = \frac{\text{range of variation of } k_y}{\text{spacing between allowed } k_y} = \frac{\frac{eB L_x}{\hbar}}{\frac{2\pi}{L_y}} = \frac{eB}{h} L_x L_y $$
The height of each Landau level is then given by:
$$ n_B = \frac{N_B}{L_x L_y} = \frac{eB}{2\pi \hbar} $$
![[Pasted image 20260113173918.png]]

##### Flux Quantum View (Semiclassical Picture)
Introducing the concept of quantum of flux, which is given by:
$$ \phi_0 = \frac{2\pi \hbar}{e} $$
As the flux carried by a single state in a Landau level, we can rewrite the number of states per Landau level as: 
$$ N_B = \frac{\text{Flux through the sample } BL_x L_y}{\text{Flux quantum }} = \frac{eB}{2\pi \hbar} L_x L_y = \frac{BL_x L_y}{\phi_0} $$
The sample can then be seen as $N_B$ electrons following circular orbits in the $x$-$y$ plane each enclosing a quantum of flux $\phi_0$.
![[Pasted image 20260113175533.png]]

##### Effect of Impurities
In a real system, impurities and defects are always present, which can affect the Landau levels. The presence of impurities can lead to the broadening of the delta-like Landau levels into Gaussian-like peaks characterized by a full width at half maximum $\Gamma =\frac{\hbar}{\tau}$, where $\tau$ is the scattering time due to impurities, also called lifetime of the electrons. The density of states in the presence of impurities can be viewed as:
![[Pasted image 20260113175827.png]]
We want to work with a material and at a temperature such that the Landau levels are distinguishable, but not with an extremely pure material (later we will see why). 

##### Dependance on Magnetic Field
As we increase the magnetic field $B$, the cyclotron frequency $\omega_C = \frac{eB}{m}$ increases, leading to an increase in the energy separation between Landau levels, given by $\Delta E = \hbar \omega_C$. This results in a larger gap between the Landau levels in the density of states. Additionally, as $B$ increases, the number of states per Landau level $n_B = \frac{eB}{2\pi \hbar}$ also increases, meaning that each Landau level can accommodate more electrons. This leads to a higher density of states at each Landau level as the magnetic field strength increases, so more degenerate states are available at each energy level.
![[Pasted image 20260113180202.png]]

##### Shubnikov–de Haas Effect 
The Shubnikov–de Haas (SdH) effect is a quantum oscillatory phenomenon observed in the electrical resistivity of a material when subjected to a strong magnetic field at low temperatures. It arises due to the quantization of electron energy levels into Landau levels in the presence of a magnetic field. As the magnetic field strength varies, the Landau levels move through the Fermi energy, leading to periodic variations in the density of states at the Fermi level. This results in oscillations in the electrical resistivity of the material as a function of the magnetic field strength.
![[Pasted image 20260113180921.png]]
The measured resistivity oscillations can be understood in terms of the filling of Landau levels.
When the Fermi energy lies between two Landau levels, the density of states at the Fermi level is low, so when the filling factor is an integer the bulk of the 2DEG does not contribute to conduction, leading to a minimum in resistivity. Conversely, when the Fermi energy coincides with a Landau level, the density of states at the Fermi level is high, resulting in increased scattering and higher resistivity. This leads to oscillations in resistivity as the magnetic field is varied, known as SdH oscillations.
The electron density of the 2DEG is kept constant, while the magnetic field is varied, leading to changes in the filling factor $\nu$, defined as:
$$ \nu = \frac{n_{2D}}{n_B} = \frac{n_{2D} \phi_0}{B} $$
Where $n_{2D}$ is the electron density of the 2DEG. As the magnetic field increases, the filling factor decreases, leading to oscillations in resistivity as Landau levels move through the Fermi energy. The SdH effect provides valuable insights into the electronic properties of materials, such as effective mass, scattering mechanisms, and Fermi surface characteristics.
![[Pasted image 20260113180941.png]]

#### Quantum Hall Effect
In the same setup used to observe the SdH effect, if we measure the Hall resistance $R_{xy}$ instead of the longitudinal resistance $R_{xx}$, we observe the Quantum Hall Effect (QHE). The Hall resistance exhibits quantized plateaus at specific distances proportional to $\frac{h}{e^2}$.
![[Pasted image 20260113181212.png]]
To understand the origin of the plateaus, we have to consider the effect of the edges on the energy of the states in the Landau levels. At the edge the electron orbits are distorted, the frequency of oscillation increases (shorter orbits), because the electron cannot go beyond the edge, leading to an increase in energy of the states at the edge of the sample (since frequency and energy are proportional, the closer the state is to the edge, the higher its energy). 
![[Pasted image 20260113182012.png]]
Starting from the Schrödinger equation:
$$\left[ \frac{1}{2m} \left[- \hbar^2 \frac{\partial^2}{\partial x^2} + \left(-i\hbar \frac{\partial}{\partial y} - eBx \right)^2 - \hbar^2 \frac{\partial^2}{\partial z^2} \right] + + V(z) \right] \psi(\vec{R}) = E \psi(\vec{R}) $$
We introduce a confining potential $V(x)$ along the $x$ direction to account for the edges of the sample:
$$\begin{cases} V(x) = 0 & \text{for } |x| < \frac{L_x}{2} \\ V(x) = \infty & \text{for } |x| \geq \frac{L_x}{2} \end{cases} $$
![[Pasted image 20260113182417.png]]
The Schrödinger equation is not analytically solvable, computations show that states in the middle of the sample (associated with $k_y$ values such that $|x_k| \ll \frac{L_x}{2}$) have energies close to the Landau levels solutions found before, while states close to the edges (associated with $k_y$ values such that $|x_k| \sim \frac{L_x}{2}$) are squeezed in less space and their energy increases significantly.
![[Pasted image 20260113182733.png]]
By watching the energy of different levels of the harmonic oscillator as a function of $x$ one can see that the energy increases near the edges.
![[Pasted image 20260113182821.png]]

Whenever the Fermi level is between two Landau levels, the bulk of the 2DEG is insulating since there are no available states at the Fermi energy. However, at the edges of the sample, there are states with energies that cross the Fermi level due to the edge effects. These edge states are localized at the boundaries of the sample and can carry current without dissipation. As a result, when the Fermi level lies between Landau levels, the conduction occurs primarily through these edge states, leading to quantized Hall conductance and the observation of plateaus in the Hall resistance.
![[Pasted image 20260113182947.png]]
Each state carries half a quantum of conductance $\frac{G_0}{2} = \frac{e^2}{h}$ , resulting in a Quantum Hall resistance given by:
$$ R_{xy} = \frac{1}{G} = \frac{1}{\nu \frac{e^2}{h}} = \frac{h}{\nu e^2} $$ 


## References
