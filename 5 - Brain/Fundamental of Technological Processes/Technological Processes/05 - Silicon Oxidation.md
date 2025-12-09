
2025-12-09 00:21

Status: 

Tags:

# Silicon Oxidation
#### Thermal Oxidation of Silicon
It allows for the formation of SiO2 layers when silicon wafers are exposed to oxidizing environments like dry oxygen (O2) or steam (H2O) at elevated temperatures (typically between 800°C and 1200°C) or starting from a polysilicon film.
So there are 3 main conditions for silicon oxidation:
- Oxidizing ambient (dry O2 or steam H2O)
- High temperature (800-1200 °C)
- Silicon exposed surface

By thermal oxidation we can create layers of 30 Armstrong to several micrometers thick. Other configurations are not used since either too thin layers are formed or the process is too slow as we can see in the figure below.
![[Pasted image 20251209163654.png]]
The most important usages of silicon oxidation are:
- electrical insultation: used ad insulator in pn junctions, MOS capacitors and MOSFETs
- masking layer: used as a mask during doping or etching processes
- thermal insulation: used to reduce heat flow in MEMS devices
- sacrificial layer: used in Surface Micromachining to create suspended structures to make them vibrate or bend

Silicon Oxide can also be made through Chemical Vapor Deposition (CVD) or Physical Vapor Deposition (PVD) but these methods produce layers with inferior electrical and mechanical properties compared to thermal oxidation.

Silicon in mostly used, even though other superconductors have better properties, as one of the reasons because Silicon Oxide is easy to form and has excellent insulating properties.

Silicon Oxide naturally forms onto silicon surfaces when exposed to air, creating a thin native oxide layer (approximately 1-2 nm thick) that can affect the electrical properties of silicon devices. We normally remove this native oxide layer because we want to have better control over the oxide thickness and quality for device fabrication.
##### Silicon Dioxide Properties
Silicon Oxide is an amorphous material with a short range order of tetrahedral SiO4 units. Some important properties of silicon dioxide are:
![[Pasted image 20251209164812.png]]
Its atomic density is half that of silicon, which means that when silicon oxidizes, the resulting SiO2 layer is thicker than the original silicon consumed. Specifically, for every unit thickness of silicon consumed, approximately 2.17 units of SiO2 are formed. This expansion must be considered during device fabrication to ensure proper dimensions and functionality.

Silicon can also be crystalline in the form of quartz, which is used as a digital frequency reference due to its piezoelectric properties(digital clocks).
##### Silicon Oxidation 
We need the 3 main conditions mentioned above to have silicon oxidation. The process can be done in 2 different ways:
1. Dry Oxidation: $Si + O_2 \rightarrow SiO_2$
2. Wet Oxidation: $Si + 2H_2O \rightarrow SiO_2 + 2H_2$

Silicon is consumed during the process, this is not a deposition process. 
![[Pasted image 20251209182514.png]]
The oxide layer will be formed at the Si/SiO2 interface, meaning that as water or oxygen molecules diffuse through the already formed oxide layer, they will react with silicon at the interface to form more SiO2, so that the oxide layer grows thicker from within.
This is also why the process slows down as the oxide layer gets thicker, since the diffusion of oxidizing species through the oxide layer becomes more difficult.
![[Pasted image 20251209182525.png]]
The Silicon Oxide will then be almost 50% inside the original silicon wafer and 50% above it, this is because of the molecular densities of Si and SiO2(to explain it better, since the ratio between the 2 molecular density is of 0.44, for every 1 nm of Si consumed, 2.27 nm of SiO2 will be formed, so 1 nm will be inside the original Si wafer and 1.27 nm will be above it).

The equipment used for thermal oxidation is a quartz tube furnace, where silicon wafers are placed inside a quartz boat and inserted into the furnace tube. The furnace is then heated to the desired temperature, and the oxidizing ambient (dry O2 or steam) is introduced into the tube to initiate the oxidation process through some inlets.
The first and last wafers in the boat may experience different oxidation rates due to variations in gas flow and temperature distribution, so they are used as dummy wafers and not for actual device fabrication.
![[Pasted image 20251209182753.png]]

The oxidation rate can vary depending on the crystallographic orientation of the silicon wafer. For example, 111 oriented wafers tend to oxidize faster since they have more atoms on the surface so more dangling bonds are available to react with the oxidizing species(1.7 times faster than 100 oriented wafers).
Even the average grain size in polycrystalline silicon can affect the oxidation rate, with smaller grains leading to faster oxidation due to the increased number of grain boundaries that can act as diffusion paths for oxidizing species.

