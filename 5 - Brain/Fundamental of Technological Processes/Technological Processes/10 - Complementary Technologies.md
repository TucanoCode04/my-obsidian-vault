
2025-12-05 16:28

Status: 

Tags:

# 10 - Complementary Technologies
##### Bulk Micromachining
Bulk micromachining is a technique used to create microstructures by selectively etching away portions of a silicon wafer. 
It's a less versatile, since we are limited to the thickness of the wafer, and with less resolution, since the etching is isotropic, but it's cheaper and faster than surface micromachining.
**Frontside Bulk Micromachining**
In frontside bulk micromachining, the etching is performed from the front side of the wafer, where the microstructures are defined. So a suspended structure is created by etching away the silicon beneath it.
![[Pasted image 20251206141717.png]]
A cantilever is a common structure created using frontside bulk micromachining, it's a beam anchored at one end and free at the other end, used in various applications such as sensors, actuators, and microelectromechanical systems (MEMS).
Normally through thermal oxidation we create a SiO2 layer that will act as an hard mask for the etching process.
![[Pasted image 20251206142640.png]]
To create a cantilever we first pattern the SiO2 layer using photolithography to define the shape of the cantilever. Then we create concave corners that will stop being etched at the 111 planes of the silicon crystal, paired with some convex corners that having a 100 plane will be etched faster, creating an underetch that will help in releasing the cantilever.
The underetch is important to make sure that the cantilever is fully released from the substrate, allowing it to move freely.
![[Pasted image 20251206142623.png]]
**Backside Bulk Micromachining**
In backside bulk micromachining, the etching is performed from the back side of the wafer, opposite to where the microstructures are defined. This technique is often used to create through-wafer structures or to thin down specific areas of the wafer.
A lot of times the two techniques are combined together to create complex microstructures.
![[Pasted image 20251206141815.png]]

