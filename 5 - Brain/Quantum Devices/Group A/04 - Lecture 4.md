
2025-10-14 15:25

Status: 

Tags:

# Lecture 4
##### Charge Transport in Semiconductors
Current is created due to the physical displacement of charge carriers(electrons and holes) in a material.
$$
\phi = \frac{\text{\# of particles}}{\text{time area}} $$
$\phi$ is the flux of particles, which is the number of particles crossing a unit area per unit time, it's dimension is $L^{-2} T^{-1}$.
If each particle has a charge $Q$, the current density $\vec{J}$ is given by:
$$ \vec{J} = \frac{\text{current}}{\text{area}} = \frac{\text{charge}}{\text{time area}} = \frac{Q \cdot \text{\# of particles}}{\text{time particles}}{\text{time area}} = Q \phi $$
Neglecting quantum phenomena(like tunneling), particles flow because of two main effects:
1. An electric field $\epsilon$ that exerts a force on the charged particles, causing them to drift.
	Following the effective mass theory, at $T > 0K$, the average velocity of the carriers is zero $\langle v \rangle = 0$. The single particle is not motionless, it has a random thermal velocity $\vec{v}_{th}$, but the average velocity of all the particles is zero. If we take a cross-section we can observe the same number of particles moving in and out. When we apply an electric field, it exerts a force on the charged particles, causing them to accelerate in the direction of the field(for holes) or opposite to it(for electrons). . However, due to scattering events with impurities, phonons, and other carriers, the particles do not accelerate indefinitely(link to Sommerfeld model).  
	The average velocity is no longer zero, so we can define a drift velocity:
$$ \begin{cases}
\vec{v}_{n, drift} = - \mu_n \vec{\epsilon} \\
\vec{v}_{p, drift} = + \mu_p \vec{\epsilon}
				\end{cases} $$
	Where $\mu_n$ and $\mu_p$ are the electron and hole mobilities, which are positive quantities that characterize how easily the carriers can move through the material under the influence of an electric field. The negative sign for electrons indicates that they move opposite to the direction of the electric field, while holes move in the same direction as the field.
	$\mu_n$ and $\mu_p$ are constant only for small electric fields, for high fields they depend on the field itself:
$$ \log_{10} |\vec{v}_{drift}| = \log_{10} |\mu \vec{\epsilon}| = \log_{10} \mu + \log_{10} |\vec{\epsilon}| $$
	So we can see that for high fields the mobility decreases with the field, and the drift velocity saturates at a certain value called saturation velocity $v_{sat}$.
	![[Pasted image 20251016183152.png]]
	They are considered constants, we say that low field mobility is constant, when we are in the low field regime of the $v_{drift}(\vec{\epsilon})$ curve. Different values of mobility give different slopes of the curve. The average velocity grows linearly with the field until it reaches the saturation velocity, which is a characteristic of the material, for semiconductors it is around $10^7 cm/s$. It doesn't always follow a smooth curve, for example in compound semiconductors like GaAs, the curve has a peak and then decreases before reaching saturation. This is due to the complex band structure of the material. 
	The drift corresponds to a drift flow of particles:
$$
\phi = \frac{\text{\# of particles}}{\text{time area}} \cdot \frac{\text{space}}{\text{space}} = \frac{\text{\# of particles}}{\text{volume}} \cdot \frac{\text{space}}{\text{time}}$$
	$area \cdot space$ on the denominator is the volume in which we find the particle moving. The first term is the density of particles $n$ or $p$, and the second term is the space in which they move over time, which is the drift velocity. So we can write:
	$$ \phi_{n, drift} = n \vec{v}_{n, drift} = - n \mu_n \vec{\epsilon} \quad \quad \quad  \phi_{p, drift} = p \vec{v}_{p, drift} = + p \mu_p \vec{\epsilon} $$
	And the current density due to drift is given by:
	$$ \vec{J}_{n, drift} = - q \phi_{n, drift} = q n \mu_n \vec{\epsilon} \quad \quad \quad  \vec{J}_{p, drift} = + q \phi_{p, drift} = q p \mu_p \vec{\epsilon} $$
2. An effect due to the random movement of free particles(diffusion of the carriers) that causes them to move from regions of high concentration to regions of low concentration, creating a diffusion current. 
	







## References
