
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
A perfect black body is defined as an object that absorbs all incident radiation, regardless of frequency or angle of incidence. Its absorptivity (α), emissivity (ε), and reflectivity (ρ) satisfy the relation:
$$\alpha + \epsilon + \rho = 1$$
At temperature T, a black body emits radiation according to the Stefan-Boltzmann law:
$$E_b = \sigma T^4$$
where σ is the Stefan-Boltzmann constant, approximately equal to 5.67 x 10^-8 W/m^2K^4. Such energy is emitted over a spectrum of wavelengths, with the peak wavelength determined by Wien's displacement law:
$$\lambda_{max} T = b$$
where b is Wien's displacement constant, approximately equal to 2.898 x 10^-3 mK.
![[Pasted image 20260105163106.png]]

Most non-metallic surfaces have high emissivity values (0.8 to 0.9), so they can be approximated as black bodies. Metals, however, tend to have lower emissivity values (0.02 to 0.2), depending on the wavelength of the incident radiation and the physical condition of the surface (e.g., polished vs. oxidized). For example, Cu oxid has an emissivity of about 0.6, for wavelengths around 10 μm, while polished for the same wavelength has an emissivity of about 0.02.
![[Pasted image 20260105163349.png]]

For two planes parallel to each other, with area A, at temperatures T1 and T2, and with emissivities ε1 and ε2, the heat transfer per unit time due to radiation is given by:
$$\dot{Q} = \sigma A (T_1^4 - T_2^4) \frac{\epsilon_1 \epsilon_2}{\epsilon_1 + \epsilon_2 - \epsilon_1 \epsilon_2}$$Hence, if they have equal emissivities ε and it are much less than 1, the equation simplifies to:
$$\dot{Q} = \sigma A (T_1^4 - T_2^4) \frac{\epsilon}{2}$$

Radiation shields are commonly used in cryogenic systems to reduce radiative heat transfer. These shields are typically made of polished metal, like copper, kept at temperature between the environmental temperature and the cryogenic bath, or multilayers, like aluminized Mylar, inserted in vacuum spaces to reflect radiation.
![[Pasted image 20260105163849.png]]

To reduce heat inflow we introduced even thermal radiation baffles, which are structures placed between two surfaces to block direct line-of-sight radiation. These baffles can be made of highly reflective materials and are often cooled to intermediate temperatures to further reduce heat transfer.
![[Pasted image 20260105164038.png]]
##### Other Causes of Heat Transfer
![[Pasted image 20260105164306.png]]

##### Example of Heat Transfer Calculation
![[Pasted image 20260105164338.png]]

##### Material Selection with Appropriate Cryogenic Thermal Conductivity




## References