The techniques used for etching are:
- Wet Etching
- Vapor Etching
- Dry Etching
We have seen them used for thin layer etching, but in bulk micromachining we use them to etch deep into the silicon substrate.
#### Etch Stop Techniques
##### P++ Etch Stop
P++ etch stop is is a technique used in bulk micromachining to create precise and controlled etching of silicon wafers. 
If a portion of the Silicon wafer is doped with a concentration of boron atoms higher than $10^{19}$, the etching rate of that region will be significantly reduced when using certain etchants, such as potassium hydroxide (KOH). 
This property allows us to use the heavily doped region as an etch stop layer, enabling us to create well-defined microstructures with precise dimensions.
![[Pasted image 20251206143636.png]]
##### Electrochemical Etch Stop
Electrochemical etch stop is a technique used in bulk micromachining to create precise and controlled etching of silicon wafers using an electrochemical process.
In this technique, a p-n junction is created within the silicon wafer, which is immersed in an electrolyte solution of a Silicon etchant, such as KOH. 
You attach a potentiostat to the wafer, applying a positive voltage to the n-type region and a negative voltage through the electrolyte solution to the p-type region. 
If the voltage is not applied the etchant will etch anisotropically the silicon wafer, but when when the voltage is applied, the p-n junction becomes reverse biased, creating a depletion region. Near the junction an anodic oxide layer is formed through silicon passivation, which prevents further etching of the silicon in that region.(Write this better)
![[Pasted image 20251206144457.png]]
##### Surface Micromachining 
In surface micromachining, microstructures are created by depositing and patterning thin films on the surface of a substrate, typically a silicon wafer. This technique allows for the creation of complex(multi-layered and multi-material) microstructures with high precision and resolution. The higher surface exploitation allows for more complex geometries and functionalities.
Surface micromachining involves two types of layers:
- Structural Layers: These layers form the actual microstructures and are typically made of materials such as polysilicon, silicon nitride, or metals. They provide the mechanical properties needed for the microstructures to function.
- Sacrificial Layers: These layers are temporarily deposited between structural layers and are later removed to create gaps or cavities. Common sacrificial materials include silicon dioxide (SiO2) or photoresist.
An example of a product created using surface micromachining is a micromirror array used in digital light processing (DLP) technology for projectors and displays. Each micromirror can be individually tilted to reflect light, allowing for high-resolution image projection.
A good design rule is to introduce holes in the structural layers to allow the etchant to reach and remove the sacrificial layers more effectively, speeding up the release process.
![[Pasted image 20251206164010.png]]
##### Criteria for selecting Sacrificial and Structural Materials 
When selecting materials for sacrificial and structural layers in surface micromachining, several criteria must be considered to ensure compatibility, performance, and manufacturability:
- Etch Selectivity: The sacrificial material should have a high etch selectivity relative to the structural material. This means that the etchant used to remove the sacrificial layer should effectively etch the sacrificial material while minimally affecting the structural material.
- Etch Rate: The etch rate of the sacrificial material should be sufficiently high to allow for efficient removal during the release process, reducing fabrication time. As always there is a trade-off with this first 2 properties.
- Deposition Temperature: The deposition temperature of different materials should be compatible to prevent damage or deformation of previously deposited layers.
- Intrinsic Stress: There are 2 main types of intrinsic stress: tensile and compressive. Tensile stress can cause the structural layers to crack or delaminate, while compressive stress can lead to buckling or warping. The materials chosen should have compatible stress profiles to minimize these issues.
- Surface Smoothness: The surface roughness of both sacrificial and structural materials should be minimized to ensure good adhesion and to prevent defects in the microstructures.
##### Stiction Problem
Stiction is a common problem in surface micromachining that occurs when microstructures adhere to the substrate or to each other during the release process. This can lead to device failure or reduced performance.
The liquid-gas transition is harsh at a micro scale, the capillary forces generated during drying can pull the microstructures down onto the substrate, causing them to stick. 
That's exactly what happens during the drying phase after the sacrificial layer has been etched away using a wet etching process. A water meniscus forms between the microstructures and the substrate, generating capillary forces(Van der Waals forces) that can cause the microstructures to stick to the substrate.
![[Pasted image 20251206165454.png]]
To prevent this issue, one of the best solution is the usage of low surface tension liquids during the rinsing and drying phases, such as Methanol or Isopropanol, that will generate lower capillary forces.
Other strategies to mitigate stiction include:
- Reducing Adhesion Area: creating dimples or patterns on the substrate to create one point contact instead of a full surface contact.
![[Pasted image 20251206165639.png]]
- Creation of Anchor Points: designing the microstructures with anchor points that help to keep them elevated above the substrate, that are removed after the drying phase.
- Sublimation Drying: you avoid the liquid-gas transition by freezing the rinsing liquid and then sublimating it under vacuum, going directly from solid to gas phase. You can-t use water since it expands when it freezes, so you have to use other liquids with low freezing points.
- CO2 Supercritical Drying: you bring the liquid above its critical point(dependent on temperature and pressure) where there is no distinction between liquid and gas phase, so there are no surface tension forces acting on the microstructures. The critical point of CO2 is at relatively low temperature and pressure (31°C and 70 bar), making it suitable for delicate microstructures.
- Vapor Phase Etching: instead of using a liquid etchant to remove the sacrificial layer, you can use a vapor phase etchant, such as HF vapor for SiO2 sacrificial layers. This eliminates the need for rinsing and drying, thereby avoiding stiction altogether. The only problem with this solution is that we need an isotropic etchant, so we can't use it for all the materials.
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
This process is surface topography tolerant, thanks to the usage of a intermediate layer. The trade-off for the low temperature is a lower bond strength.
The layer is patterned with lithography and then the wafers are aligned and brought into contact for an hermetic seal. 
The presence of an intermediate layer helps for the roughness of the surfaces or the bending of the wafers.
![[Pasted image 20251206132757.png]]
#### Polymeric Replication
Polymeric replication is a technique used to create microstructures on a substrate by using a polymer material as a mold or template. This technique is used to mass-produce microstructures with high precision and accuracy.
There are 3 main types of polymeric materials:
- Thermoplastics: These polymers can be melted and reshaped multiple times. They are commonly used in injection molding and hot embossing processes.
- Thermosetting Polymers: These polymers undergo a curing process that makes them rigid and inflexible. They are often used in applications requiring high mechanical strength and thermal stability.
- Elastomers: These polymers have elastic properties, allowing them to stretch and return to their original shape. They are used in applications requiring flexibility and resilience.
##### Microinjection Molding
This process uses mainly thermoplastic polymers. Some raw pellets of polymer are stored into an hopper and then they are fed into a heated barrel where they are melted by heaters and a rotating screw. The molten polymer is then injected into a mold cavity under high pressure, where it cools and solidifies to take the shape of the master mold. 
At the end the mold opens and the part is ejected.
![[Pasted image 20251206134016.png]]
##### Hot Embossing
This process is similar to microinjection molding, but instead of injecting molten polymer into a mold, a heated master mold is pressed into a thermoplastic polymer substrate. The polymer is heated allowing the molecules to become more mobile and slide past each other, then the mold is pressed into the polymer, creating the desired microstructure. After cooling, you de-emboss the polymer from the mold.
This technique produces parts with high resolution $\approx$ 0.2$\mu$m, but it's slower and more expensive than microinjection molding.
![[Pasted image 20251213170624.png]]
##### In-Situ Casting
In-situ casting is a technique used to create microstructures out of elastomeric polymers, such as PDMS (Polydimethylsiloxane). The process is cheap and used for disposable devices.
You pre weight the two parts of the PDMS (the olygomer base and the curing agent) and mix them together. Then you degas the mixture in a vacuum chamber to remove any air bubbles that could have formed during the mixing process. 
The degassed PDMS mixture is then poured over a master mold, which contains the negative pattern of the desired microstructure. The PDMS is allowed to cure at room temperature or slightly elevated temperatures for a few hours, during which it solidifies and takes the shape of the mold.
After curing, the PDMS microstructure is peeled off from the master mold, resulting in a flexible and durable microstructure.
![[Pasted image 20251206135716.png]]
**PDMS**
PDMS is a silicone-based elastomer that is sold as a two-part liquid mixture: an olygomer base that is made of short polymer chains and a curing agent that cross-links the polymer chains when mixed together. By changing the ratio between the two parts you can change the mechanical and adhesive properties of the final cured PDMS, for example increasing the amount of curing agent will make the PDMS stiffer.
PDMS is gas permeable, optically transparent, biocompatible and chemically inert, making it suitable for biological and chemical applications.
##### Global Planarization - Chemical Mechanical Polishing
To make the surface flat and smooth we use mechanical abrasion combined with chemical etching.
We attach the wafer upside down to a wafer carrier and use a polishing pad with slurry (abrasive particles suspended in a chemical solution) to polish the wafer surface. The two counter rotating motions and the pressure applied help to achieve a uniform planarization.
## References
