
2026-01-14 13:57

Status: 

Tags:

# Nanowires
Let's start with a review on the band structure of nanowires.
The total energy of a nanowire can be expressed as:$$E = \frac{\hbar^2 k_z^2}{2m^*} + \frac{\hbar^2 n_x^2 }{8mL_x^2} + \frac{\hbar^2 n_y^2 }{8mL_y^2}$$ Where the first term corresponds to the kinetic energy along the wire axis (z-axis), and the second and third terms correspond to the quantized energy levels due to confinement in the transverse directions (x and y axes). Here, $n_x$ and $n_y$ are quantum numbers associated with the transverse modes, and $L_x$ and $L_y$ are the dimensions of the nanowire cross-section.
To have a more compact way to write we assume $L_x = L_y$ and $n_x = n_y = n$, then we can rewrite the energy as:$$E = \frac{\hbar^2 k_z^2}{2m^*} + \frac{\hbar^2 n^2 }{8mL^2}$$The density of states (DOS) for a nanowire is given by:$$D(E) = \sum_n \left(\frac{2m^*}{\hbar^2}\right)^{1/2} \frac{1}{\pi \sqrt{E - E_n}}$$Where $E_n = \frac{\hbar^2 n^2 }{8mL^2}$ represents the quantized energy levels due to confinement in the transverse directions and it also determines the vertices of the parabolic subbands in the nanowire band structure.
![[Pasted image 20260114142444.png]]
By focusing of a single subband (fixed n), the DOS becomes:$$D(E) = \begin{cases} \left(\frac{2m^*}{\hbar^2}\right)^{1/2} \frac{1}{\pi \sqrt{E - E_n}} & \text{for } E > E_n \\ 0 & \text{for } E \leq E_n \end{cases}$$This expression shows that the DOS diverges as the energy approaches the subband edge $E_n$ from above, indicating a high density of available states near the subband minima. 

## References
