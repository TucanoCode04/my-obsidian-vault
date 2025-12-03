
2025-12-02 16:05

Status: 

Tags:

# 04 - Lithography
There are 4 main types of micro/nano technologies:
- Selection: Lithography
- Additive: Deposition, Thermal oxidation, etc
- Subtractive: Etching
- Modification: Doping, Annealing, etc

Without lithography, none of the other micro fabrication processes would be possible, since lithography is used to create the patterns that define the structures on a microchip.

Photolithography is the technique to select, to transfer a pattern from a mask to a photo-sensitive polymer layer (photoresist) on the substrate. So it's used to transfer the circuit patterns onto the silicon wafer.
The patterned photoresist acts as a mask during subsequent etching or deposition processes.
Lithography is basically the process by which a pattern is transferred from a layout on a mask to the surface of a wafer.

You basically provide energy to a photosensitive material (photoresist) through a patterned mask, which causes chemical changes in the photoresist, from insoluble to soluble or vice versa, depending on the type of photoresist used.
After developing, the exposed or unexposed areas of the photoresist are removed, revealing the underlying substrate in those areas.
![[Pasted image 20251202174117.png]]
After every step, there is usually a baking step to harden the photoresist and improve adhesion to the substrate and to remove any residual solvents.

For the realization of a single device, multiple lithography steps are required, each corresponding to a different layer of the device, so we need a method to align the different layers accurately, this is called mask alignment.
##### Mask Generation
Masks are usually made of quartz or soda lime glass, where quartz is preferred for its superior optical properties. Quartz has a transmission of over 90% even at short wavelengths (e.g., deep UV), making it ideal for high-resolution lithography processes. 
The creation of masks is a fight against diffraction, because diffraction limits the minimum feature size that can be accurately transferred onto the wafer. To explain it briefly, when light passes through a small aperture (like the features on a mask), it spreads out due to diffraction, which can blur the edges of the features being projected onto the wafer.

The masks are produced using slower and more precise lithography techniques, such as electron beam lithography (EBL) or laser writing, which can create very fine features with high accuracy. Normally the feature are created line by line, which is a slow process but allows for very high resolution. 

Normally Chromium is used as the opaque material on the mask because it has good adhesion to quartz and can be patterned with high resolution. (Search it up better)
##### Alignment Marks
The alignments marks are special patterns on the wafer and the mask that are used to align the mask to the wafer or other masks during the lithography process. We create crosses for the X and Y directions, and sometimes we also create rotational alignment marks to ensure proper angular alignment.
A perfect alignment is not possible, so the overlay accuracy is specified, which is the maximum allowable deviation between the intended and actual position of the features on the wafer after alignment.
The alignment is a bottleneck for achieving smaller feature sizes, because as the features get smaller, the required overlay accuracy becomes tighter.
##### Lithographic Process Flow
![[Pasted image 20251202184543.png]]
##### Wafer Preparation
Wafers will have a layer of native oxide on the surface, which is usually removed by baking at 130/200°C to dehydrate the surface, this way the adhesion of the photoresist to the wafer is improved. 
We further improve the adhesion by applying an adhesion promoter, such as HMDS (Hexamethyldisilazane), which reacts with the hydroxyl groups on the silicon surface to create a hydrophobic surface that enhances the bonding of the photoresist.
So the wafer preparation steps are:
- Dehydration bake
- Primer Vapor Coating
##### Resist Spin-on
Photoresists are commercialized as liquids that need to be applied to the wafer surface uniformly, because it's easy to do so, we use spin coating.
We create a vacuum between the wafer and the chuck to hold the wafer in place, then we dispense a droplet of photoresist in the center of the wafer.
We first spin the wafer at a low speed to spread the resist evenly through centrifugal force, then we increase the speed to thin the resist to the desired thickness.
We will still have some edge bead, which is a thicker ring of resist around the edge of the wafer, this is usually removed later in the process. 
This is a four stage process:
- deposition
- spin-up
- spin-off
- evaporation
![[Pasted image 20251203105215.png]]
The final thickness of the resist layer depends on the spin speed, viscosity of the resist, and the duration of spinning:$$t = K \cdot S \cdot \left( \frac{v}{\omega^2 \cdot R^2} \right)^{1/3}$$Where:
- t = final thickness
- K = constant depending on resist and solvent properties
- S = fraction of solids in the resist
- v = viscosity of the resist
- ω = angular velocity (spin speed)
- R = radius of the wafer
Obviously, higher spin speeds lead to thinner resist layers.
![[Pasted image 20251203105537.png]]
We are normally presented with a datasheet that gives us the relationship between spin speed and resist thickness for a specific resist![[Pasted image 20251203105612.png]].
##### Soft Bake
After spin coating, the resist layer contains residual solvents that need to be removed to improve adhesion and stability. The solvent were used to make it liquid, but they can cause problems during exposure or the resist could fall off the wafer if not removed.
We perform an hot plate bake at a temperature typically between 90-120°C for a duration of 30 seconds to 2 minutes, the problem is to maintain uniform temperature across the wafer to avoid stress and defects in the resist layer.
The higher the temperature, the less residual solvent remains, but we have to be careful not to exceed the glass transition temperature of the resist, which could cause it to flow and lose pattern fidelity.
##### Photoresists
Photoresists are photosensitive organic mixtures which contains:
- Inactive polymer resins: non sensitive to light, provide mechanical strength and adhesion to the substrate. For example to withstand etching processes HF, HNO2, HNO3
- Photoactive compounds (PACs): they make the resist soluble after exposure to light.
- Solvents: to make the resist liquid for spin coating.
- Other Stuff: surfactants, leveling agents, sensitizers, dyes, etc.
We decide on the type of photoresist based on the application, resolution requirements, and process compatibility. Depending on the properties of the resist:
- Polarity(positive or negative):
	- Positive Resists: where the light exposed areas become soluble and will get etched away during development. It works on Chain Scission Mechanism. They are preferred for high resolution applications because they can achieve smaller feature sizes and have better process control.
	- Negative Resists: where the light exposed areas become insoluble and remain after development. It works on Cross-Linking Mechanism. They are used when high aspect ratio structures are needed, as they tend to have better adhesion and durability.
