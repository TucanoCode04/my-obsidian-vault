
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
- Wire Bonding: Connecting the die to the package electrical leads using fine wires  made of gold, aluminum, or copper. Basically there's a machine that splashes the gold onto the die and package leads to create electrical connections
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


## References
