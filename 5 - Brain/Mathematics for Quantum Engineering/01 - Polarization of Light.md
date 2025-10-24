
2025-10-24 10:21

Status: 

Tags:

# Polarization of Light
An electromagnetic wave consists of oscillating electric and magnetic fields that are perpendicular to each other and to the direction of wave propagation. For example, a wave traveling in the z-direction has its electric field oscillating up and down on the x-axis and its magnetic field oscillating side to side on the y-axis.
Polarization of light refers to the orientation of the oscillations of the electric field vector in an electromagnetic wave. In unpolarized light, the electric field vectors vibrate in multiple planes perpendicular to the direction of propagation. In contrast, polarized light has electric field vectors that vibrate predominantly in a single plane.
![[Pasted image 20251024112911.png]]
Considering an electromagnetic wave traveling in the z-direction, the electric field can be represented as:
$$\begin{cases}
E_x(z,t) = E_{0,x} \cos(kz - \omega t + \phi_1) = E_0 \cos\theta \cos(kz - \omega t + \phi_1) \\
E_y(z,t) = E_{0,y} \cos(kz - \omega t + \phi_2) = E_0 \sin\theta \cos(kz - \omega t + \phi_2) \\
E_z(z,t) = 0
\end{cases}$$
where:
- $E_{0,x}$ and $E_{0,y}$ are the amplitudes of the electric field components in the x and y directions, respectively(so that $E_{0,x} = E_0 \cos\theta$ and $E_{0,y} = E_0 \sin\theta$).
- $E_0$ is the overall amplitude of the electric field(by amplitude, we mean the maximum strength of the electric field vector).
- $\theta$ is the angle that determines the relative amplitudes of the x and y components(i.e., the polarization angle).
- $k$ is the wave number, related to the wavelength $\lambda$ by $k = \frac{2\pi}{\lambda}$(the wave number indicates how many wave cycles fit into a unit distance, where by wave cycles we mean the repeating patterns of the wave, with a higher wave number corresponding to a shorter wavelength).
- $\omega$ is the angular frequency, related to the frequency $f$ by $\omega = 2\pi f$(the angular frequency indicates how many oscillations occur in a unit time, with a higher angular frequency corresponding to a higher frequency).
- $\phi_1$ and $\phi_2$ are the phase constants for the x and y components, respectively(these constants determine the initial phase of the wave at position $z = 0$ and time $t = 0$, where by phase we mean the position of the wave in its cycle at a given point in time and space).
- $t$ is time, and $z$ is the position along the direction of wave propagation.
![[Pasted image 20251024114216.png]]
$$E_0 = (E_{0,x}, E_{0,y}, 0) = (E_0 \cos\theta, E_0 \sin\theta, 0)$$
By the Euler's formula, we can express the electric field components as:
$$e^{i\phi} = \cos\phi + i\sin\phi \quad \Rightarrow \quad cos(kz - \omega t + \phi_1) = Re\{e^{i(kz - \omega t + \phi_1)}\} = \frac{e^{i(kz - \omega t + \phi_1)} + \text{c.c.}}{2}$$
where "c.c." stands for complex conjugate. Thus, the electric field components can be rewritten as:
$$\begin{cases}
E_x(z,t) = \frac{E_0 \cos\theta}{2} \left( e^{i(kz - \omega t + \phi_1)} + \text{c.c.} \right) \\
E_y(z,t) = \frac{E_0 \sin\theta}{2} \left( e^{i(kz - \omega t + \phi_2)} + \text{c.c.} \right) \\
E_z(z,t) = 0
\end{cases}$$
We forget about the "c.c." term for simplicity, and express the electric field vector as:
$$\vec{E}(z,t) = {E_x}(z,t) \hat{x} + {E_y}(z,t) \hat{y} = \frac{E_0}{2} e^{i(kz - \omega t + \phi_1)} \left( \cos\theta \hat{x} + \sin\theta e^{i(\phi_2 - \phi_1)} \hat{y} \right)$$
The polarization state of the light wave is determined by the relative magnitudes and phase difference between the x and y components of the electric field. By fixing $\vec{z}= -\frac{\phi_1}{k}$, we can analyze the polarization at a specific position along the propagation direction.
$$\vec{E}(\vec{z},t) = \frac{E_0}{2} e^{i(- \omega t)} \left( \cos\theta \hat{x} + \sin\theta e^{i\phi} \hat{y} \right)$$
where $\phi = \phi_2 - \phi_1$ is the phase difference between the y and x components. We can then classify the polarization vector:
$$\vec{p}(z,t) = e^{i(- \omega t)} \left( \cos\theta \hat{x} + \sin\theta e^{i\phi} \hat{y} \right) = e^{i(- \omega t)} \left( \hat{x} + m e^{i\phi} \hat{y} \right)$$
where $m = \tan\theta$ is the ratio of the amplitudes of the y and x components of the electric field. 
In the $\vec{p}(z,t)$ expression, there is no motion of intensity of the field, only the direction of the electric field vector changes with time.
##### Classification of Polarization


## References
