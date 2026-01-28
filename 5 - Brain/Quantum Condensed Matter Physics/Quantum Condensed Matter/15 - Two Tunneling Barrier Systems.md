
2026-01-28 19:52

Status: 

Tags:

# Two Tunneling Barrier Systems
![[Pasted image 20260128195607.png]]
The first figure represents a two tunneling barrier system. As we said before to calculate the transition probability we will use the transfer matrix method. The transfer matrix for the whole system is given by the product of the transfer matrices for each region.
In the second graph we see the transmittance in function of the energy for different values of the transmission coefficient of the barriers. The interesting case is when the transmission coefficient of the barriers is low, in this case we can see that there are some peaks in the transmittance(where transmission = 1) corresponding to specific energies, these energies are the resonant energies of the system. At these energies the wavefunction inside the well between the barriers constructively interferes, leading to a high probability of transmission through the system.
It's not known beforehand that with 2 barriers you will have 2 resonant energies, but in general with N barriers you will have N-1 resonant energies. It depends on the width of the well between the barriers, the width of the barriers and the height of the barriers.
The resonant energies are called resonance states or quasi-bound states, resonance because inside the well the two waves interfere constructively creating high amplitude waves, and quasi-bound because if we take the modulus squared of the wavefunction inside the well we will see that it is similar to a bound state having high probability of finding the particle there, but since there is a non-zero probability of tunneling through the barriers the particle is not truly bound, since the barriers are finite.
![[Pasted image 20260128201036.png]]
For example here, even with probability between $E_1$ and $E_2$ or greater than $E_2$ there's still much much lower probability of transmission compared to the resonant energies $E_1$ and $E_2$(where we have transmission = 1).
In general in this resonance energies is like the particle doesn't see the barriers.

![[Pasted image 20260128201603.png]]
In this slide we can see the same graph as before, but in logarithmic scale, to better see the difference with the single barrier transmission(dashed-line), otherwise too small to see. As we can see the single barrier has probability going on higher energies of $10^{-3}$ while the double barrier has probability of 1 for specific energies.

![[Pasted image 20260128211228.png]]
We see a device, where the double barrier is composed by:
- GaAs, which has lower band gap
- AlAs, which has higher band gap
- GaAs, again lower band gap
- AlAs, higher band gap
- GaAs, lower band gap
The AlAs layers act as barriers for the electrons in the GaAs layers, creating a double barrier structure. When a voltage is applied across the device, electrons can tunnel through the barriers at specific resonant energies, leading to peaks in the current-voltage characteristics of the device. This phenomenon is known as resonant tunneling and is utilized in various electronic applications, such as high-speed transistors and quantum cascade lasers.
Before and after the double barrier structure there are doped regions, which provide free electrons to the system, allowing for tunneling to occur when a voltage is applied.
##### Resonant-Tunneling Diode (RTD)
![[Pasted image 20260128212218.png]]
A Resonant-Tunneling Diode (RTD) is a type of semiconductor device that utilizes the principle of resonant tunneling through a double barrier structure to achieve high-speed electronic performance. The RTD consists of two thin layers of a high bandgap material (barriers) separated by a thin layer of a low bandgap material (well). When a voltage is applied across the RTD, electrons can tunnel through the barriers at specific resonant energies, leading to peaks in the current-voltage characteristics of the device.

![[Pasted image 20260128212627.png]]
We are now going to analyze the energy band diagram of the RTD under different bias conditions. In the image we see the zero-bias condition (first figure), where the Fermi levels on both sides of the device are aligned, and there is no net current flow. The conduction band profile shows the double barrier structure with the well in between.

![[Pasted image 20260128213009.png]]
When a small forward bias is applied (second figure), the Fermi level on the left side of the device is raised relative to the right side. By increasing the bias, the current in the I-V current increases as expected also classically. However, as the bias continues to increase, the resonant energy level in the well align with the Fermi level on the left side, leading to a peak in the current due to resonant tunneling. But after this peak, as the bias increases further, we see a sharp decrease in current(even no current if we are in a small energy scale where only tunneling current is possible), known as negative differential conductance ($\frac{dI}{dV}$). This occurs because the resonant energy level moves out of alignment with the Fermi level on the left side, reducing the tunneling probability.
Important, this is not like quantum dot, the energy state in the well is not a bound state, so there will be no current flow when the energy level is out of alignment. Unlike quantum dots where the bound states can still allow for some current flow even when not aligned, since it only depends on the bias window.
Obviously, to draw a better graph we would need to calculate the density of states in the well, the tunneling probabilities, and the Fermi-Dirac distributions on both sides of the device, but this is just a qualitative explanation of the I-V characteristics of an RTD.

## References
