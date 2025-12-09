
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
$$R_s = \frac{\rho}{t} = \frac{1}{\int_x
## References
