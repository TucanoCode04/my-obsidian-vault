
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
We now analyze, at a fictitious time $t<0$, those two regions as isolated, so we have two separate pieces of crystal, one p type and one n type. In each region, the Fermi level is constant and the assumption of global neutrality holds($\rho(x) = 0$) in each region separately. 
At time $t=0$ we put the two regions in contact, in a unique and ideal crystal. 




## References
