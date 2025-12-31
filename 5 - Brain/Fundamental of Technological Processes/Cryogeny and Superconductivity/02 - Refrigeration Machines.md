
2025-12-31 16:11

Status: 

Tags:

# 02 - Refrigeration Machines
##### Regenerative Heat Exchangers
They differ from the continuous flow exchangers discussed before. They act as cold storage devices, discontinuously absorbing heat from the cold fluid and releasing it to the hot fluid. They can store the energy from one fluid stream and then transfer it to another stream. 
Regenerative heat exchangers normally use a porous matrix of finely divided solid material to form the heat transfer surface (you can even size them as a ball to maximize surface area). 
The exchanger should have an heat capacity higher than the fluids being processed, for operations at 70-80 K stainless steel is often used, for lower temperatures, 4 K, a combination of lead balls and rare earths is used. 
#### Stirling Cycle Refrigerators
We can discuss the cycle using a pressure-volume diagram. The cycle consists of:
1. Isothermal compression (1-2): The right pistol remains fixed while the left piston compresses the gas at constant temperature $T_H$. Heat $Q_H$ is rejected to the surroundings (hot reservoir).
2. Isentropic expansion (2-3): Both pistons move simultaneously to keep the gas volume constant while the gas flows through the regenerator, releasing heat $Q_R$ to the regenerator matrix, to re enter colder the right cylinder.
3. Isothermal expansion (3-4): The left piston remains fixed while the right piston expands the gas at constant temperature $T_C$. Heat $Q_C$ is absorbed from the cold reservoir.
4. Isentropic compression (4-1): Both pistons move simultaneously to keep the gas volume constant while the gas flows back through the regenerator, absorbing the same amount of heat $Q_R$ as the previous step from the regenerator matrix, to re enter hotter the left cylinder.
![[Pasted image 20251231164222.png]]
##### Stirling Cryocoolers
A small portable single stage Stirling cryocooler can reach temperatures as low as 80 K, while the two stage versions can even reach 4 K. They are often used for magnet cooling or for precooling before a Joule-Thomson expansion stage.
The working gas is compressed in one chamber, then transferred to another chamber though a regenerative heat exchanger, where it expands and cools. The regenerator stores the heat from the gas when it flows from the hot to the cold side, and returns it to the gas when it flows back.
![[Pasted image 20251231164733.png]]
1. Compression in space $D$ by the piston $B$, the heat generated is removed by water cooling.
2. Transfer of the gas through the regenerator $G$ to the cold side $E$ using a displacer piston $C$. The gas cools down as it passes through the regenerator since it gives up heat to the regenerator material.
3. Expansion and further cooling of the gas in space $E$. The cold gas can now be used to cool the load (the load is important to avoid temperature oscillations).
4. Transfer of the gas back through the regenerator $G$ to the hot side $D$ using the displacer piston $C$. The gas warms up as it passes back through the regenerator since it absorbs heat from the regenerator material and the regenerator is cooled down for the next cycle.

**Split Cycle Coolers**
Split cycle coolers are a variation of the Stirling cryocooler where the compressor and the expander (cold head) are separated. The working gas is compressed in a remote compressor and then transferred to the cold head through a transfer line. The cold head contains the displacer/regenerator assembly and the expansion space. This design allows for more flexibility in the placement of the cold head and reduces vibrations at the cold tip.
![[Pasted image 20251231165723.png]]
![[Pasted image 20251231165807.png]]
**Special Cryocoolers**
- Single Stage Stirling Coolers: They provide cooling power in the range of a few watts at temperatures around 40-160 K. They are used to produce liquid nitrogen for various applications.
![[Pasted image 20251231170018.png]]
- 



## References
