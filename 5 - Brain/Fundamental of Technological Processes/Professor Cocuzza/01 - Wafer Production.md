
2025-09-23 11:28

Status: 

Tags: [[Semiconductor]] [[Wafer]] [[Silicon]]

# Wafer Production

### Starting Material
In the production of microstructures, in this case, wafers, we normally use semiconductors, since they are partially conductive and their electrical properties can be locally controlled through methods like doping, electric fields, light or heat. 

The most used semiconductor in this field is Silicon(Si).
We cite some other semiconductors: Gallium Arsenide(GaAs), which is used mainly for high-frequency applications, Indium Phosphide(InP), which is used for optoelectronic devices, Silicon Carbide(SiC) and Gallium Nitride(GaN), which are used for high-power and high-temperature applications.

To produce wafers out of Silicon we need to respect some important needs: 
- High purity: Silicon must be purified to be able to control doping to control the electrical properties of the wafer.  The usual purity level accepted is $\lt 1$ over $10^9$ atoms of silicon.
- Crystal: Silicon atoms must be arranged be arranged in a very regular crystal structure, we need to minimize crystallographic defects, cause otherwise they could worsen the conductive properties of the wafer. (Sometimes in quantum devices we introduce ourselves defects to exploit their quantum properties, such as radioactive decay of certain isotopes).
- Crystal structure: all the Silicon atoms must be ordered in a monocrystalline structure. Other famous structures are polycrystalline(multiple monocrystals joined together by a defect) and amorphous(no order at all).

The perfectly pure monocrystalline Silicon is not found in nature, so we need to produce it through a series of steps.
- The starting material is a relatively pure quartz based sand(SiO2).
- Silicon Refining: in the first purification step the sand is reduced in an arc furnace with coal, coke and wood chips. The product is metallurgical grade silicon(MGS), which is about 98% pure. This is not enough for wafer production, so we need to further purify it. The formal way to see the step is: $SiO_2 + 2C \rightarrow Si (solid) + 2CO (gas) \space @ 2000^\circ C \space for \space 8 \space days$.
- Silicon can't be purified any further, so we basically need to convert it into another chemical compound, purify that and then convert it back to Silicon. 
- We crush the MGS into a powder and react it with hydrogen chloride(HCl) to obtain trichlorosilane(SiHCl3)(TCS). TCS is a liquid at room temperature, so impurities are removed through fractioned distillation. The reaction is: $3HCl (gas) + Si (solid) \rightarrow SiHCl_3 (gas) + H_2 (gas) \space @ 325^\circ C$.

Fractioned distillation is a method that exploits the different boiling points of the substances in a mixture the different boiling points of the substances in a mixture. For example, to separate the different compounds of crude oil, we heat it up into a mixture called the feed, which is then vaporized and sent into a tall column called the distillation column. The column is hotter at the bottom and colder at the top, so the different compounds condense at different heights according to their boiling points. The compounds with higher boiling points condense at the bottom, while those with lower boiling points condense at the top. The distilled products are collected at different heights of the column.
Fractional distillation is the separation of a mixture into its component parts, or fractions, based on differences in boiling points using a distillation column.

Now we have TCS, which is purified, but we need to convert it back to Silicon. The purified TCS is reduced with hydrogen(H2) to obtain electronic grade silicon(EGS). 
This process is called the Siemens process and the reaction is: $SiHCl_3 (gas) + H_2 (gas) \rightarrow Si (solid) + 3HCl (gas) \space @ 1100^\circ C$.
The technique used is chemical vapor deposition(CVD), that is why we use H2 as the carrier to generate bubbles of SiHCl3(like blowing bubbles in a soda bottle). Then the bubbles are sent into a reaction chamber containing a heated silicon rod, where the reaction happens and the silicon deposits on the rod. After a few days the result is ana extremely pure polycrystalline silicon, which will be the raw material for the next step.

### Czochralski Process
Starting from the rod of polycrystalline silicon, we need to produce a monocrystalline silicon ingot. This is done through the Czochralski process, which consists of melting the polycrystalline silicon in a crucible at about $1420^\circ C$. A small seed crystal of monocrystalline silicon is dipped into the molten silicon and then slowly pulled upwards while rotating it. The molten silicon solidifies on the seed crystal, recreating the seed pattern and forming a large monocrystalline ingot as it is pulled out of the melt. The diameter of the ingot can be controlled by adjusting the pulling rate and temperature. The result is a cylindrical ingot of monocrystalline silicon, which can be several feet long and weigh hundreds of pounds.

