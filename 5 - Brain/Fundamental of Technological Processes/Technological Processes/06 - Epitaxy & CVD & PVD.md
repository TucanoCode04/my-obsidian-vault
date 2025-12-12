
2025-12-10 17:32

Status: 

Tags:

# 06 - Epitaxy & CVD & PVD
#####  Epitaxy
Epitaxy is a deposition technique used to grow a monocrystalline layer on a monocrystalline substrate, where the deposited layer follows the crystallographic orientation of the substrate. The requirements for epitaxial growth are:
- the substrate must be monocrystalline to act as a seed for the growth of the epitaxial layer
- the crystallographic structure and lattice parameters of the substrate and the deposited layer must be similar to minimize lattice mismatch and defects(maximum mismatch of 2-3%)
Epitaxy can be classified into two main types:
- Homoepitaxy: the deposited layer is made of the same material as the substrate(ex: Si on Si)
- Heteroepitaxy: the deposited layer is made of a different material than the substrate(ex: GaAs on Si, they are both cubic but have different lattice constants)
![[Pasted image 20251212120122.png]]
Epitaxial techniques can be further divide according to the characteristics of the Mother Phase, the reactor in which the epitaxial growth takes place:
- Vapor Phase Epitaxy (VPE): the precursor materials are in the vapor phase(gas or vaporized liquids). It's a simple technique and it's the most used for Si epitaxy, it can't be used for all materials since not all materials can be vaporized easily.
- Liquid Phase Epitaxy (LPE): the precursor materials are in the liquid phase(molten). It allows for high growth rates and good crystal quality, but it's limited to materials that can be melted without decomposition.
- Molecular Beam Epitaxy (MBE): the precursor materials are again gas phase, but the growth occurs in ultra-high vacuum conditions. The molecules or atoms are so rarified that their mean free path is very long, so that collisions between them are negligible. It allows for precise control over the growth process and the ability to create complex structures with atomic layer precision, but it's expensive and slow.

Why do we use epitaxy?
- to add a lightly doped layer on top of a heavily doped substrate to increase the breakdown voltage(meaning the maximum voltage that can be applied before the material becomes conductive), this is inversely proportional to the doping concentration since higher doping means more free carriers that can conduct current. For example in power devices like diodes and transistors, we want a high breakdown voltage to handle high voltages without failure.
- to create layers with opposite doping types on a substrate, for example a pn junction is a conductive diode when negative voltage is applied to the n side and positive to the p side, allowing current flow, and non conductive when the voltage is reversed. 
- to create buried doped layers in a substrate, by growing an epitaxial layer on top of a doped substrate, we can create a buried layer with specific electrical properties.
- to create a low roughness(mirrorlike, few nm) surface for subsequent processing steps, since epitaxial layers can have very low surface roughness, which is important for high-quality device fabrication. So you can grow an epitaxial layer of the same material as the substrate to create a smooth surface.
- to create heterostructures with specific electrical and optical properties, by growing layers of different materials on a substrate, we can engineer the band structure and other properties of the resulting heterostructure for applications in optoelectronics and high-speed electronics. As we know the doping distribution has a gaussian profile, but with epitaxy we can create abrupt junctions with sharp doping transitions, step like profiles.
- to create strained layers to modify the material properties, by growing a layer with a different lattice constant than the substrate, we can induce strain in the epitaxial layer, which can alter its electronic and optical properties.
![[Pasted image 20251212121909.png]]
This graph shows additionally to the requirements listed before to achieve epitaxial growth, the grow rate in function of the temperature(in this case the high temperature is on the left side). If we stay above the line we have polycrystalline growth, while below it we have monocrystalline growth, so if we want the latter we need to moderate the temperature and the growth rate.
#### Vapor Phase Epitaxy (VPE)
![[Pasted image 20251212122240.png]]
VPE is a technique where the precursor materials are in the vapor phase, typically as gases or vaporized liquids, made using bubbler systems. The process is carried out in a quartz reactor with a wafer holder made of graphite or silicon carbide(SiC) to withstand high temperatures(up to 1200°C) and RF induction coils that heat the reactor and the wafers.
Thanks to the high temperatures, the precursor gases molecules decompose on the wafer surface, where they migrate to the position where they minimize their energy, forming a monocrystalline layer that follows the crystallographic orientation of the substrate(for example they find a vacancy in the lattice and fill it). 
We use different precursors for different uses, the reaction chamber can be even used for doping by introducing dopant gases in the chamber.
The chamber's walls are maintained at a lower temperature than the wafers to avoid unwanted deposition on the walls that could contaminate subsequent processes.

