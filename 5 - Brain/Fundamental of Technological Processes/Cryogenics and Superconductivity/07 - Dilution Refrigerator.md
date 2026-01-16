
2026-01-06 20:06

Status: 

Tags:

# 07 - Dilution Refrigerator
In the previous helium refrigerators discussed, cooling is achieved by using the latent heat of vaporization of helium-4 or helium-3. However, to reach temperatures below approximately 300 millikelvin, a different approach is required. It wav suggested to use the heat of mixing of helium-3 and helium-4 isotopes to achieve lower temperatures. This method is implemented in a device known as a dilution refrigerator.
##### The $^3$He-$^4$He Dilution Refrigerator
In the liquid $^3$He-$^4$He mixture the isotopes concentrations are expressed as $x=x_3=\frac{n_3}{n_3+n_4}$ and $x_4=\frac{n_4}{n_3+n_4}=1-x_3$, where $n_3$ and $n_4$ are the number of moles of $^3$He and $^4$He respectively. 
The temperature of the superfluid phase transition of pure $^4$He is depressed (meaning it occurs at a lower temperature) by diluting the Bose liquid $^4$He with the Fermi liquid $^3$He. At temperatures below approximately 0.87 K, and concentration $x=0.675$, the $\lambda$-line (the line representing the superfluid transition) meets the phase separation curve (representing the boundary between mixed and phase-separated states). Below this temperature, the isotopes only mix for limited concentrations depending on the temperature.
The shaded region is a non-accessible region of temperature-concentration phase diagram.
![[Pasted image 20260115172534.png]]
If we cool a mixture of $^3$He and $^4$He below 0.87 K with a concentration $x >$ 6.6%, the liquid will separate into two phases: a concentrated phase, rich in $^3$He that floats on top of $^4$He since it is less dense, and a dilute phase, rich in $^4$He.
If the temperature is decreased to close to absolute zero, the $^3$He rich liquid becomes almost pure $^3$He, but the great surprise comes at the $^4$He rich phase: even at absolute zero, it contains about 6.6% of $^3$He at saturated vapor pressure. This means that at very low temperatures, there is always a finite solubility of $^3$He in $^4$He, which is important to know for the operation of the dilution refrigerator.
For classical systems, a finite solubility means $S>0$ at $T=0K$, which contradicts the third law of thermodynamics, since the entropy of a pure substance is zero at absolute zero temperature and they should become 2 pure separated phases with zero entropy. However, in this case, the finite solubility is due to quantum effects: for $T\rightarrow 0K$, the $^3$He-$^4$He mixture behaves as a degenerate Fermi system in the ground state for the $^3$He atoms (one particle per quantum state up to the Fermi energy) immersed in a superfluid Bose system for the $^4$He atoms, both with $S\rightarrow 0$ as $T\rightarrow 0K$. 
At $0.5K$, $^4$He is almost fully condensed into the quantum ground state, there are no excitations (phonons or rotons) and thus its entropy, viscosity and specific heat are negligible. So, at this temperature, $^4$He can be considered as an inert superfluid background, it contributes to the volume and effective mass but not to the thermodynamic properties of the mixture. 
The lighter isotope $^3$He with it's nuclear spin $\frac{1}{2}$ behaves as a Fermi liquid, it has to obey Fermi and Pauli statictics, like the conduction electrons in a metal, but at much lower temperatures. 
![[Pasted image 20260115191942.png]]
##### Finite Solubility of $^3$He in $^4$He at Low Temperatures
- **$^3$He in pure $^3$He(x=1):** The chemical potential(which is related to the binding energy) of pure $^3$He is given by the latent heat of evaporation $\mu_{3,C}=L_{3}$. So that the energy required to remove one atom from the liquid in vacuum is $\epsilon_{3,C}=L_{3}/N_A$.
- **One $^3$He atom in pure $^4$He(x=0):** for the dilute phase (phase in which $^3$He is dissolved in $^4$He) the binding energy of one $^3$He atom in pure $^4$He is $\mu_{3,D}/N_A=-\epsilon_{3,D} <-\epsilon_{3,C}$, since the $^3$He atom has a smaller mass, so it has a larger zero-point energy than the $^4$He atoms. Therefore, in the liquid phase $^4$He atoms occupy smaller volume than $^3$He atoms, the $^3$He atom will then be closer to $^4$He atoms than to other $^3$He atoms, leading to a stronger binding energy. So in the end it's binding is stronger in $^4$He than in $^3$He, as $\epsilon_{3,D}>\epsilon_{3,C}$.
- **Many $^3$He atoms in $^4$He (0<x<1):** When more $^3$He atoms are added to the $^4$He liquid, they will start to feel attractive interactions among themselves, due to a magnetic interaction between their nuclear magnetic moments. And due to a density effect, $^3$He has a larger zero-point motion than $^4$He, so it needs more space, thus the liquid nearby $^3$He atoms will be slightly diluted, so another $^3$He atom will feel a lower density region and would like to combine with the first one to gain more space. This effect increases the binding energy per atom as the concentration of $^3$He increases, thus $-\epsilon_{3,D}(x) < -\epsilon_{3,D}(0)$. The only problem is that $^3$He atoms are fermions, so they obey the Pauli exclusion principle, meaning that added $^3$He atoms have to occupy higher energy states, increasing the total energy of the system till the Fermi energy is reached $E_F = k_B T_F$. So the binding energy per atom will decrease as the concentration increases, thus eventually $\mu_{3,D}(x)/N_A = -\epsilon_{3,D}(x) +E_F(x)$. So for x higher than $6.6\%$, $^3$He atoms will prefer to be in the concentrated phase rather than in the dilute phase, leading to phase separation, since it's chemical potential is lower in the concentrated phase than in the dilute phase so it's energetically favorable for the whole system.
- **$^4$He atoms:** For the same reasons as dilute $^3$He atoms, $^4$He atoms will also have a stronger binding energy when surrounded by $^4$He atoms, and since they are bosons, they don't obey the Pauli exclusion principle, there's no reason to decrease their binding energy as their concentration increases, so there will be full separation of $^4$He atoms, leading to pure $^4$He in the dilute phase.
![[Pasted image 20260116112735.png]]
(I put the whole slide for the colors)

