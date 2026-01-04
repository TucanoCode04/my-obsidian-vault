
2025-12-31 18:06

Status: 

Tags:

# 03 - Properties of Cryogenic Fluids
##### Properties of Cryogenic Fluids
Cryoliquids are important for low temperature applications because they are the simplest and most economical way to achieve and maintain low temperatures. Helium is widely used for temperatures below 10K, either as a final or intermediate cooling stage. 
![[Pasted image 20260104124530.png]]
The most important properties of cryogenic fluids are:
- $T_b$: Boiling point, the temperature at which the fluid transitions from liquid to gas at a given pressure. It defines the available temperature range for cooling applications.
- $L$: Latent heat of vaporization, the amount of heat required to convert a unit mass of the liquid into vapor without changing its temperature. A higher latent heat means more efficient cooling.
- the price and availability of the cryoliquid also play a significant role in its selection for specific applications.
##### Some Common Cryogenic Fluids
- **Liquid Oxygen (LOX)**: is not commonly used for cooling applications due to its reactive nature, when in contact with organic materials, it can cause combustion.
- **Liquid Air**: is a mixture of nitrogen, oxygen, and other gases. It is not commonly used because nitrogen evaporates first(lower boiling point), leaving behind a higher concentration of oxygen, which can be hazardous. For these reasons, air is liquefied and separated into its components before use in cryogenic applications.
- **Liquid Nitrogen ($LN_2$)**: is low cost and so widely used for cooling applications down to 60K. Evaporating oxygen can cause asphyxiation if it displaces the usual 20% of oxygen in the air, so room ventilation is important when using $LN_2$.
#### Liquid Hydrogen 
In liquid hydrogen ($LH_2$), the pair of atoms in each molecule have strong covalent bonds, but the intermolecular forces between the molecules are weak(Van der Waals forces). This, and the large zero-point motion energy of the light hydrogen molecules, results in a very low boiling and melting points.
Hydrogen becomes dangerous in exothermic reactions (meaning they release energy) with oxygen, forming water. This reaction needs more than 4% hydrogen in air to become explosive, so it is used in a closed system with proper ventilation.
It is not widely used since the temperature range between the boiling point of nitrogen(77K) and helium(4.2K) is now accessible with closed-cycle cryocoolers. However, it could return to favor in the future with the emerging hydrogen energy technology.
One of the most important properties of liquid hydrogen is the ortho-para hydrogen conversion. 
The proton $^1H$ has a spin of $l =\frac{1}{2}$, so the two protons in the hydrogen molecule can have their spins aligned (ortho-hydrogen, total nuclear spin $I=1$, with degeneracy of $2I+1=3$, so triplet state) or anti-aligned (para-hydrogen, total nuclear spin $I=0$, singlet state). The lowest energy state of the hydrogen molecule is para-hydrogen, with a difference of 172K, if exposed in temperature, with respect to ortho-hydrogen, so at room temperature, all the states are equally populated, resulting in 75% ortho-hydrogen and 25% para-hydrogen. 
![[Pasted image 20260104170658.png]]
At temperature below 172K, lower energy states are favored, so there is a gradual conversion from ortho to para-hydrogen. This conversion is exothermic, releasing rather large quantities of heat, which can cause significant problems at low or ultra low temperatures>
- If the liquid consists mainly of ortho-hydrogen, it will evaporate rapidly as it converts to para-hydrogen even without any external heat input. To avoid this, one needs to pre-convert the hydrogen to para-hydrogen before cooling, by passing it over a catalyst at low temperatures, like iron oxide or ferric hydroxide.
- Many metals, such as Cu, Ag, and Pt, may contain bubbles of dissolved hydrogen of diameter around $0.1 \mu m$, produced during purification processes. The conversion from ortho to para-hydrogen in these bubbles can then give rise to heat release limiting refrigeration at very low temperatures. 
#### Liquid Helium
The most common stable isotope of helium is $^4He$, which has two protons and two neutrons, each with antiparallel spins, resulting in a total nuclear spin of $l=0$, making it a boson. There is also a rare isotope, $^3He$, which has two protons and one neutron, resulting in a total nuclear spin of $l=\frac{1}{2} + \frac{1}{2} - \frac{1}{2} = \frac{1}{2}$, making it a fermion. Their different characteristics lead to different physical properties, especially at low temperatures. $^3He$ is much more expensive because it is a by-product of the decay of tritium, used in nuclear weapons.
##### Important Properties of the Two Isotopes
![[Pasted image 20260104171216.png]]

