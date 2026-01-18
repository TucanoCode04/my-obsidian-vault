
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
$$J = \frac{\hbar e}{2mi} \left( \psi^* \frac{\partial\psi}{\partial  x} - \psi \frac{\partial\psi^*}{\partial x} \right)$$In our case the hamiltonian does not depend on time, so:$$\hat{H} = \hat{H}(x) \quad \Rightarrow \quad \Psi(x, t) = \psi(x) e^{-i\omega t}$$ So as we see in the current density expression the time dependent part cancels out:$$e^{i\omega t} e^{-i\omega t} - e^{-i\omega t} e^{i\omega t} = 0$$Since the derivative is only with respect to $x$, so we can just consider the spatial part of the wavefunction $\psi(x)$. (When we have time independent hamiltonians the time dependence consists only of a phase factor that does not affect the probability density or current.)

Now basically, we can see our transmission rate as the ratio between the transmitted current density in the region 2 and the incident current density in region 1. And following the same logic we can see the reflection rate as the ratio between the reflected current density in region 1 and the incident current density in region 1. So we have:$$T = \frac{J_2^{trans}}{J_1^{inc}} \quad , \quad R = \frac{J_1^{refl}}{J_1^{inc}}$$Calculating the current densities in each region we have:$$\begin{cases} J_1^{inc} = \frac{\hbar k_1}{m} |A|^2 \\ J_1^{refl} = \frac{\hbar k_1}{m} |B|^2 \\ J_2^{trans} = \frac{\hbar k_2}{m} |C|^2 \end{cases}$$So the transmission and reflection coefficients become:$$T = \frac{k_2}{k_1} \left| \frac{C}{A} \right|^2 \quad , \quad R = \left| \frac{B}{A} \right|^2$$We can see that the transmission coefficient depends on the ratio of the wavevectors $\frac{k_2}{k_1}$, which accounts for the change in velocity of the electron as it moves from region 1 to region 2 and also on the ratio of the amplitudes of the transmitted and incident waves $\frac{C}{A}$. The reflection coefficient depends only on the ratio of the amplitudes of the reflected and incident waves $\frac{B}{A}$.

We want to see how to calculate $T$ and $R$ using the transfer matrix $T^{(21)}$. From the definition of the transfer matrix we have:$$\begin{pmatrix} C \\ D \end{pmatrix} = T^{(21)} \begin{pmatrix} A \\ B \end{pmatrix}$$If we consider a barrier, we have no incoming wave from region 2, so $D = 0$. So we can write:$$\begin{pmatrix} C \\ 0 \end{pmatrix} = T^{(21)} \begin{pmatrix} A \\ B \end{pmatrix}$$This gives us two equations:$$\begin{cases} C = T_{11}^{(21)} A + T_{12}^{(21)} B \\ 0 = T_{21}^{(21)} A + T_{22}^{(21)} B \end{cases}$$From the second equation we can express $B$ in terms of $A$:$$B = -\frac{T_{21}^{(21)}}{T_{22}^{(21)}} A$$Substituting this into the first equation gives us:$$C = \left( T_{11}^{(21)} - \frac{T_{12}^{(21)} T_{21}^{(21)}}{T_{22}^{(21)}} \right) A$$Now we can express the transmission and reflection coefficients in terms of the elements of the transfer matrix:$$T = \frac{k_2}{k_1} \left| \frac{C}{A} \right|^2 = \frac{k_2}{k_1} \left| T_{11}^{(21)} - \frac{T_{12}^{(21)} T_{21}^{(21)}}{T_{22}^{(21)}} \right|^2 = \frac{k_2}{k_1} \left| \frac{det(T^{(21)})}{T_{22}^{(21)}} \right|^2$$$$R = \left| \frac{B}{A} \right|^2 = \left| -\frac{T_{21}^{(21)}}{T_{22}^{(21)}} \right|^2 = \left| \frac{T_{21}^{(21)}}{T_{22}^{(21)}} \right|^2$$Where we used the property of the determinant of a 2x2 matrix: $det(T) = T_{11} T_{22} - T_{12} T_{21}$. So, we had a discontinuity at $x = 0$, which we expressed using the transfer matrix $T^{(21)}$. This matrix allowed us to relate the coefficients of the wavefunctions on either side of the barrier and to calculate the transmission and reflection coefficients based on these coefficients.
In this kind of simple systems, without time dependence and the wavefunctions being symmetric plane waves with respect to the x-axis, a theorem states that the determinant of the transfer matrix is equal to 1: $det(T) = 1$. This property simplifies the expressions for the transmission and reflection coefficients:
$$T = \frac{k_2}{k_1} \left| \frac{1}{T_{22}^{(21)}} \right|^2 \quad , \quad R = \left| \frac{T_{21}^{(21)}}{T_{22}^{(21)}} \right|^2$$

