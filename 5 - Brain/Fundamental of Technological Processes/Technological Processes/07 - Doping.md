
2025-12-09 20:40

Status: 

Tags:

# 07 - Doping




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
