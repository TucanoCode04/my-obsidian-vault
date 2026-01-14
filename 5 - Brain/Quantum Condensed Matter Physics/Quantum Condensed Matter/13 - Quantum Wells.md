
2026-01-14 16:11

Status: 

Tags:

# Quantum Wells
##### Bulk Bandgap Engineering
The need for efficient light-emitting materials has driven the research towards direct bandgap semiconductors. The emission wavelength of a semiconductor corresponds to its bandgap energy. By engineering the bandgap through various techniques, we can create materials that emit light at desired wavelengths.
One of these techniques is by mixing different semiconductor materials to form alloys. There are some semiconductor with similar lattice constants, so they can be mixed without causing significant strain in the crystal structure, that have very different bandgap energies. For example, Gallium Arsenide (GaAs) has a bandgap of about 1.42 eV, while Aluminum Arsenide (AlAs) has a bandgap of about 2.16 eV. By creating an alloy of these two materials, such as Aluminum Gallium Arsenide (AlGaAs), we can achieve a bandgap that is intermediate between the two, allowing for tunable emission wavelengths.
![[Pasted image 20260114170027.png]]
So one can grow a layer of $Al_xGa_{1-x}As$ on top of a layer of GaAs, where the value of x determines the bandgap of the AlGaAs layer>
$$E_g(x) = (1.42+ 1.087x + 0.438x^2) eV$$The bandgap becomes indirect for x > 43%, so it's bad for light emission. After that, we invented quantum wells to further improve the efficiency of light emission.
#### Single Quantum Well vs Multiple Quantum Wells
A quantum well is a thin layer of a lower bandgap semiconductor material sandwiched between two layers of a higher bandgap semiconductor material. This structure creates a potential well that confines charge carriers (electrons and holes) in the lower bandgap material, enhancing their recombination efficiency and thus improving light emission.
![[Pasted image 20260114170603.png]]
We can't choose any type of semiconductor materials to form quantum wells. The materials must form type I hetero-structures with proper band alignment and lattice matching to minimize defects. 
![[Pasted image 20260114170650.png]]

They basically create a potential well for both electrons and holes, confining them in the same region and enhancing recombination efficiency.
![[Pasted image 20260114170832.png]]

##### Size of Quantum Wells
![[Pasted image 20260114170918.png]]
![[Pasted image 20260114170936.png]]

##### Multiple Quantum Wells and Superlattices
![[Pasted image 20260114171030.png]]
To have a multi quantum well structure, we just need to repeat the single quantum well structure multiple times and have $b << d$ so that the wells are independent of each other.
![[Pasted image 20260114171126.png]]
![[Pasted image 20260114171135.png]]
![[Pasted image 20260114171143.png]]

##### Eigenvalues and Eigenfunctions in Quantum Wells
![[Pasted image 20260114171844.png]]
The energy bands will be paraboiloids in k-space, coming from the fact that we have free particles in the x-y plane and confined particles in the z direction.
$$\psi_e (x,y,z) = \phi_e(x,y) \theta_e(z)$$Where $\phi_e(x,y)$ are bloch functions in the x-y plane and $\theta_e(z)$ are the confined wavefunctions in the z direction.
$$\theta_n(z) = \begin{cases} \sqrt{\frac{2}{L_z}} sin(\frac{n \pi z}{L_z}) & n \text{ even}\\ \sqrt{\frac{2}{L_z}} cos(\frac{n \pi z}{L_z}) & n \text{ odd} \end{cases}$$
With energy eigenvalues:
$$E_n(k_z) = \frac{\hbar^2 n^2}{8 m^* L_z^2} $$
While in the x-y plane, we have free particle like behavior:
$$\phi (x,y) = \frac{1}{\sqrt{A}} e^{i(k_x x + k_y y)} \mu(x,y)$$With energy eigenvalues:
$$E(k_x, k_y) = \frac{\hbar^2 (k_x^2 + k_y^2)}{2 m^*} $$
So the total energy eigenvalues are:
$$E_{e,(n,k)} = E_n + E(k_x, k_y) =  \frac{\hbar^2 n^2}{8 m^* L_z^2} + \frac{\hbar^2 (k_x^2 + k_y^2)}{2 m^*} $$
In our case $L_z = d$, the width of the quantum well. 
The confinement energy is inversely proportional to the square of the well width, so thinner wells lead to higher confinement energies. To note also that the confinement energy is also inversely proportional to the effective mass of the particle, so lighter particles experience higher confinement energies. So even light and heavy holes will have different confinement energies in the same quantum well.
![[Pasted image 20260114173006.png]]
This all calculation was for the electrons, but we can do the same for holes. The total energy for the holes will be:
$$E_{h,(n,k)} = E_n + E(k_x, k_y) =  \frac{\hbar^2 n^2}{8 m^*_{h} d^2} + \frac{\hbar^2 (k_x^2 + k_y^2)}{2 m^*_{h}} $$
Where $m^*_{hh}$ is the effective mass of the heavy holes.