##### Cooling Power of the Dilution Process
By measuring the specific heats, we know that the enthalpy of $^3$He in the dilute phase is higher than that in the concentrated phase (since it's binding energy is higher), so we have the heat of mixing that can be used for cooling. $$\dot{Q}=\dot{n}_3[H_{D}(T)-H_{C}(T)]$$This equation suggests us that if we transfer $^3$He atoms from the concentrated phase to the dilute phase at a rate of $\dot{n}_3$ moles per second, cooling will result according to the enthalpy difference between the two phases at temperature T, because enthalpy is give by:$$H(T)-H(0)=\int_0^T C(T)dT$$So we must have $C_{3,D}(T) > C_{3,C}(T)$ for cooling to occur. (Calculations)
![[Pasted image 20260116113522.png]]
So we can see that the cooling power will be $\dot{Q} \approx 84 \dot{n}_3 T^2$, which seems small, but at low temperatures $T<0.35K$ is much higher than the cooling power of evaporating $^3$He which is $\dot{Q}_{evap} = \dot{n}_3 L_3 \propto p(T) \propto e^{-\frac{1}{T}}$. 
![[Pasted image 20260116113805.png]]

##### Osmotic Pressure
![[Pasted image 20260116113824.png]]
As we will see later we have isotopic helium mixtures at varying concentrations and temperature in our refrigerators, in such situations an osmotic pressure $\pi$ develops in the $^3$He-$^4$He mixture. By considering them as ideal solutions (so in the classical regime where $T>T_F$):$$\pi V_{M,4}=xRT$$Where $V_{M,4}$ is the molar volume of pure $^4$He. In a dilution refrigerator a tube connect the mixture in the mixing chamber (where phase separation happens) to the still (where $^3$He is evaporated), so an osmotic pressure difference $\pi_{MC}-\pi_{ST} = (X_{MC}T_{MC}-X_{ST}T_{ST})\frac{R}{V_{M,4}}$develops.
If no $^3$He is pumped from the still, no difference in osmotic pressure, for example assuming the mixing chamber with $6.6\%$ mixture at 10mK and the still at 0.7K, we have:$$X_{ST} = X_{MC}(\frac{T_{MC}}{T_{ST}}) = 6.6\%(\frac{0.01}{0.7}) = 0.094\%$$Instead, if we pump $^3$He from the still, the concentration in the still decreases, leading to an increase in the osmotic pressure difference, which will push $^3$He atoms from the mixing chamber to the still, thus more $^3$He atoms will cross the phase boundary from concentrated phase to dilute phase in the mixing chamber, leading to more cooling power. The maximum osmotic pressure is obtained when the concentration of $^3$He in the still goes to zero:$$X_{ST} \rightarrow 0 \Rightarrow \Delta_{\pi_{max}} = X_{MC}T_{MC}\frac{R}{V_{M,4}} = 20 mbar$$This pressure correspond to the hydrostatic pressure of 1m of liquid helium, so the osmotic pressure will be large enough to drive the $^3$He from the mixing chamber into the still even if they are separated by 1m height difference.
##### Realization of $^3$He-$^4$He Dilution Refrigerators
![[Pasted image 20260116120754.png]]





## References
