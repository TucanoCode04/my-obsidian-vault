
2026-01-15 14:31

Status: 

Tags:

# Transfer Matrix Approach to 1D Tunneling Transport
##### Quantum Tunneling 
Quantum tunneling is a fundamental quantum mechanical phenomenon where particles can pass through potential barriers that they classically shouldn't be able to surmount. For example if we consider an insulating barrier between two metals or doped semiconductors, electrons can tunnel through this barrier, even though they do not have enough energy to overcome it classically $E < V_0$. This effect is crucial in various electronic devices, including tunnel diodes, quantum dots, and scanning tunneling microscopes.

We focus on a simple system, a one-dimensional potential barrier placed in $x = 0$, where we can define two different regions:
- Region 1 ($x < 0$): Free electron region with potential $V_1$, where we have 2 types of waves, incoming and reflected.
	- Incoming wave: $Ae^{ik_1x}$
	- Reflected wave: $Be^{-ik_1x}$, which is similar to the incoming wave but with negative momentum.
- Region 2 ($x > 0$): Barrier region with potential $V_2$, where we have only the transmitted wave.
	- Transmitted wave: $Ce^{ik_2x}$
	- Incident wave: $D e^{-ik_2x}$ (usually set to zero for a barrier)

The Schrödinger equation in each region can be solved to yield the wavefunctions:
$$\begin{cases} \psi_1(x) = Ae^{ik_1x} + Be^{-ik_1x}, & x < 0, & k_1 = \sqrt{\frac{2m(E - V_1)}{\hbar^2}} \\ \psi_2(x) = Ce^{ik_2x} + De^{-ik_2x}, & x > 0, & k_2 = \sqrt{\frac{2m(E - V_2)}{\hbar^2}} \end{cases}$$
Where $E$ is the energy of the electron. $k_1$ and $k_2$ can be real or imaginary depending on whether $E$ is greater than or less than the potential in each region.
For the 2 wavefunctions to be solutions of the Schrödinger equation of the whole system, they must satisfy:
- the continuity of the wavefunction at the boundary ($x = 0$), $\psi_1(0) = \psi_2(0)$
- the continuity of the derivative of the wavefunction at the boundary ($x = 0$), $\psi_1'(0) = \psi_2'(0)$

The derivatives of the wavefunctions in each region are:
$$\begin{cases} \psi_1' = ik_1 Ae^{ik_1x} - ik_1 Be^{-ik_1x} \\ \psi_2' = ik_2 Ce^{ik_2x} - ik_2 De^{-ik_2x} \end{cases}$$
So applying the boundary conditions at $x = 0$ gives us the following equations:
$$\begin{cases} A + B = C + D \\ ik_1(A - B) = ik_2(C - D) \end{cases}$$
One way to write these equations is in matrix form:
$$\begin{pmatrix} 1 & 1 \\ ik_1 & -ik_1 \end{pmatrix} \begin{pmatrix} A \\ B \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ ik_2 & -ik_2 \end{pmatrix} \begin{pmatrix} C \\ D \end{pmatrix} = M_1 \begin{pmatrix} A \\ B \end{pmatrix} = M_2 \begin{pmatrix} C \\ D \end{pmatrix}$$
Where $M_1$ and $M_2$ are the matrices representing the boundary conditions at the interface.
Another way to write this is to express the coefficients in region 2 in terms of those in region 1, as like the output in terms of the input:
$$\begin{cases} C = A + B - D \\ k_1(A - B) = k_2(A+ B - D) - k_2 D \end{cases}$$
$$\Rightarrow \begin{cases} C= \frac{1}{2k_2} \left(k_2 +k_1\right) A + \frac{1}{2k_2} \left(k_2 - k_1\right) B \\ D = \frac{1}{2k_2} \left(k_2 - k_1\right) A + \frac{1}{2k_2} \left(k_2 + k_1\right) B \end{cases}$$
This can also be written in matrix form:
$$\begin{pmatrix} C \\ D \end{pmatrix} = T^{(21)} \begin{pmatrix} A \\ B \end{pmatrix}$$
Where the transfer matrix $T^{(21)}$ (meaning from region 1 to region 2, or equally region 2 in terms of region 1) is given by:$$T^{(21)} = \frac{1}{2k_2} \begin{pmatrix} k_2 + k_1 & k_2 - k_1 \\ k_2 - k_1 & k_2 + k_1 \end{pmatrix}$$So basically the transfer matrix relates the coefficients of the wavefunctions on either side of the barrier, which depends on the potentials $V_1$ and $V_2$ (they define the region of space in which the electron is moving) and the energy of the electron $E$ (by changing the energy of the electron we change $k_1$ and $k_2$, so we change the probability of tunneling through the barrier). So $T^{(21)}(k_1, k_2)$. Just to be clear $M_2^{-1} M_1 = T^{(21)}$.

From a wavefunction, we can evaluate the probability current density $J$, which is given by:
$$J = \frac{\hbar e}{2mi} \left( \psi^* \frac{\partial\psi}{\partial  x} - \psi \frac{\partial\psi^*}{\partial x} \right)$$In our case the hamiltonian does not depend on time, so:$$\hat{H} = \hat{H}(x) \quad \Rightarrow \quad \Psi(x, t) = \psi(x) e^{-i\omega t}$$ So as we see in the current density expression the time dependent part cancels out,


since the derivative is only with respect to $x$, so we can just consider the spatial part of the wavefunction $\psi(x)$. (When we have time independent hamiltonians the time dependence consists only of a phase factor that does not affect the probability density or current.)
## References
