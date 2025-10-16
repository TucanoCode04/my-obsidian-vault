
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
n = \int_{E_C}^{\infty} \gamma_n \sqrt{E - E_C} \cdot \frac{1}{1 + e^{\frac{E - E_F}{kT}}} dE
$$
$$
p = \int_{-\infty}^{E_V} \gamma_p \sqrt{E_V - E} \cdot \left(1 - \frac{1}{1 + e^{\frac{E - E_F}{kT}}}\right) dE
$$






## References
