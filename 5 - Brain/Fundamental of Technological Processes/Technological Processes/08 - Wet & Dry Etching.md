
2025-12-06 18:01

Status: 

Tags:

# 08 - Wet & Dry Etching

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