To list some properties of the gases used in epitaxy: 
- corrosive to the equipment
- toxic
- flammable
- explosive
- some are pyrophoric(ignite spontaneously in air)

There are different types of reactors used in VPE, the most common are:
- Horizontal reactors: the wafers are placed horizontally in a quartz tube, and the gases flow horizontally over the wafer surfaces. This design allows for easy loading and unloading of wafers, but it can lead to non-uniform gas distribution and temperature gradients across the wafers.
- Vertical reactors: the wafers are placed vertically in a quartz tube, and the gases flow vertically over the wafer surfaces. This design provides better gas distribution and temperature uniformity across the wafers, but it can be more challenging to load and unload wafers.
- Rotating Disk Reactors: the wafers are mounted on a rotating disk that spins within the quartz tube. This rotation helps to improve gas distribution and temperature uniformity across the wafer surfaces, leading to more consistent epitaxial growth.
- Barrel Reactors: the wafers are placed in a cylindrical chamber, and the gases flow radially over the wafer surfaces. This design allows for high throughput and uniform gas distribution, making it suitable for large-scale epitaxial growth.
- Pancake Reactors: the wafers are arranged in a horizontal stack, resembling a stack of pancakes. The gases flow vertically over the wafer surfaces, providing good gas distribution and temperature uniformity. This design is often used for batch processing of multiple wafers simultaneously.
![[Pasted image 20251212170331.png]]
#### Liquid Phase Epitaxy (LPE)
![[Pasted image 20251212170526.png]]
LPE is a technique where the precursor materials are in the liquid phase, typically as molten materials, it is used when you can't vaporize the material easily. 
In this process you exploit the principle of supersaturation, meaning that the liquid solution contains more dissolved material than it can normally hold at a given temperature. When the solution is cooled or when the substrate is introduced, the excess material precipitates out of the solution and deposits onto the substrate, forming an epitaxial layer.
It is used for III-V semiconductors, SiC or multilayer structures, since it's difficult to vaporize them.
The solvent in this case is the low melting point metal component of the compound, for example in GaAs the solvent is Ga, while As is the solute or in InP the solvent is In and P is the solute.
The high temperature present a trade-off between the solubility of the solute in the solvent(higher temperature means higher solubility) and the thermal degradation of the substrate and the deposited layer(lower temperature means less degradation).
![[Pasted image 20251212171429.png]]
The reaction chamber is is made of a crucible containing the molten solution, heated by resistive heating elements. The droplets are placed in a well and the substrate is positioned on a sliding holder below the molten solution. As you reach the desired growth temperature, you slide the substrate up into contact with the molten solution. The solution cools down near the substrate surface, causing supersaturation and deposition of the epitaxial layer. After the desired thickness is achieved, you slide the substrate back down into the well to stop the growth.
You use a flow of purified H2 gas to create an inert atmosphere and avoid contamination from the air, you can't use oxygen since it would oxidize the molten solution.
#### Molecular Beam Epitaxy (MBE)
![[Pasted image 20251212171846.png]]
MBE is a technique where the precursor materials are in the vapor phase, but the growth occurs in ultra-high vacuum conditions(pressure of $10^{-10} Torr$). 
As always the molecules or atoms are rarified enough that their mean free path is very long, so that collisions between them are negligible. This allows for precise control over the growth process and the ability to create complex structures with atomic layer precision, but it's expensive and slow.
The molecules or atoms to be deposited are kept in Knudsen cells, which are heated crucibles that evaporate the source materials, creating molecular beams that travel through the vacuum chamber and deposit onto the substrate. The sliding shutter allows for precise control of the deposition time and thickness. The substrate rotates to ensure uniform deposition across its surface.
The presence of a load-lock chamber allows for the introduction and removal of substrates without breaking the ultra-high vacuum conditions in the main growth chamber, preserving the purity of the environment. The wafer is loaded in this chamber where the pressure gets pumped down to ultra-high vacuum levels before transferring it to the main chamber for epitaxial growth, thus avoiding contamination and increasing the throughput, since you don't need to wait for the main chamber to reach ultra-high vacuum levels every time you load a new wafer.
#### Chemical Vapor Deposition (CVD)
CVD is a deposition technique where precursor gases react chemically on the heated substrate surface to form a solid material that deposits as a thin film. 
CVD is not strictly monocrystalline, otherwise it would be VPE, but it can be polycrystalline or amorphous depending on the process conditions and the materials used. But LPE is not CVD since the precursor materials are in liquid phase.
##### Acceptance Angle and Conformality
![[Pasted image 20251212173551.png]]
The growth of the film depends on the flux of precursor gases incident on the substrate surface. The acceptance angle is the maximum angle at which precursor gases can effectively reach and deposit on the substrate surface. 
When the substrate is cold, the precursor gases don't have enough energy to migrate on the surface, so they deposit where they land, resulting in an acceptance angle dependency on the surface topography. This leads to poor conformality, meaning that high aspect ratio features like trenches or vias may not be fully coated, since the precursor gases can't reach the bottom of these features due to shadowing effects. 
When the substrate is heated, the precursor gases gain enough energy to migrate on the surface before depositing. This allows them to reach areas that are not directly exposed to the gas flux, improving conformality and resulting in a more uniform coating of high aspect ratio features.
![[Pasted image 20251212173931.png]]
We describe conformality based on how well the deposited film replicates the underlying surface topography. High conformality means that the film closely follows the contours of the substrate, while low conformality indicates that the film does not adequately cover features such as trenches or vias.
Some examples of bad conformality are key holes(leading to bad step coverage) and seams(leading to voids).
PVD is non conformal, while CVD is conformal. Obviously the conformality depends on the temperature of the substrate, higher temperature means higher conformality.
##### Atmospheric Pressure CVD (APCVD) and Low Pressure CVD (LPCVD)
We have two different techniques to break the gaseous precursor molecules:
- Atmospheric Pressure CVD (APCVD): the process is carried out at atmospheric pressure(1 atm). The high pressure promotes collisions between gas molecules, leading to a higher reaction rate and faster deposition. However, it can also result in non-uniform film thickness and lower conformality due to limited gas diffusion into high aspect ratio features. You have a reaction chamber with gas inlets and outlets curtains to maintain the pressure and keep control of the contamination, and you have a conveyor belt to move the wafers through the chamber for continuous processing.
![[Pasted image 20251212174625.png]]
- Low Pressure CVD (LPCVD): the process is carried out at reduced pressure(typically 5 orders of magnitude lower than atmospheric pressure, around $0.1-1 Torr$). The low pressure reduces collisions between gas molecules, allowing for better gas diffusion into high aspect ratio features and improved conformality. However, the reaction rate may be slower compared to APCVD, requiring longer deposition times. 
#### Plasma Enhanced CVD (PECVD)
##### Generating Plasma(DC Voltage)
![[Pasted image 20251212182113.png]]
A plasma is generated by applying a high voltage between two electrodes in a low pressure chamber filled with a process gas(typically Argon). The electrons come in contact with the gas molecules, ionizing them and so contributing another electron to the plasma that can ionize more gas molecules, creating a chain reaction that sustains the plasma. To explain it better an electron collides with a gas molecule, ionizing it and creating a positive ion and another electron. 
When the excited atoms return to their ground state, they release energy in the form of photons(light) and heat.
There are 4 main collision processes that can occur in the plasma:
- ionization: $e^- + A \rightarrow 2e^- + A^+$, resulting in a cascade effect that contributes to sustaining the plasma
- dissociation: $e^- + SiH_4 \rightarrow e^- + SiH_3^{\bullet} + H^{\bullet}$ where the bullet indicates a radical, so a neutral atom or molecule with fragmented bonds and unpaired electrons, making it highly reactive
- excitation: $e^- + A \rightarrow e^- + A^*$, where the atom or molecule has an electron in an higher excited state that will return to the ground state releasing a photon green, blue or purple
- relaxation: $Ar^* \rightarrow Ar + h\nu$, where an excited atom or molecule returns to its ground state releasing a photon, this gives the plasma its characteristic glow, the color of the glow depends on the gas used
##### Generating Plasma(RF Voltage, Alternator)
![[Pasted image 20251212183538.png]]
In RF plasma generation, an alternating current(AC) voltage at radio frequency(typically 13.56 MHz) is applied between two electrodes in a low pressure chamber filled with a process gas(typically Argon). The oscillating electric field causes the electrons to accelerate back and forth between the electrodes, colliding with gas molecules and ionizing them, thus sustaining the plasma.
The electrons are forced to follow the oscillating electric field, gaining energy during each half cycle and colliding with gas molecules, while the heavier ions respond more slowly to the changing electric field, resulting in a plasma that is primarily sustained by electron collisions.
A steady state plasma is achieved when the rate of ionization balances the rate of recombination and loss processes in the plasma.
##### Plasma Enhanced CVD (PECVD) Process
![[Pasted image 20251212184149.png]]
In PECVD, the plasma generated in the reaction chamber provides additional energy to the precursor gases, promoting chemical reactions on the substrate surface at lower temperatures compared to traditional CVD processes. 
It forces reaction that wouldn't happen at low temperatures, allowing for lower temperature deposition. The main disadvantage is that the plasma can damage sensitive substrates due to the presence of radicals that contain molecules that contaminate the film.
The main advantages as states before are the we can deposit on temperature sensitive substrates and in general in our process flow we want to start with high temperature processes and then move to lower temperature ones to avoid damaging previously deposited layers, so PECVD is useful for later deposition steps(near end processing).
So in the end, even if it doesn't ensure high quality films like traditional CVD, it's useful for low temperature depositions.
![[Pasted image 20251212184602.png]]
##### PECVD Process Control Parameters
![[Pasted image 20251212184647.png]]
The pros and cons of PECVD are:
- Pros: 
	- Lower deposition temperatures compared to traditional CVD processes, making it suitable for temperature-sensitive substrates.
	- High deposition rates due to acceleration of ionized species in the plasma toward the substrate.
