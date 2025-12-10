
2025-12-09 20:40

Status: 

Tags:

# 07 - Doping
#### Silicon Doping
Doping is the intentional introduction of external atoms (impurities) into a semiconductor lattice to modify its electrical properties, either to increase conductivity or to increase resistivity. The resistivity of Silicon can be modified up to 8 orders of magnitude through doping, basically going from an insulator to a good conductor.
There are two types of dopants:
- n-type dopants: These are elements from group V of the periodic table, such as Phosphorus (P), Arsenic (As), and Antimony (Sb). They have five valence electrons, one more than Silicon. When introduced into the Silicon lattice, they donate an extra electron, which becomes a free charge carrier in the conduction band, increasing the material's conductivity. They are called donor dopants.
- p-type dopants: These are elements from group III of the periodic table, such as Boron (B), Aluminum (Al), and Gallium (Ga). They have three valence electrons, one less than Silicon. When introduced into the Silicon lattice, they create "holes" (missing electrons) in the valence band, which act as positive charge carriers, also increasing the material's conductivity. They are called acceptor dopants.

When you introduce dopants into Silicon, they first become interstitial, not forming bonds with the Silicon atoms, but after some time or after a thermal annealing process, they move to substitutional sites, replacing Silicon atoms in the lattice and forming bonds with the surrounding Silicon atoms.
Silicon has 5.2 $\times 10^{22}$ atoms/cm$^3$, so the normal concentration of dopants is much lower than that, typically in the range of 10$^{13}$ to 10$^{20}$ atoms/cm$^3$.
The elements mentioned before are good dopants because they have greater solid solubility in Silicon, meaning they can be introduced in higher concentrations without forming precipitates or secondary phases that could degrade the material's properties.
Other than electrical properties, doping also affects other properties of Silicon, such as:
- Optical properties: Doping can change the absorption and emission spectra of Silicon, which is important for optoelectronic devices. You can introduce Chromium to create a Ruby laser.
- Chemical properties: Doping can influence the chemical reactivity and corrosion resistance of Silicon. For example, heavily Boron doped Silicon can be more resistant to oxidation.
- Piezoelectric properties: Doping can induce piezoelectric effects in Silicon, which can be utilized in sensors and actuators.(look this fucking piezoresistor up)

For a doping process to be effective we need to define 3 main parameters:
- Dopant Distribution: $N(x)$ or $C(x)$, which describes how the concentration of dopants varies with depth $x$ in the Silicon substrate.
- Total Dose: $Q$, which is the total number of dopant atoms introduced per unit area (atoms/cm$^2$). It's calculated by integrating the dopant distribution over depth: $Q = \int_{0}^{\infty} N(x) dx$
- Junction Depth: $x_j$, which is the depth at which the dopant concentration equals the background concentration of the substrate. Basically telling us how deep the dopants have penetrated into the substrate, so the result of our doping process.(The background concentration is the concentration of dopants already present in the substrate before any doping process is applied, usually very low)
##### Ion Implantation
To introduce dopants into Silicon we can use different methods, the most common and precise one is Ion Implantation. Using an ion implanter, we can ionize the dopant atoms and accelerate them using an electric field to high energies(3keV to 3MeV), then we direct the ion beam towards the Silicon substrate. 
The ionic beam scans the wafer surface vertically and horizontally to ensure uniform doping across the entire wafer. When the high-energy ions collide with the Silicon atoms, where there's no mask, they penetrate the surface and come to rest at a certain depth, creating a dopant distribution profile.
The depth at which the ions come to rest depends on the implantation energy, the mass of the ions, and the angle of incidence. Higher energies result in deeper penetration, while heavier ions tend to have shallower penetration due to increased collisions with the Silicon atoms.
Just a small side note on different energies:
- deposition energies, low, few keV
- sputtering energies, medium, tens to hundreds of keV
- implantation energies, high, hundreds of keV to MeV

This process can be done at room temperature, so we can use polymeric photoresist masks without worrying about thermal degradation.
So the process is fast: from lithography to create the mask, to implantation, directly. Instead of etching another material before implantation.
Other characteristics of ion implantation:
- instant off and instant on control of dopant dose
- precision control through monitoring in situ
- ability to increase implant energy to penetrate thin films
- the peak concentration of dopants is always buried below the surface, reducing surface damage
- a mass separator is used to select the desired ion species, allowing each implanter to handle multiple dopant types

