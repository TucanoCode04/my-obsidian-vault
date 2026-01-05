
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
![[Pasted image 20260105170418.png]]

#### Heat Switches
Heat switches are devices used to connect and disconnect thermal paths in cryogenic systems. 
##### Gaseous Heat Switches
Gaseous heat switches are used to thermally couple components by introducing a gas into a vacuum space. When the gas is present, it increases thermal conductivity, allowing heat transfer. When the gas is evacuated by pumping, the thermal conductivity drops significantly, effectively isolating the components. This method is often used in pre-cooling stages of cryogenic systems.
Even low pressures of gas can significantly increase thermal conductivity, but they will require longer pump-down times to achieve high vacuum levels, which can be a drawback because of the time dependent heat leaks due to a continuous desorption and condensation of gases on cold surfaces.
For $^4$He the superfluid film flow contributes to heat transfer too.
##### Mechanical Heat Switches
Thermal contact is achieved by physically bringing two components into contact and pressing them together using a mechanical mechanism. The disadvantages are that these systems require large forces to achieve good thermal contact, and the heat generated during the switching process can be significant.
They are adequate for temperatures above 1 K.
![[Pasted image 20260105172449.png]]
##### Superconducting Heat Switches
The thermal conductivity of a superconductor drops exponentially with temperature below its critical temperature (Tc) due to the formation of Cooper pairs, which do not contribute to heat conduction, and the number of quasiparticle excitations decreases significantly. It can be of several orders of magnitude lower than that of its normal state.
Some material can be easily switched between superconducting and normal states by applying a magnetic field or heating. This allows for a thermal switch that can be controlled without mechanical movement, they are used for temperatures below 1 K.
One of the main advantages is that the heat flow in the open state is very low, since the thermal conductivity in the superconducting state is extremely low, so they are easy to switch off. The switching ratio $\frac{\kappa_{normal}}{\kappa_{superconducting}}$ can be very high for $T << T_c$. In fact $\kappa_{normal} \propto T$ while $\kappa_{superconducting} \propto e^{-\frac{\Delta}{k_B T}}$ where Δ is the superconducting energy gap, for T > Tc/10. While for T < Tc/10 the thermal conductivity is dominated by phonons and follows a T^3 dependence.
Al is a good candidate for superconducting heat switches, since it has high $\kappa_{normal}$ and large $\theta_D$ (Debye temperature), and it is extremely pure, and has a convenient critical field of about 10 mT. It also has good durability and it's easy to handle, the only problem is the surface oxide layer that can increase thermal contact resistance.
There can be problems when switching the field due to magnetic flux trapping, which can lead to incomplete transitions between superconducting and normal states, reducing the effectiveness of the heat switch. To mitigate this, the metal part of the switch is perpendicularly oriented to the applied magnetic field, so that the normal cores of the trapped flux lines will not short-circuit the heat flow.
![[Pasted image 20260105173538.png]]
#### Thermal Boundary Resistance
##### Boundary Resistance Between Metals
Thermal equilibrium is more difficult to achieve in a system when the temperature is low, not only for the decreasing of thermal conductivity of materials, but also because of the thermal boundary resistance (or Kapitza resistance) that arises at the interface between two materials. 
If we have two material in contact and a heat flow $\dot{Q}$ across the interface, the temperature step ΔT at the interface is proportional to the heat flow:$$\Delta T = R_K \cdot \dot{Q}$$ where $R_K$ is the Kapitza resistance.
For metals, the actual contact area is much smaller than the apparent contact area, due to surface roughness and asperities. $R_K$ scales inversely with the actual contact area, we can improve thermal contact by increasing the contact pressure.
![[Pasted image 20260105174022.png]]

The boundary or Kapitza resistance can be kept small if the surfaces are clean, gold-plated, and pressed together with high force, so that we have an overlap of the electronic wave functions across the interface, allowing efficient electron transport, and so electrical and thermal flow.
We achieve extremely low thermal boundary resistance between gold-plated Cu surfaces bolted together with stainless steel bolts (the contact resistance is inversely proportional to the tightening torque of the bolts), in the range of $0.1 - 10 \mu \Omega$ at 4K.
The addition of Indium foil or Apiezon N grease can further reduce the thermal boundary resistance by filling in microscopic gaps and improving contact area.
Mechanical and electrical contact is usually achieved by soldering, but unfortunately the most used solders become superconducting at low temperatures, which are good for electrical contact, but bad for thermal contact, since the thermal conductivity drops significantly in the superconducting state.
![[Pasted image 20260105174615.png]]

##### Boundary Resistance Between Liquid Helium and Solids
Between dielectrics and Helium, the energy transfer occurs only via phonons, since there are no free electrons in dielectrics. A temperature discontinuity arises at the interface due to the mismatch in acoustic properties between the two materials, leading to a Kapitza resistance.
For helium/solid interfaces, the acoustic mismatch is of three orders of magnitude, $\rho_s v_s\approx 10^6 g cm^{-2} s^{-1}$ for solids, and $\rho_{He} v_{He} \approx 10^3 g cm^{-2} s^{-1}$ for liquid helium, where ρ is the density and v is the velocity of phonons in the material.
![[Pasted image 20260105175032.png]]

Hence the acoustic mismatch and a small critical angle for phonon transmission at the interface lead limits the energy exchange between liquid helium and solids at low temperatures.
It's Kapitza resistance scales as:
$$R_K \propto (T^3 A)^{-1}$$
where A is the contact area. Most experimental data for 0.02K < T < 0.2K typical values are $AR_K T^3 \approx 10^{-2} m^2 K^4 W^{-1}$ for liquid He in contact with Cu or Ag.
The most efficient way to reduce Kapitza resistance at these interfaces is to increase the contact area using sintered metal powders.

So basically the Kapitza resistance problem can be divided into three regimes:
1. At temperatures above 1 K, the Kapitza resistance is the same for liquid and solid $^4$He and $^3$He, orders of magnitude smaller than predicted, we don't know why.
2. Between 20 mK and 200 mK, the Kapitza resistance follows the expected T^-3 dependence, and the values are consistent with the acoustic mismatch model.
3. Below 20 mK, the Kapitza resistance approaches $T^{-2}$ or even $T^{-1}$ dependence, possibly due to magnetic dipole coupling between the $^3$He nuclear moments and electrons in the solid, together with a coupling of helium phonon modes to soft vibrational modes in the solid. 

## References
