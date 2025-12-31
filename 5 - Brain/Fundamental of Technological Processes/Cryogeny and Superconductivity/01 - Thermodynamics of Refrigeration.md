
2025-12-30 12:12

Status: 

Tags:

# Thermodynamics of Refrigeration
##### Cryogenics
Cryogenics is the study of the production and behavior of materials at temperatures below room temperature.
The lowest temperature found in nature is 2.7 K, the temperature of the background radiation of the universe, due to fossil photons from the Big Bang.
In laboratory is now possible to reach temperatures of hundreds of picoKelvin ($10^{-16}$ K).
A small list of important low temperatures is:
- Evaporation of Helium-4: 1.3 K
- Evaporation of Helium-3: 0.3 K
- Dilution of Helium-3 in Helium-4: 10 mK
- Electronic Magnetic Refrigeration: 3 mK
- Nuclear Magnetic Refrigeration: 100 $\mu$K

#### Isentropic Cooling
Isentropic cooling is a thermodynamic process that can be explained through a S-T diagram. In our case $S = S(T, X)$, where $X$ is an external parameter that can be changed to modify the entropy of the system, for example the pressure or the magnetic field.
![[Pasted image 20251231104019.png]]
The entropy of a system at constant volume or pressure generally monotonically increases with temperature.
The isentropic cooling process consists in:
1. Starting from an initial state $A$ at temperature $T_B$ on the external parameter $X_1$.
2. Through isothermal compression (magnetization in case of magnetic refrigeration, where the external parameter is the magnetic field) bring the system to state $B$ at temperature $T_B$ on the external parameter $X_2$.
3. Through adiabatic expansion (demagnetization in case of magnetic refrigeration) bring the system to state $C$ at temperature $T_C < T_B$ on the external parameter $X_1$.
4. Repeat the cycle starting from state $C$, to get to even lower temperatures.

Using this process it is possible to reach very low temperatures, depending on the properties of the material used, but always above the absolute zero for the Third Law of Thermodynamics (which states that it is impossible to reach the absolute zero through a finite number of processes).

This process highlights the syntactic equivalence: cooling $\Leftrightarrow$ ordering $\Leftrightarrow$ entropy reduction.
#### Isenthalpic Cooling
Isenthalpic cooling is a throttling process, meaning that it occurs at constant enthalpy $H$.
We can explain this process through an example of an electric refrigerator for domestic use.
![[Pasted image 20251231105651.png]]
The main components of a refrigerator are:
- Liquid Tank: contains the refrigerant fluid in liquid state at temperature $T_H > T_{ambient}$ and pressure $p_H > p_{ambient}$ (saturated liquid).
- Expansion Valve: a throttling valve that uses adiabatic expansion (Joule-Thomson expansion) to cool the refrigerant fluid at $T_C < T_H$ and there's a partial vaporization of the fluid.
- Evaporator: a heat exchanger that provides latent heat $Q_L$ to the refrigerant fluid from the material or chamber to be cooled, bringing the fluid to saturated vapor state.
- Compressor: compresses the refrigerant fluid, so that is returned to $T_H > T_{ambient}$ and $p_H > p_{ambient}$, 
- Condenser: a heat exchanger that removes latent heat $Q_H$ from the refrigerant fluid to the ambient (air or water), bringing the fluid to saturated liquid state.

The minimum temperature reachable with this type of refrigerator is of the order of $-30 ^\circ C$.
The refrigerant fluid can be any fluid that can perform the thermodynamic cycle described.
The work done on the system is $W = Q_H - Q_C$, where $Q_H$ is the heat removed from the refrigerant fluid to the ambient and $Q_C$ is the heat absorbed by the refrigerant fluid from the material or chamber to be cooled.
![[Pasted image 20251231111144.png]]

This process can also be explained through a V-P diagram.
![[Pasted image 20251231111245.png]]
- State 1: saturated liquid at high pressure $p_1$ and temperature $\theta_H$.
- State 2: after the expansion valve (throttling process) at low pressure $p_2$ and temperature $\theta_C$, with partial vaporization of the fluid.
- State 3: saturated vapor at low pressure $p_2$ and temperature $\theta_C$ after isothermal and isobaric vaporization in the evaporator. In this state we have more volume for the same mass of fluid, so the specific volume $v_3$ is higher than $v_2$.
- State 4: after the compressor (adiabatic compression) at high pressure $p_1$ and temperature $\theta_H$. 

We go back to state 1 after the isothermal and isobaric condensation in the condenser. Where the volume decreases for the same mass of fluid, so the specific volume $v_1$ is lower than $v_4$.
![[Pasted image 20251231112500.png]]

We can calculate the Coefficient of Performance (COP) of the refrigerator as:
$$COP = \frac{Q_C}{W} = \frac{Q_C}{Q_H - Q_C}$$
Which basically measures how much heat $Q_C$ is absorbed from the material or chamber to be cooled for each unit of work $W$ done on the system. A typical value for a domestic refrigerator ranges from 2 to 7.
From this we can see that is convenient to heat a house by cooling the outside air rather than using resistive heating elements, since if for example we have $COP = 5$, for each joule of work done on the system we get 5 joules of heat removed from the house, while with resistive heating elements we would get only 1 joule of heat for each joule of work done.