The DOS for a given paraboloid band structure is given by:
$$D(E) = \frac{m^*}{\pi \hbar^2 L_z}$$
Where $m^*$ is the effective mass of the particle (depending on whether it's electron or hole).
##### Consequences of Quantum Confinement
![[Pasted image 20260114173322.png]]

##### Optical Absorption in Quantum Wells
![[Pasted image 20260114173454.png]]
In a quantum well the absorption edge is shifted to higher energies due to the confinement energies of electrons and holes. 
$$\Delta E = \hbar \omega = E_g + \frac{\hbar^2 n^2}{8 m^*_{e} d^2} + \frac{\hbar^2 k^2}{2 m^*_{e}} + \frac{\hbar^2 n'^2}{8 m^*_{h} d^2} + \frac{\hbar^2 k'^2}{2 m^*_{h}} $$
Where n and n' are the quantum numbers for electrons and holes respectively. All this for $n=n'=1$ for the first absorption peak, and $k=k'=0$ for normal incidence.
So it basically adds up to the bandgap, for example if we had Ga with $E_g = 1.42 eV$, we create some quantum dimensions and we can shift the absorption edge to higher energies, in particular by changing the well width d.

##### Fermi Golden Rule
We now want to have some light of frequency higher than the band gap to be absorbed, we want to see how the absorption changes in function of the incident light frequency.
The optical absorption coefficient is determined by the transition rate $W_{i\rightarrow f}$ from an initial state $\psi_i$ to a final state $\psi_f$ induced by absorption of a photon of angular frequency $\omega$. According to Fermi's Golden Rule:$$W_{i\rightarrow f} = \frac{2 \pi}{\hbar} |<\psi_f | \hat{H'} | \psi_i>|^2 g(\Delta E)$$Where $H'$ is the perturbation Hamiltonian due to the interaction with the electromagnetic field, and $g(\Delta E)$ is the joint density of final states at the energy difference $\Delta E = E_f - E_i = \hbar \omega$.)
We specify that the light wavevector has only a component in the z direction, so $k = (0,0,k_z)$ $$\hat{H'} = -e \vec{r}\cdot \vec{E_0}e^{i k_z z}$$Where $\vec{E_0}$ is the electric field amplitude of the incident light, so it has only x and y components.
The matrix element can be separated:$$M_{fi} = <\psi_f | \hat{H'} | \psi_i> = <\phi_f |-e\vec{r}\cdot \vec{E_0}e^{i k_z z} | \phi_i> = - <\phi_f |e x E_{0x} e^{i k_z z} |\phi_i> - <\phi_f |e y E_{0y} e^{i k_z z} | \phi_i> $$If isotropic then x and y will be the same, so we focus on the term x:$$-<\phi_f |e x E_{0x} e^{i k_z z} |\phi_i> = - \int \theta_{en}^*(z) \phi_{ek_x k_y}^*(x,y) e x E_{0x} e^{i k_z z} \phi_{hk_x' k_y'}(x,y) \theta_{hn'}(z) dxdydz $$The final state is assumed to be an electron state, while the initial state is a hole state, because we are considering absorption from the valence band to the conduction band. We separate the wavefunctions into their z-dependent and x-y dependent parts.$$= -\int \theta_{en}^*(z) e^{i k_z z} \theta_{hn'}(z) dz \int \phi_{ek_x k_y}^*(x,y) e x E_{0x} \phi_{hk_x' k_y'}(x,y) dxd y $$The first integral is the overlap integral in the z direction, while the second integral is the in-plane transition matrix element. $z$ varies between $0$ and $d$, in fact $\theta(z)$ are only defined in the well region.$$k_z=\frac{2 \pi}{\lambda} \approx 10^7 m^{-1} \quad \quad z= 10^{-9} m $$So $k_z z << 1$, we can approximate $e^{i k_z z} \approx 1$. So the integral becomes:$$= -\int \theta_{en}^*(z) \theta_{hn'}(z) dz \int e^{-i(k_x x + k_y y)} \mu_C^*(x,y) e x E_{0x} \cdot e^{i(k_x' x + k_y' y)} \mu_V(x,y) dxd y $$The first integral is the overlap integral in the z direction, which is:$$\delta_{n n'} = \begin{cases} 1 & n=n' \\ 0 & n \neq n' \end{cases} $$This means that transitions are only allowed between states with the same quantum number n. This is known as the selection rule for quantum wells. Better explained, we can't mix sub-bands with different quantum numbers, for example the first electron sub-band can only couple with the first hole sub-band, and so on.$$=- \delta_{n n'} \int e^{-i(k_x x + k_y y)} \mu_C^*(x,y) e x E_{0x} \cdot e^{i(k_x' x + k_y' y)} \mu_V(x,y) dxd y $$The second integral is the in-plane transition matrix element, which involves the Bloch functions of the conduction and valence bands. This integral determines the strength of the optical transition between the initial and final states in the x-y plane. We introduce another simplification here, we assume that the momentum of the photon is negligible compared to the momentum of the electrons and holes, so $k_x \approx k_x'$ and $k_y \approx k_y'$. This is known as the dipole approximation.$$M_{fi}=- \delta_{n n'} E_{0x} \int \mu_C^*(x,y) e x \mu_V(x,y) dxd y $$The remaining integral is the interband dipole matrix element, which quantifies the coupling between the conduction and valence band states due to the electric field of the light. This matrix element is crucial for determining the optical absorption properties of the quantum well.
![[Pasted image 20260114184853.png]]
(Remember to look at the slides, because there are things that are not here!!!!!!!!)


As we go to higher frequencies, we can couple states with higher quantum numbers n, since they are parallel to each other, we will have absorption peaks at energies corresponding to transitions between these sub-bands. This can be seen by analyzing the joint density of states for the quantum well structure.$$\Delta E = Eg + E_{e,1} + E_{h,1} + \frac{\hbar^2 k_{xy}^2}{2 \mu} $$Where $\mu$ is the reduced mass of the electron-hole pair in the x-y plane.
Considering a subband in valence band with quantum number n' and a subband in conduction band with quantum number n, the joint density of states for transitions between these subbands is given by:$$g_{n n'}(\Delta E) = \frac{\mu}{\pi \hbar^2 }$$Resulting in a step-like increase in the absorption coefficient with the height of each step corresponding to the joint density of states for that particular transition $\frac{\mu}{\pi \hbar^2 }$ and the distance between the steps determined by the confinement energies of the respective subbands $E_g + E_{e,n} + E_{h,n'}$.
The steps are given because we still have, for example at $n = n' = 2$, the excitations given by $n=n'=1$ are still possible, so we have a step increase in absorption at that energy.
![[Pasted image 20260114194031.png]]

We can see heavy holes and light holes contributions separately, because they have different effective masses, so they will give different step heights in the absorption spectrum.
The $\downarrow$ indicates points where the selection rule is broken, due to imperfections in the quantum well structure, allowing transitions between subbands with different quantum numbers n and n'. For example, after $n=n'=2$, is broken, we assumed an infinite potential well, but in reality the potential is finite, so there is some tunneling of the wavefunctions into the barrier region, which can lead to mixing of states with different quantum numbers. 
After a while the steps will smooth out, becoming similar to $\sqrt{E}$ dependence of bulk materials, because at higher energies the confinement effects become less pronounced, and the density of states approaches that of a three-dimensional system.
![[Pasted image 20260114194326.png]]

##### Optical Emission
We also have emission, after thermalization of the carriers in the subbands, we have recombination and emission of photons. The emission spectrum will also show peaks corresponding to transitions between subbands with the same quantum number n, following the same selection rule as absorption.
The emission coefficient depends again on $L_z$, the well width, because it determines the confinement energies and thus the energies of the emitted photons.
![[Pasted image 20260114194539.png]]
![[Pasted image 20260114194549.png]]

##### Laser Diodes
![[Pasted image 20260114194627.png]]
You inject current into the quantum well region, creating a population inversion between the electron and hole subbands. When the population inversion is achieved, stimulated emission occurs, leading to coherent light output from the laser diode.
In this device, other than electrical confinement, we have optical confinement as well, because the refractive index of the quantum well region is higher than that of the surrounding barrier layers, creating a waveguide structure that confines the light within the active region.

#### 2D Electron Gas
To create it we need a type I heterostructure, for example AlAs heavily doped n-type and GaAs undoped. The electrons from the AlAs will diffuse into the GaAs, creating a depletion region in the AlAs and an accumulation region in the GaAs, till the two Fermi levels align.
In the GaAs region, we will have a triangular potential well at the interface, confining the electrons in the z direction, while they are free to move in the x-y plane, creating a two-dimensional electron gas (2DEG).
The 2D electron gas is characterized by high mobility, higher than metals, $\approx 10^6 cm^2/Vs$, because the electrons are confined in a region with low impurity scattering, since the dopants are far away in the AlAs layer.
To each energy level in the triangular well corresponds a paraboloid in k-space, so we have subbands in the z direction and free particle behavior in the x-y plane.

(there are other things in the slides)









## References
