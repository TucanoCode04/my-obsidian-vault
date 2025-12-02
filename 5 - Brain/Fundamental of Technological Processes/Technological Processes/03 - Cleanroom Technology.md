
2025-12-02 14:37

Status: 

Tags:

# 03 - Cleanroom Technology
It's needed to work in a clean environment to avoid contamination of sensitive components. 
Contamination can ruin devices, a single ruined component can lead to the failure of an entire system. Leading to a low yield in production and high costs.
The poisoned equipment must be removed from the production line, reducing throughput and increasing costs.
Contamined products can also pose a safety risk to employees and end-users. Greatly increasing costs, liabilities and damaging the reputation of a company.

Most of contamination comes from the working humans themselves. Humans shed skin particles, hair, perfume or smoke, walk with dust on their shoes and carry microbes on their bodies. Human external skin has the highest exchange rate, we completely renew our skin every month. 
So humans should be protected with special clothing to reduce contamination.
Another contamination source is the machinery and tools used in production. They are subject to aging and wear, abrasion, corrosion and outgassing. valves, pumps and filters are prone to lose particles into the environment. 
The cleanroom equipment is in fact installed "through the wall", meaning that the clean and usable area in situated inside the cleanroom(white area), while the machinery is placed outside the cleanroom(grey area).
Other sources of contamination are raw materials, in fact we tend to use extremely pure raw materials, like deionized water, ultra pure chemicals and high purity gases. The processes themselves can also generate contamination, like chemical reactions, mechanical processes and thermal processes.
A widely used gas is Nitrogen 5.0, which is 99.999% pure(the 5 indicates the number of nines in the purity percentage).

Some contamination induces problems are:
- mobile ions in oxides: ions are extremely mobile and they can travel fast through electrical components, causing change in electric fields and voltages, leading to malfunction or destruction of components.
- unintentional films between layers: the presence of unintentional films between thin layers can create unwanted mechanical stress, leading to cracks and delamination, or even cause short circuits or impede adhesion between moving parts.
- particles: the most probable failure is contamination due to particles, which are undesired objects of size 0.06 µm to 100 µm. They are not chemically active like ions and are smaller than films. They adhere to surfaces thanks to Van der Waals forces, electrostatic forces and capillary forces. They can cause shadowing during lithography, producing defects in patterns, they can also cause short circuits and open circuits, or create mechanical interference in moving parts(jamming).
In lithography processes, you can resolve the issue of particles by using a pellicle, which is a thin transparent film placed above the photomask. The particles will adhere to the pellicle instead of the photomask, and since the pellicle is out of focus during exposure, the particles won't affect the pattern.

To reduce contamination, cleanrooms are used. Cleanrooms are controlled environments where particulate contamination, temperature, humidity and pressure are regulated to minimize the presence of contaminants, so that experiments and manufacturing processes can be repeated with high precision and reliability.
Cleanrooms are classified according to the number and size of particles per volume of air. A cleanroom belong to a certain class if the number of particles of a certain size is below a certain limit. For example to be in the class 100, the number of particles of size 0.5 µm or larger must be less than 100 particles per cubic foot of air.
![[Pasted image 20251202151750.png]]
Particulate concentration can be measured using filtering and counting methods, or exploiting optical scattering of laser beams. The latter works by shining a laser beam through a sample of air, and measuring the scattered light using photodetectors. The intensity and pattern of the scattered light can provide information about the size and concentration of particles in the air sample.

##### Cleanroom Design
![[Pasted image 20251202152054.png]]
A flow of clean filtered air is introduced into the cleanroom, while the contaminated air is extracted. There are 2 main types of designs:
- Raised Floor: the clean air is introduced from the ceiling vertically downwards, and the contaminated air is extracted from the floor. The floor is raised to create a plenum for air circulation. The air then goes from the raised floor to lateral return air plenums, where is filtered. Then as the last step the air is reintroduced from the ceiling, through HEPA filters, also called absolute filters. These filters can remove at least 99.97% of airborne particles of size 0.3 µm or larger. They work using a combination of diffusion, interception and inertial impaction to capture particles.
- Low-wall return: the clean air is introduced from the ceiling vertically downwards, and the contaminated air is extracted from low wall vents. The air is filtered and reintroduced in a similar manner as the raised floor design. The main difference is that the air is extracted from low wall vents instead of the floor, which results in a non vertical airflow pattern, meaning that the middle of the room will have a less efficient air circulation so it will be more prone to contamination.

##### Cleanroom Classification
To the previous classification, we add how much air changes per hour(ACH) are needed to maintain the cleanliness level. 
We also added a standard for the variation of temperature and humidity allowed. The standard temperature is 20°C ± 2°C, while the standard humidity is 50% ± 5% RH.
We also held a positive pressure inside the cleanroom compared to the outside, so particles in the room tend to go outside and particles from outside don't enter the cleanroom.(In contrast in chemical labs negative pressure is held to avoid leaks of dangerous chemicals outside the lab like viruses or toxic gases)
![[Pasted image 20251202153642.png]]

The federal 2009 standard is no more used, instead ISO is used to get rid of national differences(for example in unit measurements). 
![[Pasted image 20251202153808.png]]

Read the following classes:
![[Pasted image 20251202153834.png]]

##### Cleanroom Air Filters
**High Efficiency Particulate Air (HEPA) Filters**: These filters are designed to capture at least 99.97% of airborne particles that are 0.3 micrometers in diameter. They are commonly used in cleanrooms to maintain air purity. They are mechanical filters made of a net of gla
## References
