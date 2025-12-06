
2025-12-05 16:28

Status: 

Tags:

# 10 - Complementary Technologies
Da slide 14
#### Wafer Bonding
Wafer bonding is a process used to join two or more wafers together to create a single, unified structure. It can be used to bond two silicon wafers or two different materials, such as silicon and glass. 
It's used in various applications:
	- microfluid circuits and systems, to create multiplayer or complex microchannels for fluid flow and manipulation.
![[Pasted image 20251205164229.png]]
	- complex mechanical systems, like microaccelerometers or gyroscopes, where multiple layers are needed to achieve the desired functionality.
![[Pasted image 20251205164218.png]]
	- packaging: to encapsulate and protect delicate microstructures or devices.
There 3 main categories of wafer bonding techniques: 
- Heat-Assisted Bonding: involves applying heat and pressure to bond the wafers together. This method is suitable for materials with similar thermal expansion coefficients.
- Electrical Field Assisted Bonding: uses an electric field to promote bonding between the wafers. This technique is often used for bonding materials with different properties.
- Chemistry-Assisted Bonding: relies on chemical reactions to create strong bonds between the wafers. This method is commonly used for bonding materials like silicon and glass.
It's normally a 3 step process:
1. Surface Preparation: The wafer surfaces are cleaned and treated to remove contaminants and ensure good adhesion. Since a particulate could create voids between the wafers, the cleaning process is crucial.
![[Pasted image 20251205164542.png]]
2. Contacting: The wafers are aligned and brought into contact under controlled conditions.
3. "Annealing": The wafers are heated to promote bonding. The temperature and duration depend on the materials being bonded and the specific bonding technique used. It's not used in all bonding methods.
The first step is important because the quality of the bond often depends on the surface conditions, No Surface Topography Tolerant bonding methods require extremely flat and smooth surfaces to ensure good contact and adhesion between the wafers.
##### Fusion Bonding
Fusion bonding is one of the first and most used wafer bonding techniques. It involves bringing two ultra-clean, flat, and smooth wafer surfaces into contact and applying heat and pressure to create a strong bond. 
After a certain time due to the heat and external load, between the 2 wafers will be created a layer of SiO2 that will bond the two wafers together(since at some temperature silicon reacts with oxygen to form silicon dioxide) creating covalent bonds at the interface. 
In the process we use some mechanical spacers to keep the wafers aligned during the bonding process, and they will slowly be removed during the annealing step.
The bonding is so strong that if you try to cut the wafers apart you will end up breaking the silicon itself rather than the bond.
This process is not surface topography tolerant.
![[Pasted image 20251205165335.png]]
##### Anodic Bonding
Anodic bonding is a wafer bonding technique used to bond a silicon wafer to a glass wafer, to guarantee that one side is transparent.
The process is not surface topography tolerant, the max allowed roughness is in the order of 0.1 $\mu$m.
You put the wafer on a hot plate (400-500 °C) with the Pyrex glass on top of the silicon wafer.
The two materials have different coefficients of thermal expansion, so when you heat them up the glass expands more than the silicon, creating mechanical stress at the interface, that's why we compensate with an high dc voltage applying the negative electrode to the glass and the positive one to the silicon wafer.
We use a special type of glass that it's the most similar in terms of thermal expansion to silicon (Pyrex 7740).
The high temperature makes the sodium ions in the glass more mobile, and they migrate towards the negative electrode , leaving behind negatively charged oxygen ions at the interface, which produce an electrostatic force that, similarly to the mechanical stress, pushes the two wafers together, promoting bonding why the increasing of the temperature.
![[Pasted image 20251205170459.png]]
##### Glass Frit Bonding
Glass frit bonding is a wafer bonding technique that uses a low melting point glass(as low as 160°) material (glass frit) to bond two wafers together. This technique allows from the bonding of materials that would not withstand high temperatures, such as certain metals or polymers.
This process is surface topography tolerant, thanks to the usage of a intermediate layer. The trade.off for the low 
##### Global Planarization - Chemical Mechanical Polishing
To make the surface flat and smooth we use mechanical abrasion combined with chemical etching.
We attach the wafer upside down to a wafer carrier and use a polishing pad with slurry (abrasive particles suspended in a chemical solution) to polish the wafer surface. The two counter rotating motions and the pressure applied help to achieve a uniform planarization.



## References
