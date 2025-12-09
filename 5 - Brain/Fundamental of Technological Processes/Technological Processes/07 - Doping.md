
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


## References