**Some key variables in Oxidation**
![[Pasted image 20251209193520.png]]
##### Thermal Oxidation Model
The Deal-Grove model is the most widely used model to describe the kinetics of silicon oxidation. It provides a mathematical framework to predict the oxidation rate over time and the final oxide thickness based on process parameters.
$$\frac{\partial x_{ox}(t)}{\partial t} , \quad x_{ox}(t) = \text{oxide thickness at time t}$$
As we stated before thermal oxidation is a diffusion limited problem, so the growth rate of the oxide layer is determined by the diffusion of oxidizing species through the existing oxide layer to the silicon interface.
The model describes 3 fluxes:
1. Flux of oxidizing species from the ambient to the oxide surface: $F_1$
2. Flux of oxidizing species through the oxide layer to the Si/SiO2 interface: $F_2$
3. Flux of oxidizing species reacting at the Si/SiO2 interface: $F_3$
At steady state, these fluxes are equal: $F_1 = F_2 = F_3$, meaning that the rate of oxidizing species reaching the oxide surface, diffusing through the oxide layer, and reacting at the interface are all the same. This condition is not valid as soon as you turn on the oven, but after a short transient time.
Each flux is calculated as: $F = \frac{\text{number of particles}}{\text{area} \cdot \text{time}}$
The gradient of concentration is negative from the surface to the interface, from $N_0$ to $N_i$(concentration at the surface and interface respectively).
![[Pasted image 20251209194437.png]]
From the statements above we derive Fick's first law of diffusion:$$J = F_2 = -D \frac{\partial N}{\partial x} = D \frac{N_0 - N_i}{x_{ox}(t)}$$Where:
- $N_0$: concentration of oxidizing species at the oxide surface, which is $5.2 \times 10^{16} \text{ molecules/cm}^3$ for dry oxidation at 1000 °C and 1 atm pressure and $3 \times10^{19} \text{ molecules/cm}^3$ for wet oxidation at 1000 °C and 1 atm pressure.
- $D$: diffusion coefficient of the oxidizing species in the oxide layer $\frac{cm^2}{s}$, which is a constant of proportionality between the flux and the concentration gradient. 

If we combine Fick's law with the reaction rate at the Si/SiO2 interface:
$$J = F_3 = k_s N_i$$
Where:
- $k_s$: reaction rate constant at the Si/SiO2 interface $\frac{cm}{s}$

And considering that at steady state $F_2 = F_3$, and substituting $N_i$ from the second equation into the first one, we get:
$$J = \frac{D N_0}{x_{ox}(t) + \frac{D}{k_s}}$$

The constant $k_s$ represents the reaction speed at the Si/SiO2 interface, so it accounts for a lot of other factors such as:
- Temperature
- Silicon Solid State(crystalline or amorphous)
- Crystallographic orientation
- Oxidant molecules
- Surface contamination
- Doping

We introduce the term $N_{ox}$, which is the number of oxidant molecules required to form a unit volume of SiO2, which is>
- $2.2 \times 10^{22} \text{ molecules/cm}^3$ for dry oxidation, since each SiO2 molecule requires 1 O2 molecule
- $4.4 \times 10^{22} \text{ molecules/cm}^3$ for wet oxidation, since each SiO2 molecule requires 2 H2O molecules

The growth rate of the oxide layer can be expressed as:
$$\frac{\partial x_{ox}(t)}{\partial t} = \frac{J}{N_{ox}} = \frac{D N_0}{N_{ox} \left( x_{ox}(t) + \frac{D}{k_s} \right)}$$
Which describes the ratio between the available oxidizing species flux at the interface and the number of oxidizing species required to form a unit volume of SiO2. Flux/concentration gives us a velocity, which is the growth rate of the oxide layer.
It's a differential first order equation in time, so we can just force an initial condition for the oxide thickness at time t=0:
$$x_{ox}(0) = x_i$$Where $x_i$ is the initial oxide thickness, which can be 0 if we start from bare silicon or a small value if we have a native oxide layer.
So the general relation for silicon oxidation is:
$$\frac{x_{ox}(t)^2}{B} + \frac{x_{ox}(t)}{\frac{B}{A}} - (\tau + t) = 0$$Where:
- $B = \frac{2 D N_0}{N_{ox}}$: parabolic rate constant $\frac{cm^2}{s}$
- $A = \frac{2 D}{k_s}$: linear rate constant $cm/s$
- $\tau = \frac{x_i^2}{B} + \frac{x_i}{\frac{B}{A}}$: time correction factor $s$ to account for initial oxide thickness
- t: oxidation time $s$

The final solution is given by:
$$x_{ox}(t) = \frac{1}{2} A\left[\left(\sqrt{1 + \frac{4 \cdot B}{A^2} (t + \tau)}\right) - 1\right]$$

Wet Oxidation is typically faster than Dry Oxidation, but the quality of the oxide layer produced is lower, since Hydrogen can get trapped or create holes in the oxide layer. For this reason, we normally use a 3 step process:
1. Dry Oxidation to create a thin, high-quality oxide layer 
2. Wet Oxidation to quickly grow the oxide layer to the desired thickness
3. Dry Oxidation again to create a high-quality surface layer

![[Pasted image 20251209201549.png]]
111 oriented wafers oxidize faster than 100 oriented wafers, we can see it from the graph since it starts from a higher thickness at the same time.

![[Pasted image 20251209201756.png]]
This graph demonstrates accounting for $\tau$, for example by following the first process we end up with a thickness of 190 nm, so the second process will start from that thickness, keeping in mind the temperature and type of oxidation used. So we go basically to the gray dot following the line, till the new red dot.
##### Growth Rate Regimes


##### Rapid Thermal Oxidation (RTO)
It is use
## References