##### Other Peculiarities of $^4He$ and $^3He$
They have very weak intermolecular forces, since they are noble gases with closed electron s-shells, resulting in absence of static dipole moments. This leads to smallest atomic polarizability among all elements, the dielectric constants are $\epsilon_r = 1.057$ for $^4He$ and $\epsilon_r = 1.042$ for $^3He$ at their boiling points. This also results in very low boiling and melting points.

Due to their small atomic mass, they have large zero-point motion energies, $E_0= \frac{\hbar^2}{8 m a^2}$, where $a$ is the radius of the potential well created by the intermolecular forces, $a = \frac{V_m}{N_A}^{1/3}$, with $V_m$ the molar volume and $N_A$ Avogadro's number. The large energy gives rise to a zero-point vibration amplitude which is about $\frac{1}{3}$ of the interatomic distance, preventing solidification at his own vapor pressure, even at absolute zero. To solidify helium, an external pressure of at least 25 bar for $^4He$ and 30 bar for $^3He$ is required at low temperatures.
![[Pasted image 20260104172553.png]]
The first graph shows the total energy as the sum of the potential energy due to intermolecular forces and the the zero-point energy due to quantum effects. 
The second graph shows the total energy in function of volume, the minimum corresponds to the equilibrium molar volume. The large zero-point energy for the liquid phase results in a larger equilibrium volume for the liquid than for the solid, leading to the unusual property of helium expanding upon solidification.

Due to its smaller mass, $^3He$ has a larger zero-point energy than $^4He$, resulting in lower density, smaller boiling and melting points, and larger vapor pressure at a given temperature.

They are called quantum fluids.

**Phase Diagrams of $^4He$ and $^3He$**
![[Pasted image 20260104171732.png]]
##### Latent Heat and Vapor Pressure
Latent heat of vaporization and vapor pressure are important properties for cryogenic fluids used in cooling applications.
Due to Zero-point energy effects, helium has a a relatively low latent heat of vaporization compared to other cryogenic fluids. This effect is more pronounced in $^3He$ due to its larger zero-point energy. The small $L$ values limit the efficiency of helium as a cryogenic coolant, because it is very easy to vaporize it, so they require shielding against heat introduction from the environment.
![[Pasted image 20260104174314.png]]
In the latent heat diagram of $^4He$, there is a sharp peak at the lambda point (2.17K), which is the temperature at which helium transitions from normal fluid (He I) to superfluid (He II). This peak is due to the unique thermodynamic properties of superfluid helium, which has extremely high heat capacity and thermal conductivity.

The vapor pressure can be derived from the Clausius-Clapeyron equation:
$$\left(\frac{dP}{dT} \right)_{vap}= \frac{S_{gas} - S_{liq}}{V_{m, gas} - V_{m, liq}} $$
Where $S$ is the entropy the entropy and $V_m$ is the molar volume. Since the molar volume of the gas is much larger than that of the liquid so $V_{m, gas} >> V_{m, liq}$,, that $\Delta S_{gas, liq} = \frac{L}{T}$ and that for for Helium $V_{m, gas} = \frac{R T}{P}$, we can approximate the equation as:
$$\left(\frac{dP}{dT} \right)_{vap}= \frac{L P}{R T^2} \quad \Rightarrow \quad P_{vap} \propto e^{-\frac{L}{R T}} $$
If we further approximate $L$ as constant over small temperature ranges, we can see that the vapor pressure increases exponentially with temperature, which implies that even small increases in temperature can lead to significant increases in vapor pressure. This is particularly important for helium, as its low latent heat of vaporization means that it can vaporize easily, leading to rapid pressure increases in cryogenic systems if not properly managed.
![[Pasted image 20260104175034.png]]