By reversing the valve, the thermal cycle can be used as a heat pump to heat a house, with the same COP.
![[Pasted image 20251231112943.png]]
##### Refrigerants
Its is important to choose the right refrigerant fluid to adjust the temperature of the cold body and that of the hot reservoir.
The history of refrigerants can be divided into three main generations:
1. First Generation: used toxic and flammable substances like ammonia ($NH_3$), it was very efficient since it had high latent heat of vaporization, but dangerous for human health.
2. Second Generation: used chlorofluorocarbons (CFCs) commercially called Freons, which were non-toxic and non-flammable, but being heavy molecules they caused depletion of the oxygen leading to possible asphyxiation, and also damaged the ozone layer.
3. Third Generation: used hydrofluorocarbons (HFCs) like R-134a, which don't damage the ozone layer, but are powerful greenhouse gases with high global warming potential (GWP) by remaining in the atmosphere for a long time.
##### Throttling Process
The throttling process makes use of a porous wall, which permits the fluid to pass from a chamber to another chamber while controlling the pressure, unlike free expansion.
The process is adiabatic, so no heat exchange occurs with the environment, and it is irreversible due to the presence of friction.
![[Pasted image 20251231114153.png]]
Both pistons are moved at different speeds to the right so that we mantain an higher pressure on the left chamber ($p_i$, where $i $ stands for initial) and a lower pressure on the right chamber ($p_f$, where $f$ stands for final).
The gases pass through the porous wall from the left chamber to the right chamber, in the middle of the process the gas finds itself in a dissipative non-equilibrium state, and finally reaches the final equilibrium state in the right chamber. 
The friction of the chamber walls and of the porous wall causes internal mechanical irreversibilities.

![[Pasted image 20251231122201.png]]
We can easily calculate the throttling process to be isenthalpic, meaning that the enthalpy before and after the process is the same ($H_i = H_f$).
The process is adiabatic, so $Q = 0$, so the only remaining energy exchange is the work done by the system. Bu we can easily see that the sum of the internal energy of the initial system plus the work done by the system is equal to the internal energy of the final system plus the work done on the system.
Even though the initial and final enthalpy are the same, the process is not strictly isenthalpic, since the system passes through a non-equilibrium state in an irreversible process.
A continuous throttling process can be achieved by a pump that maintains a constant pressure difference across a porous plug, allowing the fluid to pass from the high-pressure side to the low-pressure side.
##### Joule-Thomson Expansion
The Joule-Thomson expansion is a particular case of throttling process, where a real gas expands from a high-pressure region to a low-pressure region through a porous plug or valve, it is normally used to liquefy gases and in refrigeration cycles.
The gas undergoes a continuous throttling process, it flows in radial direction through the porous plug from the high-pressure side to the low-pressure side. The throttling valve and the surrounding walls are thermally insulated, so the process is adiabatic.
The process starts from an initial state with pressure $p_i$ and temperature $T_i$, and ends in a final state with pressure $p_f$ and temperature $T_f$. The high-pressure side is chosen arbitrarily while the low-pressure side is set to any desired value $< p_i$. $T_f$ is calculated and can be seen on the isenthalpic curves of the gas.
![[Pasted image 20251231124414.png]]
We can see that lower pressures doesn't always lead to lower temperatures, depending on the initial state of the gas. The isenthalpic curve represents all equilibrium states that can be reached from the initial state through a throttling process.
![[Pasted image 20251231125411.png]]
Starting from different initial states ($p_i$, $T_i$) different isenthalpic curves are obtained. The slope of the isenthalpic curves an any point indicates whether the gas cools down or heats up during the expansion and is called the Joule-Thomson coefficient $\mu$:
$$\mu = \left( \frac{\partial T}{\partial p} \right)_H$$
If $\mu > 0$ the gas cools down during the expansion, if $\mu < 0$ the gas heats up during the expansion. Where $\mu = 0$ indicates the inversion curve, which separates the cooling region from the heating region.
A thermodynamic equation can be obtained starting from the difference in molar enthalpy between the initial and final state:
$$\mu = \frac{1}{C_p} \left[ T \left( \frac{\partial V}{\partial T} \right)_p - V \right]$$
Where $C_p$ is the molar heat capacity at constant pressure, $V$ is the molar volume. This is the equation for real gases, for ideal gases $\mu = 0$ since $V = RT/p$ (meaning that ideal gases don't change temperature during a throttling process).
Cooling by throttling is possible only for real gases, because the temperature change is due to the change in energy of the gas molecules when the average distance between them changes during the expansion (internal work is done by the intermolecular forces).

To have the cooling effect during the Joule-Thomson expansion, the initial $T$ must be below the inversion temperature of the gas. For many gases like air and nitrogen the inversion temperature is above room temperature, so they cool down during the expansion at room temperature. For other gases like hydrogen and helium the inversion temperature is below room temperature ($T_i < 200 K$ for hydrogen and $T_i < 40 K$ for helium), so they heat up during the expansion at room temperature and must be precooled using liquid nitrogen or hydrogen before performing the Joule-Thomson expansion to reach lower temperatures.
Once the gas ha been precooled below its inversion temperature, the optimal pressure for the expansion can be determined by analyzing the isenthalpic curves of the gas.
Normally a counter-current heat exchanger is used to pre-cool the gas before the expansion valve, using the cold gas exiting the low-pressure side to cool the high-pressure gas entering the expansion valve, improving the efficiency of the cooling process. For the heat exchanger to work properly, the opposing stream temperatures must be within the cooling region of the isenthalpic curves, meaning that both streams must have $\mu > 0$ during the heat exchange. The stream must be long and well insulated to have a sufficient speed to cause turbulent flow, improving the heat exchange between the two streams, and they need to be in good thermal contact through a high-conductivity material.
![[Pasted image 20251231130638.png]]
When a steady state is reached, liquid is formed at a constant rate, and the liquid fraction can be calculated from the enthalpy balance of the process:
$$H_i = y H_L + (1 - y) H_f \quad \Rightarrow \quad y = \frac{H_f - - H_i}{H_f - H_L}$$ 

## References
