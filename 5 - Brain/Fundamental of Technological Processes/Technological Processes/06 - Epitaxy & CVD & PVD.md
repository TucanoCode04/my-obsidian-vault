
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