One can pump on the vapor phase of liquid helium to lower its pressure and thus its boiling point. By pumping away atoms from the vapor phase, the most energetic atoms will replenish the vapor phase, lowering the average energy of the liquid phase, thus lowering its temperature. This technique is commonly used to achieve temperatures below the normal boiling point of helium (4.2K at 1 atm). By reducing the pressure above the liquid helium, one can reach temperatures as low as 1K or even lower with additional cooling methods.
For a pumped-on helium bath, the cooling power $\dot{Q}$ can be calculated as:
$$ \dot{Q} = \dot{n} L $$ Where $\dot{n}$ is the particle per second being removed from the liquid phase to the vapor phase, and $L$ is the latent heat of vaporization at the reduced pressure.
With a pump with constant volumetric flow rate $\dot{V}$, the particle flow rate is proportional to the vapor pressure $P_{vap}$ and inversely proportional to the temperature $T$, giving a cooling power of:
$$ \dot{Q} \propto P_{vap} L \propto e^{-\frac{1}{T}} $$
As the temperature decreases, the vapor pressure drops exponentially so pumping becomes less effective at lower temperatures, limiting the minimum achievable temperature through this method alone. 
Eventually, there's a practical limit to how low the temperature can be reduced by pumping on the vapor phase, due to the absence of vapor. This is reached when the refrigeration power $\dot{Q}$ equals the heat leak into the system from the environment. At this point, further pumping will not lower the temperature any further, as the heat being removed by vaporization is balanced by the heat entering the system.
Other advantages of the temperature dependence of vapor pressure are:
- cryopumping: the ability to trap gases on cold surfaces, useful in vacuum systems.
- vapor-pressure thermometers: using the known relationship between vapor pressure and temperature to measure low temperatures accurately. The helium vapor pressure curve is often used as a standard for low-temperature measurements.
![[Pasted image 20260104185346.png]]
##### Specific Heat
The specific heat of liquid helium is large compared to other cryogenic fluids, meaning that it can absorb a significant amount of heat with only a small increase in temperature. This property is particularly important in applications where temperature stability is crucial, in fact in low temperature apparatus, the thermal behavior is often dominated by the properties of liquid helium rather than the solid materials used in the construction.
Moreover, the latent heat of vaporization of helium is large compared to the specific heat of other materials at low temperatures, making it an efficient coolant for removing heat from systems operating at cryogenic temperatures.
Both properties result in the temperature of any experiment following the temperature of the liquid helium bath very closely, providing a stable and uniform thermal environment.
![[Pasted image 20260104190250.png]]

The specific heat of $^4He$ shows a sharp peak at the lambda point (2.17K), where helium transitions from normal fluid (He I) to superfluid (He II), called the lambda transition. This peak decreases with increasing pressure, shifting to $T_\lambda  = 1.77K$ at the melting line.
Above the lambda point, $^4He$ behaves like a normal liquid, almost like a classical gas due to its low density, with specific heat decreasing with temperature. Below the lambda point, in the superfluid phase, the specific heat and entropy decrease rapidly with temperature, due to its condensation in momentum space (Bose-Einstein condensation).
Between 1 and 2K, the specific heat has a strong temperature dependence, due to the roton excitations in the superfluid phase (which are quantized vortices in the fluid). Below 0.5K, the specific heat follows a $T^3$ dependence, characteristic of phonon excitations in the superfluid, as for an insulating Debye solid.
![[Pasted image 20260104190829.png]]

The other isotope, $^3He$, being a fermion, must obey Fermi-Dirac statistics. It has has many properties in common with conducting electrons in metals, such as specific heat proportional to temperature at low temperatures, due to the Pauli exclusion principle limiting the number of accessible states for excitations near the Fermi surface.
Since they are Fermi particles they cannot condense into a single quantum state like bosons, since no two fermions can occupy the same quantum state simultaneously (as we know two fermions have half-integer spins, resulting in antisymmetric wavefunctions under particle exchange, which leads to the Pauli exclusion principle that forbids multiple fermions from occupying the same quantum state). However, at very low temperatures (below 2.4 mK for $P= P_{melting}$), $^3He$ undergoes a transition to a superfluid phase through the formation of Cooper pairs, similar to the mechanism in superconductors. In this phase, pairs of $^3He$ atoms behave like bosons and can condense into a single quantum state, resulting in superfluidity with unique properties such as zero viscosity and quantized vortices.
![[Pasted image 20260104191308.png]]

##### Transport Properties of Liquid $^4He$
Liquid $^4He$ above the lambda point (He I) behaves like a normal fluid, it exhibits low thermal conductivity and viscosity, similar to other liquids. Due to its low thermal conductivity, there will be non uniform temperature distributions in He I, so the boiling process will be less efficient and it will create temperature gradients in the liquid, producing bubbles and turbulence.
![[Pasted image 20260104193535.png]]
Below the lambda point (He II), under ideal condition of heat flow $

## References
