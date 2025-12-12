
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
This graph shows additionally to the requirements listed before to achieve epitaxial growth, the grow rate in function of the temperature(in this case the high temperature is on the left side). )



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
