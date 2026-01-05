
2026-01-04 19:52

Status: 

Tags:

# 04 - Thermal Contact and Thermal Isolation
When designing systems that involve heat transfer, understanding thermal contact and thermal isolation is crucial. A general treatment of thermal conductivity is necessary to optimize performance and ensure safety, contact resistance, and insulation properties.
#### Heat Transfer 
Heat transfer occurs through three primary mechanisms: conduction, convection, and radiation. In low temperature environments, convection is often minimized, due to the evacuation of air or other gases to achieve thermal isolation. Thus, heat transfer is primarily through:
- conduction through residual low pressure gases,
- conduction through solid materials in contact,
- radiation 
Other factors may be Joule heating from electrical components, eddy current heating from changing magnetic fields, mechanical vibrations, absorption of gases, etc.
##### Conduction Through Low Pressure Gases
The residual gas pressure in a cryostat is reduced to the point where the mean free path of gas molecules is similar to the dimensions of the system. In this regime, the thermal conductivity of the gas depends on the number of molecules present and their average speed, since they can travel significant distances without colliding.  For approximately parallel surfaces of equal area A at temperatures T1 and T2, the heat transferred by conduction through the gas is given by:
$$\dot{Q} = \text{constant} \cdot A \cdot \alpha \cdot p(T_2- T_1)$$
where p is the gas pressure and α is the accommodation coefficient, which is the fraction of gas molecules that equilibrate to the surface temperature upon collision, and the constant depends on the gas species (specific data on the slides).
##### Conduction Through Solid Materials 
The heat transfer through a solid of cross section A under a temperature gradient is given by Fourier's law:
$$\dot{Q} = -\kappa A\frac{dT}{dx}$$
where k is the thermal conductivity of the material, which can vary significantly with temperature, especially at cryogenic temperatures. The negative sign indicates that heat flows from higher to lower temperatures. If the end temperatures T1 and T2 are known, the equation can be integrated to give:
$$\dot{Q} = \frac{A}{L} \int_{T_1}^{T_2} \kappa(T) dT$$
where L is the length of the solid through which heat is conducted.
![[Pasted image 20260105155940.png]]

Dielectric materials, metals, alloys, glasses and polymers are subject to  phononic and electronic mechanisms of heat conduction. Heat, in fact, can be carried by lattice vibrations (phonons) and free electrons. 
These carriers do not move ballistically from the hotter to the colder side, but rather scatter with each other and with defects in the material. To capture this behavior, we use transport theory, where we see electrons and phonons as a kinetic gas diffusing through the material. The thermal conductivity can then be expressed as:
$$\kappa \approx c \cdot v \cdot \lambda$$ Where c is the specific heat per unit volume of the carriers, meaning what amount of energy is transported per unit volume per degree of temperature change, v is the average velocity of the carriers performing the transport, and λ is the mean free path between scattering events, meaning how far the carriers can travel before being scattered.
The main scattering events are:
- at low T: scattering from defects and impurities, constant with T
- at intermediate T: scattering from thermally excited phonons, increasing with T
As a result we find a maximum in thermal conductivity at some intermediate temperature, which depends on the material purity and defect density.
![[Pasted image 20260105160832.png]]

![[Pasted image 20260105160923.png]]
At very low temperatures(T < 1 K), thermal conductivity is linearly proportional to T, very high for pure metals, like copper, to about 7 orders of magnitude lower for graphite and teflon.
As we said before $\kappa$ depends on purity and defect density. In literature, thermal conductivity data is often reported for different RRR values (Residual Resistivity Ratio), which is the ratio of electrical resistivity at room temperature to that at 4 K. It is used since the correct measurement of thermal conductivity at cryogenic temperatures is challenging, while electrical resistivity is easier to measure. Higher RRR values indicate higher purity and lower defect density, leading to higher thermal conductivity at low temperatures.
In a metal both conductivities are related by the Wiedemann-Franz law, since they are determined by the flow of electrons and their scattering mechanisms are similar.
$$\frac{\kappa}{\sigma}= L \cdot T$$
where L is the Lorenz number, approximately equal to 2.44 x 10^-8 WΩK^-2. Thus, by measuring electrical resistivity, we can estimate thermal conductivity using this relationship.
For practical cryogenic design, the effective heat conductance of a solid bar with certain end temperatures T1 and T2 can be calculated using:
$$\overline{\kappa} = \frac{1}{T_2 - T_1} \int_{T_1}^{T_2} \kappa(T) dT$$
![[Pasted image 20260105161850.png]]
##### Radiation


## References
