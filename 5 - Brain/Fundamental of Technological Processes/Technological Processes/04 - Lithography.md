
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
- **DUV Lasers:** Deep Ultraviolet (DUV) lasers emit light at wavelengths shorter than 300 nm, to increase resolution. Common DUV laser wavelengths include 248 nm which correspond to the KrF excimer laser, that is composed of a mixture of krypton and fluorine gases, that wouldn't naturally lase, but when provided with energy, it forms an excited dimer that emits DUV light when it returns to the ground state. Normally a pulsed excitation is used to replenish the excited states. $Kr + NF_3 \rightarrow KrF \rightarrow photon + Kr + F$. ArF excimer lasers emit at 193 nm and are used for even higher resolution applications and F2 lasers emit at 157 nm. These shorter wavelengths allow for finer feature sizes, but they also require specialized optics and photoresists that can handle the high energy photons. By reducing the wavelength you also reduce diffraction effects, but you would need to also change the whole lithography system and the next processes to be compatible with these shorter wavelengths. We would normally be able to print a feature size of about half the wavelength, so for 193 nm we can print features down to about 96 nm. Some ArF lasers algo go to 65 nm with immersion lithography.
![[Pasted image 20251203171714.png]]
- **EUV Lithography**: Extreme Ultraviolet (EUV) lithography uses light with wavelengths around 13.5 nm. It works by heating up a tin droplet with a high-energy laser a first time to create a plasma, then a second laser pulse hits the plasma to generate EUV photons. These photons are then collected using mirrors, cause otherwise we would have a point source that would diffract a lot and if used directly on the mask it would heat the mask up and not pass through it well. The mirrors should be able to replicate 70% of the light, so we need multiple mirrors to focus the light on the wafer, to get in the end about 1-2% of the initial light. The roughness of the mirrors should be in the picometer range to avoid scattering the EUV light. It it operated in vacuum because EUV light is absorbed by air. 
![[Pasted image 20251203173520.png]]
- **Electron Beam Lithography (EBL)**: EBL uses a focused beam of electrons to directly write patterns onto the resist layer, direct writing means that we don't need a mask, which is useful for prototyping and small-scale production. Electrons possess a wavelength of 0.2-0.5 $\mathring{A}$. It uses vector scanning, which means that the beam is always on and moves to the desired locations to expose the resist, this leads to high resolution but low throughput. Diffraction is negligible because the wavelength is so small. The main limitation is proximity effects, where electrons scatter within the resist and substrate, causing unintended exposure of nearby areas. 
![[Pasted image 20251203174542.png]]
##### PMMA Resist
PMMA (Polymethyl methacrylate) is a commonly used positive deep-UV and electron beam resist. It has high resolution capabilities, making it suitable for applications requiring fine feature sizes. It has low sensitivity, meaning it requires higher exposure doses compared to other resists, so some sensitizers are added to improve this. 
![[Pasted image 20251203175509.png]]
##### Exposure tools
- **Contact:** The mask is placed in direct contact with the resist-coated wafer. The wafer is all exposed at once, and it's cheap and simple, but the mask can get damaged and particles can cause defects. There's no magnification, so the feature size on the mask is the same as on the wafer. The masks are usually the same size as the wafer, it's difficult to create very large masks, so the industry stopped at the 6 inch wafer masks and a defect on the mask would ruin all the wafers. Contact printing is not used in high volume manufacturing anymore due to these limitations, because it created unacceptable defect levels. The line/gap period is an empirical formula to calculate the magnitude of the resolution of the tool, the best resolution for contact is 0.5-1 $\mu m$:$$2\cdot b_{min} = 3 \cdot \sqrt{\frac{\lambda \cdot z}{2}}$$Where:
	- $b_{min}$ = minimum line/gap width
	- $\lambda$ = wavelength of the exposure light
	- z = resist thickness
![[Pasted image 20251203183721.png]]
- **Proximity:** The mask is placed very close to the wafer, but not in direct contact, a tool is used to adjust the gap between the mask and wafer. This reduces the risk of mask damage and contamination, but diffraction effects become more pronounced, leading to reduced resolution and pattern fidelity, used for printing feature of few $\mu m$. The mask is again the same size of the wafer. The line/gap period for proximity is:$$2\cdot b_{min} = 3\cdot \sqrt{\lambda \cdot (s + \frac{z}{2})}$$Where:
	- s = gap between mask and wafer