The only cons is that the implantation process damages the Silicon crystal structure, creating defects and dislocations that can affect the electrical properties of the material. To repair this damage, a thermal annealing step is typically performed after implantation, which allows the Silicon lattice to recrystallize and the dopant atoms to move to substitutional sites(dopant activation).
##### Implanter Components
The main components of an ion implanter are:
- Ion Source: This is where the dopant atoms are ionized by electron cascading from tungsten filaments, creating a plasma of ions.
- Extraction region: Here, an electric field is applied to extract the ions from the plasma and accelerate them using a negative potential.
- Mass Analyzer: 


##### Sheet Resistance
The sheet or square resistance is a measure of resistance of a portion of material that has a uniform thickness. It's commonly used in semiconductor and thin film applications to characterize the electrical properties of thin layers.
To calculate the sheet resistance we can start with Ohm's law:
$$R = \frac{\rho L}{A} = \frac{\rho}{t} \frac{L}{W} = R_s \frac{L}{W}$$Where:
- $R$ is the resistance
- $\rho$ is the resistivity of the material, meaning how strongly the material opposes the flow of electric current
- $L$ is the length of the material
- $A$ is the cross-sectional area
- $t$ is the thickness of the material
- $W$ is the width of the material
- $R_s$ is the sheet resistance, defined as $R_s = \frac{\rho}{t}$
- $L/W$ is the number of squares in the material

It's a method use to translate a layout through different process steps, for example if we have a sheet resistance of 10 Ω/sq and we want a total resistance of 100 Ω, we can easily calculate that we need 10 squares of that material.

In the real case scenario, the sheet resistance is not constant across the wafer, since the dopant concentration can vary due to process variations, resulting in an higher conductivity area where the dopant concentration is higher, and an higher resistivity area where the dopant concentration is lower.
$$R_s = \frac{\rho}{t} = \frac{1}{\int_{x_{j1}}^{x_{j2}} \sigma(x) dx}$$Where: 
- $\sigma(x)$ is the conductivity at depth $x$, which depends on the dopant concentration at that depth
- $x_{j1}$ is the first junction depth, meaning the depth where the dopant concentration starts to increase significantly
- $x_{j2}$ is the second junction depth, meaning the depth where the dopant concentration returns to the background level

The junction depths are calculated based on $C_b$, which is the background concentration of the substrate(basically the dopant concentration before any doping process is applied).(look it up better)
![[Pasted image 20251209230956.png]]

The function $\sigma(x)$ depends on the type of dopant used:
- n-type dopants: $\sigma(x) = q \mu(x) n(x)$
- p-type dopants: $\sigma(x) = q \mu(x) p(x)$
Where;
- $q$ is the elementary charge
- $\mu(x)$ is a function of the mobility of charge carriers at depth $x$, which can vary with dopant concentration and temperature
- $n(x)$ is the electron concentration at depth $x$ for n-type doping
- $p(x)$ is the hole concentration at depth $x$ for p-type doping

We can better calculate the sheet resistance using the following formula:
$$R_s = \frac{1}{q \int_{x_{j1}}^{x_{j2}} \mu(x) (N_{A,D}(x) - N_b) dx}$$Where:
- $N_{A,D}(x)$ is the dopant concentration at depth $x$, either acceptor concentration for p-type doping or donor concentration for n-type doping
- $N_b$ is the background concentration of the substrate
(check N_b and C_b better)
##### Implanting Through a Mask
The implantation process can be controlled using a mask, to basically decide where the peak concentration of dopants, depicted by the gaussian curve, will be located.
![[Pasted image 20251210112049.png]]
We can calculate the fraction transmitted through the mask:$$FT= \frac{\int_{d}^{\infty} N(x) dx}{\int_{0}^{\infty} N(x) dx}$$Where:
- $d$ is the thickness of the mask
- $N(x)$ is the dopant concentration at depth $x$, following a gaussian distribution
$$N(x) = N_p e^{-\left(\frac{x - R_p}{\Delta R_p \sqrt{2}}\right)^2}$$Where:
- $N_p$ is the peak concentration of dopants
- $R_p$ is the range of implantation, meaning the depth at which the peak concentration occurs
- $\Delta R_p$ is the standard deviation of the implantation range, indicating how spread out the dopant distribution is around the peak, also called straggle
Resulting in:$$FT = \frac{1}{2} erfc\left(\frac{d - R_p}{\Delta R_p \sqrt{2}}\right)$$Where erfc is the complementary error function.
Let's deeply analyze this equation:
- When $d << R_p$: The mask is much thinner than the implantation range, meaning most of the dopants will penetrate through the mask. In this case, $FT \approx 1$, indicating nearly all dopants pass through.
- When $d \approx R_p$: The mask thickness is approximately equal to the implantation range. Here, $FT \approx 0.5$, meaning about half of the dopants penetrate through the mask.
![[Pasted image 20251210113419.png]]
- When $d >> R_p$: The mask is much thicker than the implantation range, resulting in most dopants being blocked. In this scenario, $FT \approx 0$, indicating that very few dopants pass through the mask.

