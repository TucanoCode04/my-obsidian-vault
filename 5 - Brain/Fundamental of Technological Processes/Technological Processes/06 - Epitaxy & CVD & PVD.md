
2025-12-10 17:32

Status: 

Tags:

# 06 - Epitaxy & CVD & PVD





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
#### Sputtering






##### Electron Beam Evaporation
![[Pasted image 20251211164338.png]]
A filament is heated to emit electrons, which are accelerated through a negative voltage and directed using a magnetic field perpendicular to the electron beam path, towards the liner containing the source material. The kinetic energy of the electrons is converted into thermal energy when they hit the source material, causing its evaporation.
The liner is pre-cooled to avoid cross contamination between the liner material and the source material, and from the liner to the deposited film.
Normally a carousel with multiple liners is used to deposit different materials without breaking the vacuum and exploiting a single electron gun. This way you can also deposit multiple layers in sequence.
We deposit multiple metallic layers to avoid delamination due to poor adhesion between some metals and Silicon, for example Ti is used as an adhesion layer between Si and Au, and also to avoid oxidation we can add a passivation layer like Au on top of Cu.
For example to create a Ti/Al/Au Ohmic contact we deposit an adhesion layer of Ti to avoid delamination and to compensate for Al poor adhesion on Si, then an Al layer for the Ohmic contact, and finally a Au layer to avoid oxidation of Al.
We use a single deposition technique to deposit multiple layers in sequence to accelerate the process and to have greater throughput, also to maintain the vacuum and avoid contamination.
![[Pasted image 20251211165600.png]]




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
