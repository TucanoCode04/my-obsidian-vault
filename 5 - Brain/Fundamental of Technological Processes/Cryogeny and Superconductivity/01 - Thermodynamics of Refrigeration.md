
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
- Expansion Valve: a throttling valve that uses adiabatic expansion to cool the refrigerant fluid at $T_C < T_H$ and there's a partial vaporization of the fluid.
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



## References