- Cons:
	- More complex equipment and process control compared to traditional CVD.
	- More expensive due to the need for plasma generation equipment.
	- Film quality may be lower compared to traditional CVD processes, with higher levels of impurities and defects.
#### Atomic Layer Deposition (ALD)
![[Pasted image 20251212192427.png]]
ALD is a thin film deposition technique that allows for precise control of film thickness and composition at the atomic scale. It is based on sequential, self-limiting surface saturation reactions between precursor gases and the substrate surface, meaning that each precursor gas reacts with the surface until all available reactive sites are occupied, preventing further reaction until the next precursor is introduced.
One cycle is a 4 step process, we give an example of depositing Al2O3 using TMA(trimethylaluminum, C3H9Al) and H2O as precursors:
1. Elimination of hydrogen atoms bound to oxygen at the substrate surface: The methyl groups(CH3) from TMA react with hydrogen atoms bound to oxygen on the substrate surface, forming methane(CH4) and leaving behind Al atoms bonded to the oxygen atoms on the surface, till all the reactive sites are occupied. So basically we start on the surface with -OH groups, we lose an -H from the -OH that bounds with a CH3 from TMA, forming CH4 and leaving an -O-Al- group on the surface with still attached -CH3 groups.
2. Purge: An inert gas, such as nitrogen or argon, is introduced into the chamber to remove any unreacted TMA and byproducts from the previous step.
3. Reaction with water: Water molecules react with the Al atoms bonded to the oxygen atoms on the surface, forming Al-OH groups and releasing methane(CH4) as a byproduct, till all the reactive sites are occupied. So now we have -O-Al- groups with still attached -CH3 groups on the surface, the H2O reacts with the -CH3 groups, forming CH4 and leaving -O-Al-OH groups on the surface. Ready for the next cycle.
4. Purge: Another inert gas purge is performed to remove any unreacted water and byproducts from the previous step.
This way we have deposited exactly one monolayer of Al2O3 per cycle, and we can repeat the cycle since the surface is ready with -OH groups again. It's called atomic layer deposition since we deposit one atomic layer per cycle.
This process is perfectly conformal, since the precursor gases can reach all areas of the substrate surface, even high aspect ratio features like trenches or vias, due to the self-limiting nature of the surface reactions.
#### Deposited Materials
##### Silicon Dioxide (SiO2)
Silicon Dioxide (SiO2) can be created through oxidation, but we can deposit it, with worse quality, using CVD, for different applications:
- undoped oxide: used as physical separator or insulator between different layers of metal(where you can't use thermal oxidation since it would oxidize the metal) or as masking layer for ion implantation and diffusion processes, or just to increase the thickness of a thermally grown oxide layer. For example in transistors we superimpose 17 layers of metals and to sustain them and insulate them we use undoped oxide layers deposited with CVD.
- doped oxide: used for passivation layers to protect the underlying layers from contamination and damage, or as last layer to protect the device.

![[Pasted image 20251212193247.png]]
In the table we can see the different deposition techniques for SiO2, from right to left we see: lower temperature, worse contamination, worse thermal stability, worse dielectric strength, worse mechanical stress, worse conformality. So it's a trade-off between temperature and quality.
##### Polysilicon
Polysilicon is a material made up of small silicon crystals, or grains, that are randomly oriented. 
The grain size depends on the deposition temperature, higher temperature means larger grains, leading to monocrystalline-like properties, while lower temperature means smaller grains, leading to more grain boundaries and defects. 
High temperature is mandatory to create monocrystalline silicon, but it's not sufficient, since we also need a seed crystal to grow on, otherwise we would create polycrystalline silicon.
Polysilicon is used for example to create gate electrodes in MOSFETs, since it can be heavily doped to achieve high conductivity, and it can withstand high temperatures during subsequent processing steps.
#### Physical Vapor Deposition (PVD)
The type of bonding is no more chemical, but physical (Van der Waals forces, electrostatic forces, etc). The atoms or molecules are deposited by physical means, such as evaporation or sputtering. The process is mostly used for metals and alloys.
##### Thermal Evaporation
![[Pasted image 20251210185712.png]]
A high vacuum chamber(since low pressure is needed to avoid collisions between the evaporated atoms and gas molecules, of $10^{-5} Pa$) is used to increase the mean free path of the evaporated atoms(the mean free path is the average distance traveled by a moving particle between successive collisions). This allows for a line of sight deposition, meaning that starting from the source, the atoms will travel in straight lines to the substrate without colliding with gas molecules. The downside is that it promotes non conformal coverage due to shadowing effects.
![[Pasted image 20251210185726.png]]
In CVD the source material is heated promoting the diffusion of atoms or molecules on the surface, resulting in a less topography dependent deposition. While in PVD the source material is cold, so no migration happens, resulting in a more topography dependent deposition.
The wafers are placed upside down to lower the contamination from particles falling from the source.
A shutter is implemented to avoid deposition during the heating phase.
You can only deposit material with lower melting point than the heating element.

The source material(the one to be deposited) is placed in a crucible, which is heated by resistive heating, thanks to the Joule effect. When the material reaches its evaporation temperature, atoms or molecules leave the surface and travel to the substrate, where they condense forming a thin film.
You can use it both for sublimating materials(solid to gas transition) and for materials that melt first(liquid phase).
![[Pasted image 20251210190901.png]]
There's a table to help choosing the crucible material based on the source material, since:
- some materials can react with the crucible
- the crucible melting point must be higher than the source material melting point
- cross contamination with the wire used for resistive heating must be avoided(ex: W wire can contaminate with W atoms the deposited film)
Not every material can be thermally evaporated, for example materials with very high melting points like Ta, W, Mo are not suitable.

If we want an higher throughput(deposition rate), we can use a planetary substrate holder, where we place source in the center and substrates on rotating holders tangentially to the sphere surface to guarantee a uniform deposition on all substrates. We rotate the substrates to average out non uniformities in the deposition rate due to the geometry of the system and the whole holder to have a more uniform distance from the source, that's why it's called planetary.
![[Pasted image 20251211165953.png]]
##### Electron Beam Evaporation
![[Pasted image 20251211164338.png]]
A filament is heated to emit electrons, which are accelerated through a negative voltage and directed using a magnetic field perpendicular to the electron beam path, towards the liner containing the source material. The kinetic energy of the electrons is converted into thermal energy when they hit the source material, causing its evaporation.
The liner is pre-cooled to avoid cross contamination between the liner material and the source material, and from the liner to the deposited film.
Normally a carousel with multiple liners is used to deposit different materials without breaking the vacuum and exploiting a single electron gun. This way you can also deposit multiple layers in sequence.
We deposit multiple metallic layers to avoid delamination due to poor adhesion between some metals and Silicon, for example Ti is used as an adhesion layer between Si and Au, and also to avoid oxidation we can add a passivation layer like Au on top of Cu.
For example to create a Ti/Al/Au Ohmic contact we deposit an adhesion layer of Ti to avoid delamination and to compensate for Al poor adhesion on Si, then an Al layer for the Ohmic contact, and finally a Au layer to avoid oxidation of Al.
We use a single deposition technique to deposit multiple layers in sequence to accelerate the process and to have greater throughput, also to maintain the vacuum and avoid contamination.
![[Pasted image 20251211165600.png]]

#### Sputtering
![[Pasted image 20251211174630.png]]
Sputtering is a physical vapor deposition technique. Starting from a chamber with a pressure of a few mTorr(10-100 mTorr) to decrease the possibility of collisions between the sputtered atoms and to avoid contamination from the atmosphere, an Argon gas is introduced in the chamber. A high voltage is applied between the target(the source material to be deposited, positioned on a cathode) and the substrate(anode), creating a plasma. Argon is used since it's a noble gas and won't react with the target material. The high energy ions created in the plasma are accelerated towards the target, where they hit the surface and transfer their kinetic energy to the atoms of the target material. If the transferred energy is higher than the binding energy of the atoms in the target, they will be ejected from the surface(thus sputtered) and travel to the substrate, where they condense forming a thin film.
You can deposit almost any material with sputtering, even those with high melting points like Ta, W, Mo. The only downside is that is more expensive.
Through sputtering you can achieve a better adhesion between the deposited film and the substrate, since the high energy of the sputtered atoms promotes intermixing at the interface.
We can have both DC and RF sputtering.
##### DC Sputtering
![[Pasted image 20251211175315.png]]
You place a DC voltage on the cathode(target) and ground the anode(substrate). The plasma is created and the ions are accelerated towards the target, sputtering atoms that will deposit on the substrate. You have one inlet for the Argon gas and one outlet for the vacuum pump.
Since the substrate is cold there's no migration of atoms on the surface, so the deposition is topography dependent. But it's a little bit better than Electron Beam Evaporation since the source points are multiple, basically every sputtered atom is a source point, so shadowing effects are reduced, while in Electron Beam Evaporation there's a single source point.
So the conformality of DC sputtering(step coverage) is better than Electron Beam Evaporation, but still not great, and it gets worse with higher aspect ratio features and as the deposition thickness increases because shadowing effects increase. So the top areas get more deposition than the bottom of the trenches.
![[Pasted image 20251211175832.png]]
The bottlenecks of DC sputtering  are the power to create and sustain the plasma, and the target material may be loss due to sputtering.
##### RF Sputtering
![[Pasted image 20251211180451.png]]
RF sputtering is used for insulating target materials, since in DC sputtering the target needs to be conductive to avoid charge build up on the surface that would stop the sputtering process.
An AC voltage at radio frequency(typically 13.56 MHz) is applied to the target, creating a plasma. The oscillating electric field causes the ions to accelerate towards the target during the negative half cycle, sputtering atoms. During the positive half cycle, electrons are accelerated towards the target, neutralizing the charge build up on the surface, and we allow the deposition on the substrate.(write it better)
Basically when the electric field points upwards the target is negative and ions are accelerated towards it, while when it points downwards the target is positive and electrons are accelerated towards it and deposition will happen on the substrate.
So the RF sputtering is slower than DC sputtering by half, since only the negative half cycle contributes to sputtering.
The top electrode, the one connected to the RF power supply, the target, is now smaller than the grounded electrode, the substrate holder. This causes a self biasing effect, where the target develops a negative DC bias with respect to the plasma potential, increasing the energy of the ions hitting the target and thus the sputtering rate.
##### Magnetron Sputtering
![[Pasted image 20251211181404.png]]
Magnetron sputtering is a variation of sputtering that uses magnetic fields perpendicular to the electric field to confine the plasma close to the target surface, by forcing the ions and electrons to follow helical paths around the magnetic field lines. This increases the ionization efficiency and the sputtering rate, allowing for higher deposition rates at lower pressures and lower energy consumption.
Basically the magnetic field make it so the now curved paths of the electrons and ions increase the probability of collisions between them, thus increasing the plasma density close to the target surface. The magnetic fields are normally placed behind the target.
The two main disadvantages are the higher cost and the non uniform erosion of the target, since the magnetic field is not uniform across the target surface, causing uneven sputtering and reducing the target utilization efficiency.
##### Reactive Sputtering
![[Pasted image 20251211181938.png]]
Reactive sputtering is a variation of sputtering that involves introducing a reactive gas, such as oxygen or nitrogen, into the sputtering chamber along with the inert sputtering gas(Argon). The reactive gas reacts with the sputtered atoms from the target to form a compound film on the substrate.
This way we can use DC sputtering even for insulating materials, since the compound film is formed on the substrate and not on the target, because the silicon is doped to be conductive enough to avoid charge build up on the target surface.
For example to deposit SiO2 we can use a Si target and introduce O2 gas in the chamber, the sputtered Si atoms will react with O2 to form SiO2 on the substrate.
So the main difference between reactive and non reactive sputtering is that in reactive sputtering the deposited film is a compound formed by the reaction between the sputtered atoms and the reactive gas, while in non reactive sputtering the deposited film is made of the same material as the target.
##### Ionized Sputtering or HDP Sputtering
As we said previously the conformality of sputtered films is not great, since the sputtered atoms are neutral and travel in straight lines from the target to the substrate, causing shadowing effects. To improve the conformality we can ionize the sputtered atoms using an RF coil placed between the target and the substrate. The ionized atoms can then be directed towards the substrate using electric fields, allowing for better step coverage and conformality, especially in high aspect ratio features.
This technique is also called High Density Plasma(HDP) sputtering, since the ionization of the sputtered atoms increases the plasma density in the chamber.
For example we can use this technique to create vertical interconnection between different metal layers in a multilayer structure, called vias, with good step coverage and conformality.
![[Pasted image 20251211183939.png]]
#### Electroplating - Electrodeposition - Galvanic Deposition
One of the oldest deposition techniques, the most basic form of electroplating involves:
- a bath: a solution containing metal ions to be deposited
- an anode: a metal that dissolves into the solution to replenish the metal ions
- a cathode: the substrate on which the metal ions are reduced and deposited
- a power supply: to provide a dc voltage between the anode and cathode

The process involves 2 steps:
1. Oxidation at the anode: Metal atoms lose electrons and go into solution as metal ions.
2. Reduction at the cathode: Metal ions in the solution gain electrons and deposit as solid metal on the substrate.

The role of the power supply is to drive the non-spontaneous redox reactions by providing the necessary energy.

Not all metals can be electroplated easily. The most commons ones are Au, Ni, Cu, Ag, Zn, Sn, Cd.
It's a really fast process($\sim \mu m/min$) and can produce thick films ($> 100 \mu m$) with good uniformity and adhesion. 
However, it requires a seed layer of conductive material on the substrate to start the deposition, since Silicon itself is not conductive enough. So normally a metallic seed layer is deposited using PVD or CVD before electroplating, the deposition will only happen in those areas.
![[Pasted image 20251210175150.png]]
We also need electrical connection between the metallic seeds.
## References
