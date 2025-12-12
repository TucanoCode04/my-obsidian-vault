
2025-12-06 17:02

Status: 

Tags:

# 09 - Packaging
An overview of the packaging steps contains several key stages:
- Finished Wafer
- Wafer Test: Electrical testing of individual dies on the wafer to identify functional units and roughness tests
- Defective Die Inking: Marking with ink or laser to identify defective dies
- Wafer Sawing: Cutting the wafer into individual dies using a diamond saw or laser
- Packaging: Encapsulating the good dies in protective packages
- Final Test: Electrical testing of packaged devices to ensure functionality and performance
##### Packaging Steps
- Wafer Sawing: The wafer is cut into individual dies mechanically using a diamond saw or laser. The mechanical saw is used for thicker and irregular wafers
- Dies bonding: The good dies are picked and placed onto a substrate 
- Wire Bonding: Connecting the die to the package electrical leads using fine wires made of gold, aluminum, or copper. Basically there's a machine that splashes the gold onto the die and package leads to create electrical connections
- Package Sealing: The die and wire bonds are encapsulated in a protective package using molding or sealing techniques to protect against environmental factors
- Inspection and Testing: The packaged devices undergo final electrical testing and visual inspection to ensure quality and functionality
![[Pasted image 20251206172658.png]]
##### Functions of Packaging
- Power distribution from circuit board to the die(chip)
- Signal distribution between the die and the circuit board
- Heat dissipation from the die to the environment
- Protection of the die from physical damage and environmental factors, mechanical, chemical and electromagnetic protection
The functionality depends on the package type and design, for example in quantum applications we don't need to dissipate the heat generated inside the chip, instead we need to isolate the chip from the environment to avoid decoherence.
##### Packaging Types
- Dual In-line Package (DIP): A rectangular package with two parallel rows of pins, commonly used for through-hole mounting on circuit boards. The ratio of magnitude between the chip and the package is very high, meaning the package is much larger than the chip itself, so it's suboptimal.
- Single In-line Package (SIP): Similar to DIP but with a single row of pins, used for through-hole mounting. Also has a high package-to-chip size ratio.
- Leadless Chip Carrier (LCC): A package where the leads are all around the package, designed for surface mounting on circuit boards. The package size is still significantly larger than the chip.
- Pin Grid Array (PGA): A package with an array of pins on the bottom, used for high pin count and faster signal transmission like microprocessors or memory chips. The package size is still much larger than the chip.
- Ball Grid Array (BGA): A package with an array of solder balls on the bottom, used for high pin count and better thermal and electrical performance. The package size is still significantly larger than the chip.
![[Pasted image 20251206173713.png]]
##### Flip-Chip Bonding
Flip-chip bonding is an advanced packaging technique where the die is flipped upside down and directly connected to the substrate using solder bumps. This method allows for shorter electrical paths, improved performance, and better heat dissipation compared to traditional wire bonding methods. This way you reduce resistance and inductance, allowing for higher frequency operation, the footprint of the package is also reduced since you don't need the wire bonds.
![[Pasted image 20251206174552.png]]
##### Multi-Chip Modules (MCM)
Multi-chip modules (MCM) are advanced packaging solutions that integrate multiple dies within a single package. MCMs improve the efficiency of space, this model defines a lower bound for efficiency of 30%. Efficiency is defined as the ratio of the total die area to the total package area(circuit board area). (Maybe look up something more)
##### 3D Packaging
3D packaging involves stacking multiple dies vertically within a single package, connected through vertical interconnects such as through-silicon vias (TSVs). The only problem with this technique are:
- Thermal Management: Stacked dies can generate more heat, making it challenging to dissipate effectively.
- Electrical Connections: two different approaches:
	 - TSVs: Vertical interconnects that pass through the silicon substrate, providing direct electrical connections between stacked dies. They are usually made using deep reactive ion etching (DRIE) to ensure low inductance and resistance, and electroplating for the deposition of conductive material to ensure low resistance.
	 - Wire Bonds: Traditional wire bonding techniques can be adapted for 3D packaging, but they may introduce additional complexity and potential reliability issues.
## References
