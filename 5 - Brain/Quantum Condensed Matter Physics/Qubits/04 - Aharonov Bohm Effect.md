
2026-01-12 16:44

Status: 

Tags:

# 04 - Aharonov Bohm Effect
The Aharonov Bohm Effect is a quantum mechanical phenomenon that demonstrates how the vector potential affects the transmittance of electrons even in regions where the magnetic field is zero. Basically, it shows that the potentials in quantum mechanics have physical significance, unlike in classical mechanics where only fields matter.
Let's suppose we have a solenoid that generates a magnetic field confined within a loop, but in the ring arms the magnetic field is zero. We need to find an $A$ vector potential suitable for this configuration.
![[Pasted image 20260112173657.png]]
We notice that any close line of $A$ that includes the solenoid span an area that contains the entire magnetic flux $\Phi_M$. 
$$\int_{\Sigma} \vec{B} \cdot d\vec{S} = \int_{\Sigma} (\nabla \times \vec{A}) \cdot d\vec{S} = \Phi_M$$
Therefore, by applying Stokes' theorem, we have:
$$\oint A \cdot d\vec{l} = \int_{\Sigma} (\nabla \times \vec{A}) \cdot d\vec{S} = \Phi_M$$
So any $A$ we choose that exists on the arms of the ring must be non zero (where we need to calculate Schrödinger's equation).
We use Coulomb gauge, so $\nabla \cdot A = 0$. 
Assuming a solenoid generating a uniform magnetic field $B$ inside, we can find $A$ in cylindrical coordinates:
$$\begin{cases}
2 \pi r A(r) = \pi r^2 B \Rightarrow A(r) = \frac{B r}{2} & r < a \\
2 \pi r A(r) = \pi a^2 B \Rightarrow A(r) = \frac{B a^2}{2 r} & r > a
\end{cases}$$
Where $a$ is the radius of the solenoid.
![[Pasted image 20260112174833.png]]
If we plot $A(r)$, we see that 


## References