We could have even approached this problem by defining the incoming in terms of the outgoing, so expressing the coefficients in region 1 in terms of those in region 2. This would have led us to define a different transfer matrix $S$:$$\begin{pmatrix} A \\ B \end{pmatrix} = S^{(12)} \begin{pmatrix} C \\ D \end{pmatrix}$$
Where the transfer matrix $S^{(12)}$ (meaning from region 2 to region 1, or equally region 1 in terms of region 2) is given by:$$S^{(12)} = \frac{1}{2k_1} \begin{pmatrix} k_1 + k_2 & k_1 - k_2 \\ k_1 - k_2 & k_1 + k_2 \end{pmatrix}$$Which is basically the inverse of the transfer matrix $T^{(21)}$: $S^{(12)} = (T^{(21)})^{-1}$. This approach would lead us to similar expressions for the transmission and reflection coefficients:$$T = \frac{k_2}{k_1} \left| \frac{1}{S_{11}^{(12)}} \right|^2 \quad , \quad R = \left| \frac{S_{21}^{(12)}}{S_{11}^{(12)}} \right|^2$$


![[Pasted image 20260115155422.png]]
So if for example we add another barrier at position $x = d$, we can define a new region 3 ($x > d$) with potential $V_3$ and wavevector $k_3$. We can define what would happen in terms of transfer matrices:
$$\begin{pmatrix} E \\ F \end{pmatrix} = T^{(32)} \begin{pmatrix} C \\ D \end{pmatrix}$$
Where $E$ and $F$ are the coefficients of the wavefunction in region 3, and $T^{(32)}$ is the transfer matrix from region 2 to region 3. Now we can combine the two transfer matrices to relate the coefficients in region 3 directly to those in region 1:$$\begin{pmatrix} E \\ F \end{pmatrix} = T^{(32)} T^{(21)} \begin{pmatrix} A \\ B \end{pmatrix} = T^{(31)} \begin{pmatrix} A \\ B \end{pmatrix}$$Where $T^{(31)} = T^{(32)} T^{(21)}$ is the combined transfer matrix from region 1 to region 3. This approach can be extended to multiple barriers or regions by multiplying the corresponding transfer matrices, allowing us to analyze complex tunneling structures efficiently.
And if we assume that there is no incoming wave from region 3, so $F = 0$, we can again derive the transmission and reflection coefficients for the entire structure using the elements of the combined transfer matrix $T^{(31)}$:
$$T = \frac{k_3}{k_1} \left| \frac{det(T^{(31)})}{T_{22}^{(31)}} \right|^2 \quad , \quad R = \left| \frac{T_{21}^{(31)}}{T_{22}^{(31)}} \right|^2$$
Which again simplifies to:
$$T = \frac{k_3}{k_1} \left| \frac{1}{T_{22}^{(31)}} \right|^2 \quad , \quad R = \left| \frac{T_{21}^{(31)}}{T_{22}^{(31)}} \right|^2$$

(The professor doesn't specify the reflection every time, but it's good to have it for completeness)

And for $n-1$ barriers, we also normally defines $V_1$ and $V_{n}$ as equal and flat and $k_1$ and $k_n$ are the same as a consequence, so the electron comes from a region with potential $V_1$ and exits to a region with the same potential $V_n = V_1$. So we have $n$ regions and $n-1$ barriers. The system can be described as:$$\begin{pmatrix} Y \\ Z\end{pmatrix} = T^{(n1)} \begin{pmatrix} A \\ B \end{pmatrix}$$Where $Y$ and $Z=0$ are the coefficients of the wavefunction in region $n$, and $T^{(n1)}$ is the combined transfer matrix from region 1 to region $n$, obtained by multiplying the transfer matrices of each barrier:$$T^{(n1)} = T^{(n(n-1))} T^{((n-1)(n-2))} \cdots T^{(21)}$$The matrices are not all the same since they occupy different positions in space, meaning they have $x$ dependence.
So we can again derive the transmission coefficient for the entire structure using the elements of the combined transfer matrix $T^{(n1)}$:$$T = \frac{|Y|^2}{|A|^2} = \left| \frac{1}{T_{22}^{(n1)}} \right|^2$$
If this time the the discontinuity is from $0$ to $d$(region 1 from $x < 0$ to region 2 from $x> d$) we have to consider the propagation of the wavefunction in region 2. ![[Pasted image 20260118175922.png]]
We introduce 2 propagation matrices to account for the phase change of the wavefunction as it propagates through region 2, so this time:$$T^{(21)}(d) = \begin{pmatrix} e^{ik_2 d} & 0 \\ 0 & e^{-ik_2 d} \end{pmatrix} \cdot T^{(21)}(0) \cdot \begin{pmatrix} e^{-ik_1 d} & 0 \\ 0 & e^{ik_1 d} \end{pmatrix}$$Where $T^{(21)}(0)$ is the transfer matrix at the boundary $x = 0$ and the propagation matrices account for the phase accumulation as the wavefunction travels through region 2 of width $d$. This modification is crucial for accurately modeling tunneling through barriers separated by finite distances, as it captures the interference effects that arise from the wave nature of electrons.


## References