- Resolution: the minimum feature size that can be reliably produced. It's related to processes like source and development. Thinner layers generally yield higher resolution. Positive resists typically offer better resolution than negative resists, thanks to their smaller size of polymer fragments after exposure.
- Sensitivity: the amount of exposure energy required to achieve the desired chemical change, depending on positive(completely eliminated) or negative(fully cross-linked). 
- Contrast: the ability to distinguish between exposed and unexposed areas during development. Slope of the curve($\gamma= \frac{\Delta E}{\Delta x}$ where E is exposure dose and x is the normalized remaining resist thickness).
- Viscosity: affects the thickness of the resist layer after spin coating.
- Absorption Spectrum: the wavelength range over which the resist is sensitive to light.
- Adhesion: how well the resist sticks to the substrate.
- Etch Resistance: how well the resist can withstand etching processes without degrading.
- Surface tension: affects the uniformity of the resist layer during spin coating.
- Storage and Handling: resist stability over time and under different environmental conditions.
##### Positive Resist 
In positive resists, the photoactive compound (PAC) undergoes chain scission, basically breaking the long polymer chains into smaller fragments when exposed to light to make them more soluble in the developer solution.
This is used to replicate the mask pattern onto the resist layer, where the exposed areas become soluble and are removed during development, leaving behind the unexposed areas.
![[Pasted image 20251203161643.png]]
##### Negative Resist
In negative resists, the PAC undergoes cross-linking, where the polymer chains form bonds with each other upon exposure to light, creating a network that is less soluble in the developer solution.
This means that the exposed areas remain after development, while the unexposed areas are washed away.
![[Pasted image 20251203161728.png]]
##### HD Curve
![[Pasted image 20251203161248.png]]
The HD curve shows the relationship between the exposure dose and the remaining resist thickness after development. It helps us understand how the resist responds to different exposure levels.
Basically at E0, we have no exposure, so the entire resist layer remains after development. We hit a threshold dose E1, where the exposed areas start to dissolve, leading to a decrease in remaining thickness. At dose ET, the exposed areas are completely removed, leaving only the unexposed regions intact.(For positive resist)
##### Sensitivity and Contrast
Since the exposure source is constant in power $\frac{E}{t}$, we can express the sensitivity in terms of exposure time instead of dose. A resist with high sensitivity requires a shorter exposure time to achieve the desired chemical change, which is beneficial for high throughput manufacturing.
Contrast is a measure of how sharply the resist transitions from unexposed to fully developed. A high contrast resist will have a steep slope in the HD curve, meaning that small changes in exposure dose result in significant changes in remaining thickness. This is important for achieving precise patterning and minimizing feature blurring.
![[Pasted image 20251203162349.png]]
##### Photoresist Exposure
We use different types of light sources for exposure, depending on the desired resolution and throughput:
- **HG Lamps**: Mercury lamps are commonly used for general lithography applications. Electrons are accelerated and collide with mercury plasma, which emits light at specific wavelengths called lines. Obviously the shorter the wavelength, the higher the resolution we can achieve, since it will match the feature size better. The common lines are:
	- I-line (365 nm): used for standard resolution applications.
	- G-line (436 nm): used for lower resolution applications.
	- H-line (405 nm): used for high-resolution applications.
	You can either use the full spectrum to have higher exposure energy, so less exposure time and higher throughput, or you can use filters to select specific lines for better resolution. 
	Different photoresists are formulated to be sensitive to specific wavelengths, so we choose the resist based on the light source and vice versa.
![[Pasted image 20251203165620.png]]
- **UV LEDs**: UV LEDs are becoming increasingly popular due to their energy efficiency, long lifespan, and ability to replicate specific wavelengths. They can be switched on and off quickly, allowing for rapid exposure cycles, compared to traditional lamps that require warm-up time. As always the problem is diffraction limits. 
![[Pasted image 20251203170059.png]]
- **DUV Lasers:** Deep Ultraviolet (DUV) lasers emit light at wavelengths shorter than 300 nm, to increase resolution. Common DUV laser wavelengths include 248 nm which correspond to the KrF excimer laser, that is composed of a mixture of krypton and when 

## References