Suppose that we want to minimize the fraction transmitted through the mask, we can increase the thickness of the mask $d$, or we can choose choose an implantation energy $E$ that results in a smaller range of implantation $R_p$, or even reduce the straggle $\Delta R_p$ by selecting an appropriate ion species or implantation conditions.
So the degrees of freedom are the thickness of the mask $d$ and the material properties that influence $R_p$ and $\Delta R_p$.(Since they are the depending on the mask material and not on silicon)
So that we maximize the argument of the error function, which will minimize the fraction transmitted through the mask.
We now show a graph of the minimum mask thickness in function of the implantation energy for different materials.
![[Pasted image 20251210113316.png]]
##### Silicon on Insulator (SOI) wafers
The CMOS inverters are subject to parasitic capacitances that slow down the switching speed and increase power consumption.
An inverter is made by connecting a pMOS and an nMOS transistor in series with a Field Oxide in between them. The pMOS transistor has the p sites immersed in an n-well.
The main parasitic capacitances in a CMOS inverter are:
- NPN junction capacitance: between the n-well and the p-type substrate
- PNP junction capacitance: between the p-type source/drain regions and the n-well
They are parasitic because they are not intentional, but they are a consequence of the device structure and operation, and they affect the performance of the inverter by slowing down the switching speed and increasing power consumption.
![[Pasted image 20251210114201.png]]
To reduce these parasitic capacitances, we can use Silicon on Insulator (SOI) or Silicon on Sapphire (SOS) wafers.
SOI wafers consist of a thin layer of silicon(2 to 100 $\mu m$) on top of a buried oxide layer, which is on top of a silicon substrate.
This structure effectively isolates the active silicon layer from the bulk substrate, significantly reducing the parasitic capacitances.
![[Pasted image 20251210114257.png]]
The buried oxide is typically made of silicon dioxide (SiO2), through thermal oxidation so its thickness ca vary between 0.5 to 2 $\mu m$.

But how do we obtain the monocrystalline silicon layer on top of the buried oxide? There are 3 main methods:
- Separation by IMplantation of OXygen (SIMOX): In this method, a gaussian profile of oxygen ions is implanted into a silicon wafer at high energy. The wafer is then annealed, not to repair the damage caused by the implantation, but to cause the implanted oxygen atoms to react and form a buried oxide layer. The silicon above the buried oxide remains monocrystalline, while the silicon below becomes polycrystalline due to the implantation damage.
![[Pasted image 20251210115537.png]]
- Bond and Etch Back SOI (BESOI): This method involves bonding two silicon wafers together using fusion bonding. One or both wafers have a thin oxide layer on their surfaces. After bonding, one of the wafers is thinned down by grinding and chemical etching to achieve the desired thickness of the top silicon layer. It-s a little more expensive since you need 2 wafers and one of them is wasted.
![[Pasted image 20251210115549.png]]
- Smart Cut™ Technology: We start by oxidizing a silicon wafer to create a thin oxide layer on its surface. Next, we implant hydrogen ions into the wafer at a specific depth to create a weakened layer. The wafer is then bonded to another silicon wafer, which may also have an oxide layer. After bonding, the wafer is subjected to thermal annealing, which causes the implanted hydrogen ions to form microbubbles at the weakened layer. This leads to a controlled splitting of the wafer along this layer, transferring a thin layer of silicon onto the second wafer. Finally, any remaining surface irregularities are smoothed out through chemical-mechanical polishing (CMP).
![[Pasted image 20251210115942.png]]
## References
