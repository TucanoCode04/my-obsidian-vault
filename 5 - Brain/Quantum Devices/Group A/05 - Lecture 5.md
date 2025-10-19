
2025-10-16 16:16

Status: 

Tags:

# Lecture 5
##### Non Homogeneous Devices At Equilibrium
The non homogeneity aspect implies position dependency on the carrier densities:
$$n = n(x) \quad p = p(x)$$
These dependencies explicit the presence of diffusion currents:
$$J_{n, diff} |_{eq} \neq 0 \quad J_{p, diff} |_{eq} \neq 0$$
However, the equilibrium condition, called of detailed balance, implies that the total current for both carriers SEPARATELY is zero:
$$J_n |_{eq} = 0 \quad J_p|_{eq} = 0$$
So we need drift currents that compensates separately the diffusion currents. So the detailed balance condition implies the existence of electric fields inside the device at equilibrium such that:
$$J_{n, drift} |_{eq} + J_{n, diff} |_{eq} = 0 \quad J_{p, drift} |_{eq} + J_{p, diff} |_{eq} = 0$$
We will have regions where the field is non zero, and regions where it is zero. This electric field is called built-in electric field(or contact electric field), but it doesn't exist by itself, it comes with electrostatic laws: if we have an electric field we have a potential difference between points of the non homogeneous device called built-in voltage. This is caused by two different parts of the material with different properties, so we have a charge distribution inside the device that creates an electric field. 
$$\varepsilon (x) |_{eq} \neq 0 \quad \Rightarrow \quad \frac{\partial\psi}{\partial x}|_{eq} = - \varepsilon(x) |_{eq} \neq 0$$
##### Example of Non Homogeneous Device: The pn Junction
Let's examine a piece of crystal where we can differentiate two regions: one with a high density of acceptors(p type) and one with a high density of donors(n type). This is called a pn junction. We define it in function of the position(since we are in a non homogeneous device). 
We define the metallurgical junction as the point where the acceptor and donor densities are equal, in a graph showing the net doping profile in function of position it is the point where the curve crosses the x axis.
To simplify the analysis we assume an abrupt junction, meaning that the transition between the two regions is very sharp, not allowing for a smooth transition from $N_A$ to $N_D$.
We now analyze, at a fictitious time $t<0$, those two regions as isolated, so we have two separate pieces of crystal, one p type and one n type. In each region, the Fermi level is constant and the assumption of homogeneity and global neutrality holds($\rho(x) = 0$) in each region separately. 
It has been doped with acceptor atoms, each acceptor captures one electron, becoming negatively ionized, and leaving behind a hole in the valence band. To find a free electron in the conduction band is very unlikely if we think about the mass action law:
$$n \cdot p = n_i^2$$
At time $t=0$ we put the two regions in contact, in a unique and ideal crystal. We don't have the technology to connect instantly two pieces of crystal, but we want to imagine that each free carrier is now able to diffuse freely from one region to the other. So there should be a transient(instantaneous) that creates a net diffusion of electrons from the n region to the p region, and holes from the p region to the n region, due to the concentration gradients. We want to then analyze the built-in electric field that will be created to restore the equilibrium condition of detailed balance. 
For $t>0$, a transient starts, and electrons start diffusing from the n region n region to the p region, leaving behind positively ionized donor atoms in the n region, and holes start diffusing from the p region to the n region, leaving behind negatively ionized acceptor atoms in the p region. 
Far from the center of the system, the material remains neutral($\rho = 0$), since the free carrier densities are very high compared to the ionized impurity densities. So the number of holes equals the number of ionized acceptors in the p region, and the number of electrons equals the number of ionized donors in the n region. 
In the central region, close to the metallurgical junction, we have a space-charge depleted region, where the free carrier densities are very low compared to the ionized impurity densities. So in this region, the net charge density is approximately equal to the negative of the ionized impurity density:
$$\rho(x) \approx \begin{cases} - q N_A & x < 0 \\ + q N_D & x > 0 \end{cases}$$
This region is called the depletion region or space-charge region, and it extends from $-x_p$ to $x_n$, where $x_p$ and $x_n$ are the widths of the depletion region in the p and n sides respectively. To uniquely define the thickness of the depletion region, we use the same approximation from the abrupt junction: we assume that the transition from the neutral region to the depletion region is very sharp(depletion approximation).
Globally, the crystal remains neutral, so the total negative charge in the p side of the depletion region must equal the total positive charge in the n side:
$$q N_A x_p = q N_D x_n \quad \Rightarrow \quad N_A x_p = N_D x_n$$
We integrate the charge density to find the built-in electric field in the depletion region using Gauss's law:
$$\frac{d \varepsilon}{d x} = \frac{\rho(x)}{\epsilon} \quad \Rightarrow \quad \varepsilon(0) = -\frac{qN_A}{\epsilon} x_p = \frac{qN_D}{\epsilon} x_n$$
The functions are even because of global neutrality.
![[Pasted image 20251019180547.png]]
We can integrate again to find the built-in potential:
$$\frac{d \psi}{d x} = = - \varepsilon(x) \quad \Rightarrow \quad -\varepsilon(0) = \frac{qN_A}{\epsilon} x_p = \frac{qN_D}{\epsilon} x_n \quad \Rightarrow \quad V_{bi} = \psi(x_n) - \psi(-x_p)= \phi_n +\phi_p$$
where $\phi_n$ and $\phi_p$ are the potential differences between the neutral regions and the junction on the n and p sides respectively, choosing $\psi(-x_p) = 0$ as reference. We can find expressions for $\phi_n$ and $\phi_p$ integrating:
$$\frac{d \psi}{d x} = - \varepsilon(x) \quad \Rightarrow \quad \psi(x) - \psi(0) = - \int_{x_1}^{x_2} [-\varepsilon(x)] dx \quad \Rightarrow \quad
\begin{cases}
\phi_n = \psi(x_n) - \psi(0) = \frac{1}{2} x_n [-\varepsilon(0)] = q\frac{N_D}{2\epsilon} x_n^2 \\
\phi_p = \psi(0) - \psi(-x_p) = -\frac{1}{2} x_p [-\varepsilon(0)] = q\frac{N_A}{2\epsilon} x_p^2
\end{cases}$$
![[Pasted image 20251019181955.png]]
$V_{bi}$ is the built-in voltage of the pn junction at equilibrium, so the voltage difference between the two ends of the depletion region. 
(LOOK BETTER WHY WE INTEGRATED(EASIER WAY OF SOLVING?) AND THE SHAPE OF THE FUNCTIONS)
We now have 2 equations and 2 unknowns($x_n$ and $x_p$), but if $V_{bi}$ is known we can find explicit expressions for $x_n$ and $x_p$:
$$\begin{cases}
V_{bi} = q\frac{N_D}{2\epsilon} x_n^2 + q\frac{N_A}{2\epsilon} x_p^2 \\


## References
