
2025-12-06 18:01

Status: 

Tags:

# 08 - Wet & Dry Etching
##### Wet Etching Silicon("HNA")
A common wet etchant for silicon is a mixture of Hydrofluoric acid (HF), Nitric acid (HNO3), and Acetic acid (CH3COOH), known as HNA. 
The wet etching is an isotropic process that normally works better only on polycrystalline silicon or amorphous silicon. But we use a trick, adding Nitric acid to the mixture, which oxidizes the silicon surface to create an amorphous SiO2 layer, which is then etched by the HF in the solution. This way we can etch single crystal silicon as well.
Water or Acetic acid is used to dilute the solution and control the etch rate as shown in the graph in function of the percentage of H2O or CH3COOH, HF, and HNO3. Basically in the graph the points were the 3 concentrations add up to 100%.
![[Pasted image 20251208185640.png]]
##### Anisotropically wet etching of Si
The most famous anisotropic wet etchant for silicon are:
- KOH (Potassium Hydroxide): it etches Si at different rates depending on the crystal orientation. It etches quickly the Silicon(so you can't use it to etch few nanometers), but is not compatible with microelectronic processes since it contains potassium ions that can contaminate the devices moving through the fab. If dissolved in water it produces H2 gas that can create bubbles on the surface acting as a masking layer, creating hillocks and roughness. The only masking layers that can be used with KOH are SiO2 and Si3N4. It is used putting it in a Pyrex glass becker and heating it to 80-90°C to increase the etch rate. The average etch rates at 80°C is $\approx 1 \mu m/min$, but it depends strongly on the crystal orientation, the solution concentration, and the temperature. 
- EDP (Ethylene Diamine Pyrocatechol): it is compatible with microelectronic processes, but is more dangerous to handle.
- TMAH (Tetramethyl Ammonium Hydroxide): most recent
##### Etch Rate of Si in KOH based on Crystal Orientation
![[Pasted image 20251208190921.png]]
We can easily see that the 111 planes etch almost one order of magnitude slower than the 100 and 110 planes. This is due to the atomic density of the planes, the 111 plane has the highest atomic density, so it is more difficult for the etchant to break the bonds and remove atoms from that plane.
##### Etch Rate of Si in KOH based on Temperature and Concentration
![[Pasted image 20251208191104.png]]
 Increasing the temperature increases the etch rates of all planes exponentially, but the ratio between the etch rates of different planes remains almost constant. 
 Increasing the concentration of KOH increases the etch rates up to a certain point, after which the etch rates start to decrease. This is because at high concentrations the solution becomes more viscous, reducing the diffusion of the etchant to the surface and the removal of reaction products from the surface.
 ##### Etch Rate of SiO2 in KOH, Selectivity of Si vs SiO2
![[Pasted image 20251208191241.png]]
The etch rate of SiO2 in KOH is two orders of magnitude lower than that of Si, so we can even use thin SiO2 layers as masking layers for KOH etching of Si.
We have a trade-off between etch rate and selectivity, higher temperatures increase the etch rate of Si, but decrease the selectivity of Si vs SiO2.
##### Hydrofluoric Acid (HF) for SiO2 Etching
At room temperature, HF etches SiO2 but not Si. For this reason, HF is widely used to etch SiO2 layers especially to remove the native oxide from silicon wafers created by exposure to air at room temperature. One of the problems is that it also attacks Aluminum, so it can't be used in processes where Al is present.
The etch rate depends strongly on the concentration, with a maximum etch rate of $\approx 2 \mu m/min$ at 49% concentration. Diluted HF solutions are used to have better control over the etch rate, $\approx 0.1 \mu m/min$ at 5 to 50:1 dilution.
It's super dangerous to handle, since it can penetrate the skin and react with calcium in the bones, causing serious health issues.
It's normally used in buffered solutions (BOE - Buffered Oxide Etch) with ammonium fluoride (NH4F) to control the pH and the etch rate, since normally the HF molecules would rarify quickly in water losing the control of the etch rate.
#### Dry Etching
Dry etching is either plasma based or non-plasma based. The non-plasma based dry etching is basically using wet etchants in vapor phase.
Plasma is used since it can provide directionality to the etching process, creating anisotropic etching and since it has high versatility in terms of parameters that can be tuned to optimize the etching process.
##### Vapor Etching
Some wet etchants can be used in vapor phase to etch materials. For example, XeF2 can be used to etch Si in vapor phase. The process is isotropic and has a high selectivity of Si vs SiO2, Al, and photoresists. It's useful but it produces a rough surface.
The process consists of sublimating solid XeF2 into XeF2 gas at pressure 1 tor, which is then introduced into the etching chamber where it reacts with the Si surface to form SiF4 gas and Xe gas, which are then pumped out of the chamber.
$$Si + 2XeF_2 \rightarrow SiF_4 + 2Xe$$One problem is his high reactivity with water, that can produce HF that will attack other materials in the chamber, so the chamber has to be kept dry.

Another example is the use of HF vapor to etch SiO2. The process requires a chamber where the HF is vaporized fr

##### Dry Etch Chemistries
- For Si, SiO2, and Si3N4, we use fluorine-based chemistries like CF4, SF6, CHF3, C4F8.
- For Al and other metals, we use chlorine-based chemistries like Cl2, BCl3, SiCl4. Chlorine also partially erodes the chamber walls, which can lead to contamination, so normally the chamber will undergo  maintenance and cleaning and will be only used for metal etching.
- For Organic materials and photoresists, we use oxygen plasmas (O2) to ash the organics.
##### Selectivity of Si vs SiO2
CF4 plasmas processes are used to etch Si selectively over SiO2 and SiO2 over Si. 
- **Adding 02:** Adding O2 to CF4 plasmas increases the etch rate of Si, because the oxygen reacts with the CF4 plasma to form CO and CO2, which increases the F concentration in the plasma which enhances the chemical etching of Si.
- **Adding H2:** Adding H2 to CF4 plasmas increases the etch rate of SiO2, because the hydrogen reacts with the fluorine in the plasma to form HF, removing F from the plasma and reducing the chemical etching of Si. This makes the plasma more selective for SiO2 over Si. The etch rate of Si is nearly 0 at 40% H2 in CF4.
So basically F radicals etch Si, so the more F you have, the higher the Si etch rate. O2 helps produce more F, while H2 consumes F to make HF.
![[Pasted image 20251206181405.png]]
##### Anisotropy in Dry Etching
For now we only spoke about chemical etching, which is isotropic. To achieve anisotropic etching in dry etching, we combine chemical etching with bias voltage to create ion bombardment. 
Basically we can add H2 to CF4 to reduce the chemical etch rate of Si, but enhance the bias to have a better physical anisotropic etch. 
This procedure is usually used to etch really small features, where anisotropy is critical.
![[Pasted image 20251206181820.png]]
##### Aspect Ratio
The aspect ratio is defined as the ratio between the height of the feature and its width. It's used both for etching and deposition processes.
![[Pasted image 20251206181938.png]]
##### Deep Reactive Ion Etching (DRIE)
It's a time multiplexed process used to achieve to achieve very high aspect ratio features. It alternates between two steps:
1. **Etching step:** A plasma of SF6 with a substrate bias of 5-30 V is used so that the cations bombard the surface and create anisotropic etching. The SF6 plasma creates F radicals that chemically etch Si.(To explain it better, the neutral F radicals etch the Si isotropically, while the biased $F5^+$ ions bombard the surface and create anisotropy by removing the passivation layer at the bottom of the features). 
2. **Passivation step:** A mixture of C4F8 and Argon is used to deposit a Teflon-like polymer(polymerized CF2) on the sidewalls and bottom of the etched features approximately 50 nm thick. This protects the sidewalls from being etched in the next step. The C to F ratio in the plasma is critical to achieve good passivation without excessive deposition.
3. **Repeat:** The two steps are repeated multiple times to achieve deep etching with high aspect ratios.
![[Pasted image 20251206183306.png]]
![[Pasted image 20251206183321.png]]
## References