![[Pasted image 20251203184201.png]]
- **Projection:** The mask is projected onto the wafer using a system of lenses or mirrors, allowing for high-resolution patterning without direct contact. This method minimizes mask wear and contamination risks, and magnification can be used to reduce the feature size on the wafer compared to the mask without reducing resolution. So even if the mask is placed far away from the wafer, diffraction effects are minimized. The only disadvantages of this method are the high cost and complexity of the projection optics, and the fact that each die on the wafer is exposed sequentially cause of the de-magnification, resulting in lower throughput compared to contact or proximity methods. 
![[Pasted image 20251208233355.png]]
##### Exposure Tools: Projection Steppers and Scanners
Projection lithography systems can be classified into two main types: steppers and scanners.
- **Steppers:** In a stepper system, the entire mask pattern is projected onto the wafer in a single exposure. The wafer is then "stepped" to the next position for subsequent exposures. Steppers are suitable for applications where high resolution and precision are required, but they may have lower throughput compared to scanners due to the need to expose each die individually. The number of steps grows exponentially with the de-magnification factor.(I didn't understand this part well) It takes approximately 6 seconds to expose a wafer die.
- **Scanners:** In a scanner system, the mask and wafer move simultaneously during exposure. The mask is scanned across the wafer while the projection optics continuously expose the resist. This allows for higher throughput compared to steppers, as multiple dies can be exposed in a single pass. Scanners are commonly used in high-volume manufacturing where speed is critical. The scanner can use smaller lenses compared to steppers, because the exposure area is smaller at any given time. It takes approximately 6 seconds to expose a wafer die.
![[Pasted image 20251208234258.png]]
(I didn't understand well )
Water has a diffractive index of 1.44 at 193 nm, so by placing a thin layer of water between the final lens and the wafer, we can effectively reduce the wavelength of the light in the resist to about 134 nm, allowing for smaller feature sizes to be printed. While air has a a refractive index of 1, so the wavelength remains 193 nm. 
So an higher refractive index medium allows for better resolution, because it reduces diffraction effects.
##### Front-Backside Alignment
In front-backside alignment, we need to align features on the front side of the wafer with those on the back side. This is typically done using alignment marks that are visible from both sides of the wafer.
For example in the Piezoresistive Pressure Sensor, we need to align the cavity etched on the backside with the piezoresistive elements on the front side, so that the pressure applied to the diaphragm correctly translates to stress on the piezoresistors. This requires precise alignment techniques to ensure that the features on both sides are properly registered.
![[Pasted image 20251208234814.png]]
**Infrared Alignment**
Infrared (IR) alignment is a technique used to align features on the front and back sides of a wafer using infrared light. Silicon is transparent to infrared light, allowing us to see through the wafer and align features on both sides simultaneously.
In this method, infrared light is shone through the wafer, and cameras or sensors detect the alignment marks on both sides. The system then adjusts the position of the wafer or mask to achieve proper alignment based on the detected marks.
![[Pasted image 20251208235326.png]]
**Mask Alignment**
If a sample is not infrared transparent, we can use mask alignment techniques to align features on both sides of the wafer. This involves using a focusing and storage system to capture images of the alignment marks on the mask and then adjust the wafer position accordingly.
![[Pasted image 20251208235633.png]]
##### Reflection and Standing Waves 
When light passes through the photoresist and reaches the substrate, some of it gets reflected back into the resist layer. Depending on the materials used and their refractive indices, this reflected light can be out of phase with the incoming light, leading to interference effects. These interference effects can create standing waves within the resist layer, resulting in variations in exposure intensity at different depths. This can lead to uneven development of the resist. 
So there can be an alternation of high intensity, so faster development, and low intensity, so slower development, regions within the resist layer.
![[Pasted image 20251209000016.png]]
![[Pasted image 20251209000025.png]]
To mitigate these effects, there are 2 main strategies:
- depositing a top anti-reflective coating (TARC) on top of the resist layer for a specific wavelength, so that the wavelength is absorbed and not reflected back.
- allowing the formation of standing waves, and after exposure, performing a post-exposure bake (PEB) to smooth out the variations in exposure intensity by promoting diffusion of the photoactive compounds within the resist layer. This helps to even out the chemical changes induced by the standing waves, leading to more uniform development. It's normally done at 110-130°C for 1-2 minutes.
![[Pasted image 20251209000337.png]]
##### Develop Photoresist
After exposure, the photoresist needs to be developed to remove the soluble areas and reveal the underlying substrate. The development process involves immersing the wafer in a chemical developer solution that selectively dissolves the exposed or unexposed areas of the resist, depending on whether a positive or negative resist is used. The timing is important to neither under-develop nor erode too much of the resist.
Another developing method is spray development, where the developer solution is sprayed onto the wafer surface using nozzles. This allows for more precise control over the development process and can help achieve better uniformity across the wafer.
![[Pasted image 20251209000549.png]]
##### Hard Bake
After development, a a hard bake is performed to further harden the remaining photoresist, evaporate any residual solvents, and improve adhesion to the substrate. This step enhances the resist's resistance to subsequent processing steps, such as etching or deposition. It can also fill in pinholes or defects in the resist layer. The hard bake is typically done at the same temperature as the soft bake, but for a longer duration, usually around 2-5 minutes.
#### Etching vs Lift-off
In microfabrication, both etching and lift-off are techniques used to create patterns on a substrate, but they operate in fundamentally different ways.
- **Etching:** In etching, we start with a substrate that has a layer of material (like metal or oxide) deposited on it. We then apply a photoresist layer and pattern it using lithography. The exposed areas of the substrate are then removed using either wet chemical etching or dry plasma etching, leaving behind the desired pattern. Etching is typically used when we want to create features by removing material from the substrate.
- **Lift-off:** In lift-off, we first pattern the photoresist layer using lithography, creating openings where we want to deposit material. We then deposit the desired material (like metal) over the entire surface, including on top of the photoresist. After deposition, we immerse the wafer in a solvent that dissolves the photoresist, lifting off the unwanted material and leaving behind the desired pattern on the substrate. Lift-off is typically used when we want to create features by adding material to the substrate.
![[Pasted image 20251209001247.png]]

If we want to create a multilayer structure, maybe we can't find the etchants that selectively etch only one layer without affecting the others, so we would use lift-off instead. But lift-off has limitations in terms of feature size and aspect ratio, since the deposited material can create overhangs that make it difficult to achieve very small features, resulting in a broken pattern.
A way to improve lift-off is to use image reversal resists, which create an undercut profile in the resist layer after development. This undercut helps to prevent the deposited material from bridging over the resist sidewalls, making it easier to achieve clean lift-off and better-defined patterns.
This type of resist is different from normal positive or negative resists, because it goes through multiple steps:
![[Pasted image 20251209001722.png]]
(this slide is important )
##### Models and Simulations
To optimize the lithography process and predict the outcome of different parameters, various models and simulations are used.

## References
