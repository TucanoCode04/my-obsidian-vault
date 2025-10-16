
2025-10-14 15:25

Status: 

Tags:

# Lecture 3
In order to provide a better understanding of the Fermi Energy level, we will see the graphical representation of the Fermi-Dirac distribution function.
![[Pasted image 20251016091018.png]]
We can first identify some asymptotes:
- For very high energy values, the probability of occupation tends to 0
- For very low energy values the probability of occupation tends to 1, meaning that all states are occupied
- At the Fermi level the probability of occupation is $\frac{1}{2}$
- The span of the transition region is $\approx 3kT$

The transition is monotonic, meaning that the probability of occupation decreases as the energy increases. 
The value of $T$ determines the slope of the transition region, the higher the temperature the smoother the slope $T_2 > T_1 = 300K$, the lower the temperature the steeper the slope $T_3 < T_1 = 300K$. 
When the temperature $T \to 0K$ the transition becomes a step function, in fact at $0K$ all the states below $E_F$ are occupied and all the states above it are empty. 

We now have all factors to get an expression for the populations of electrons in the conduction band and holes in the valence band at thermal equilibrium.
$$
n = \int_{E_C}^{\infty} \gamma_n \sqrt{E - E_C} \cdot \frac{1}{1 + e^{\frac{E - E_F}{kT}}} dE \quad , \quad n=n(E_F)
$$
$$
p = \int_{-\infty}^{E_V} \gamma_p \sqrt{E_V - E} \cdot \frac{1}{1 + e^{- \frac{E - E_F}{kT}}} dE \quad , \quad p=p(E_F)
$$
So the density of electrons and holes are integrals over energy that multiplies the density of states by the probability of occupation(Fermi-Dirac function).
We write $n = n(E_F)$ and $p = p(E_F)$ to highlight that the populations depend on the Fermi energy level.
We now have a system of 2 equations with 3 variables, $n$, $p$ and $E_F$.
$E_F$ depends on $n$ and $p$ at equilibrium, $n$ and $p$ depend on doping, so $E_F$ depends on doping. Because it influences the number of carriers, doping influences the Fermi level.
For zero doping, the semiconductor is intrinsic so we use the intrinsic carrier concentration $n_i$:
$$
n = n_i = n(E_{F_i}) \quad , \quad p = n_i = p(E_{F_i}) \quad \Rightarrow \quad n_i^2 = n(E_{F_i}) \cdot p(E_{F_i})
$$
Where $E_{F_i}$ is the intrinsic Fermi level.
Since doping changes the population from $n_i$ to $n$ and $p$, the Fermi level shifts from $E_{F_i}$ to $E_F$.
If we concentrate for example on the n-type doping, the number of carriers in modified to $n > n_i$, causing the Fermi level to shift up $E_F > E_{F_i}$, but $E_F$ is a also a variable in the expression for $p$, so there should be a corresponding decrease in the number of hole $p < n_i$. 
This correlation is $\sqrt{np} = n_i$ and is called the mass action law. We will see that this correlation stands only when the doping does not exceed a certain limit(the semiconductor is not degenerate(to check)).
A semiconductor is non-degenerate if $E_V < E_F < E_C$.
This guarantees that the Fermi level is in the band gap, so we can use the Boltzmann approximation to simplify the equations for $n$ and $p$.
1. For electrons:
$$E > E_F \quad \forall E \in CB \quad \Rightarrow \quad E - E_F > 0 \Rightarrow e^{\frac{E - E_F}{kT}} >> 1$$







## References
