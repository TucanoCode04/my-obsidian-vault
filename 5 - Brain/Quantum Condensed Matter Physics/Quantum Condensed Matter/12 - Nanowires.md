
2026-01-14 13:57

Status: 

Tags:

# Nanowires
Let's start with a review on the band structure of nanowires.
The total energy of a nanowire can be expressed as:$$E = \frac{\hbar^2 k_z^2}{2m^*} + \frac{\hbar^2 n_x^2 }{8mL_x^2} + \frac{\hbar^2 n_y^2 }{8mL_y^2}$$ Where the first term corresponds to the kinetic energy along the wire axis (z-axis), and the second and third terms correspond to the quantized energy levels due to confinement in the transverse directions (x and y axes). Here, $n_x$ and $n_y$ are quantum numbers associated with the transverse modes, and $L_x$ and $L_y$ are the dimensions of the nanowire cross-section.
To have a more compact way to write we assume $L_x = L_y$ and $n_x = n_y = n$, then we can rewrite the energy as:$$E = \frac{\hbar^2 k_z^2}{2m^*} + \frac{\hbar^2 n^2 }{8mL^2}$$The density of states (DOS) for a nanowire is given by:$$D(E) = \sum_n \left(\frac{2m^*}{\hbar^2}\right)^{1/2} \frac{1}{\pi \sqrt{E - E_n}}$$Where $E_n = \frac{\hbar^2 n^2 }{8mL^2}$ represents the quantized energy levels due to confinement in the transverse directions and it also determines the vertices of the parabolic subbands in the nanowire band structure.
![[Pasted image 20260114142444.png]]
By focusing of a single subband (fixed n), the DOS becomes:$$D(E) = \begin{cases} \left(\frac{2m^*}{\hbar^2}\right)^{1/2} \frac{1}{\pi \sqrt{E - E_n}} & \text{for } E > E_n \\ 0 & \text{for } E \leq E_n \end{cases}$$This expression shows that the DOS diverges as the energy approaches the subband edge $E_n$ from above, indicating a high density of available states near the subband minima. 
#### Current Calculation
![[Pasted image 20260114142858.png]]
We will use a model that consists on a 1D channel that connects two contacts (source and drain) as shown in the figure above. The two contacts have different Fermi levels, such that $E_{FL} > E_{FR}$, which creates a bias voltage across the channel. We further assume that:
- The channel is ballistic, meaning that electrons can travel through it without scattering.
- Electrons entering the contacts from the channel instantly thermalize to the local Fermi level reaching equilibrium.
- The contacts are reflectionless, meaning that electrons entering the contacts do not reflect back into the channel.
So the transport in the wire happens because electrons with negative momentum (moving from right to left) are injected from the right contact with Fermi level $E_{FR}$, and electrons with positive momentum (moving from left to right) are injected from the left contact with Fermi level $E_{FL}$. The net current is then given by the difference between the currents contributed by electrons from each contact(maybe it's the contrary, check).

The dispersion relation is the sum of the kinetic energy along the wire and the quantized energy levels due to confinement:$$E_{n,k_x} = \frac{\hbar^2 k_x^2}{2m^*} + E_n$$Where $E_n = \frac{\hbar^2 n^2 }{8mL^2}$ represents the quantized energy levels due to confinement in the transverse directions and is called cut-off energy.
We will consider the c






## References