The temperature is selected so that the silicon is just above its melting point, to ensure that the seed doesn't melt when dipped into the molten silicon. 

The pullup speed is inversely proportional to the diameter of the ingot, so a slower pullup speed results in a larger diameter ingot. There exists different diameters of ingots for different applications, but in general larger diameters are preferred since they allow for more wafers to be produced from a single ingot, reducing production costs. 

It basically works thanks to epitaxial growth, that is the growth of a crystalline layer on a crystalline substrate, where the layer follows the crystallographic orientation of the substrate. Since the atoms prefer to bond in the lowest energy configuration, they will arrange themselves in the same pattern as the seed crystal.

During the pulling process, below the seed, is created a neck by pulling faster, this is done to prevent defects from the thermal shock of the seed to propagate into the ingot. Then you progressively slow down the pull rate to increase the diameter of the ingot to the desired size.
The bottom part of the ingot prevents shock back into the body when the ingot is finally detached from the melt.
The excessive parts will be reused.

Normally impurities are added to the melt to dope the silicon, depending on the desired electrical properties of the final wafer. There are dopants that help with conductivity. The only problem is that the dopant normally prefers to stay in the melt, so as the ingot is pulled out of the melt, the concentration of the dopant in the melt increases, leading to a non-uniform doping profile along the length of along the the ingot. The lower part of the ingot will be more doped than the upper part. 

### Liquid Encapsulated Czochralski(LEC)
If we want to create GaAs wafers we need to modify the CZ technique, since Ga is solid and As in a gas and they have different melting points and different vapor pressures(vapor pressure means how slowly does the material evaporate) and the evaporation of the two could result in toxic fumes and non-uniform crystal growth.

The solution is to make so that Arsenic can't escape the chamber, by putting it under Gallium. But still, as the Ga melts the As could easily escape through, so we use a layer of Boric Oxide(B2O3) about 1 cm thick. The Boric Oxide does not react with GaAs, it melts at $500^{\circ} C$ and seals the crucible, while Ga and As start reacting at $800^{\circ} C$. At the end you will need to mechanically remove the Boric Oxide.

The all chamber is also externally pressurized(?).

### From Boule to Wafers
1. Ingot Cropping: this phase consists in cutting the extremities of the ingot that contains the highest defect concentration
2. Ingot Inspection: we need to check:
	1. Size: if there are any parts of the ingot where it's undersized(in that case we break the all ingot and restart the process)
	2. Resistivities: control the resistivities at the top and bottom of the ingot to assess the gradient of the dopant, the final result will be in function of the location
	3. XRD: check of the crystallographic orientation of the ingot
	4. Almost 50% of the ingots gets rejected
3. Shaping of the ingot: in the pulling phase due to the speed could vary and it can create waves at the ingot surface. In this process, through mechanical abrasion, the ingot is rounded and made of the correct diameter
4. Flat(s) Grinding: we creates flat zones so that the wafer can be correctly placed in the device
5. Ingot Sawing
6. Edge Grinding: after sawing, some peaks of matter remain on the peripheral zones of the slice. So we basically make the edges rounder.
7. Wafer Lapping and Grinding: the thickness and section varies after sawing, you could get a tapered or a bowed wafer. In order to improve the surface quality the slices are polished. The end result of this phase is a wafer mechanically flat on both sides(like the opaque side of the final wafer). To get it optically flat you need to proceed to the next phase
8. Wafer Polishing: the final result of this phase will be a mirror-like wafer with a roughness of 1-2nm. It is a procedure similar to lapping, but the polishing solution is less aggressive with a mixture containing smaller grains of alumina or diamond(use in lapping as well). So after the mechanical abrasion we use some chemicals. On the market there are mainly two types of wafers: SSP(Single Sided Polished) and DSP(Double Sided Polished). The mirror-like feature is necessary cause, for example, in lithography(basically light is projected through a mask on the wafer to create a quantum device) we need the precision of nanometers, or else we couldn't create or have the wanted effects for our quantum devices. (Mics are made using DSP wafers)
9. Wafer Cleaning: the edge can't be used to fabricate quantum devices cause it contains defects(I think). Larger wafers are obviously better cause of productions costs.

If you break the wafer it will follow the crystallographic orientation, super cool.


## References
