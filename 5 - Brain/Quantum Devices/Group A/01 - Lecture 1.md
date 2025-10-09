
2025-10-09 10:38

Status: 

Tags:

# Lecture 1
##### Introduction to Electrical Conduction in Crystals
A crystal is a spatially periodic arrangement of identical atoms or molecules. An elemental material is made of a single type of atom normally from group IV of the periodic table, like Silicon (Si) or Germanium (Ge). A compound material is made of two or more types of atoms, normally from groups III and V, like Gallium Arsenide (GaAs) or Indium Phosphide (InP).
A particle with electric charge $Q$ in an electric field $\vec{E}$, the electric field could even be inside a material by applying a voltage for example, experiences a force $\vec{F}$ given by:
$$\vec{F} = Q \vec{E}$$
This force causes particles(electrons or holes) to accelerate, creating an electric current $\vec{J}$, this is the microscopic origin of electrical conduction.
The electric field tilts the potential energy landscape of the crystal, wells created by the nuclei, creating a potential gradient that causes charged particles to move towards lower potential energy(higher if the charge is negative like electrons). The electric field does work on the charged particles, increasing their kinetic energy and causing them to move through the crystal lattice.
##### Microscopic Ohm's Law
Depending on the material conductivity, the density of current $\vec{J}$ is proportional to the applied electric field $\vec{E}$:
$$\vec{J} = \frac{I}{A} = \sigma \vec{E}$$ Where $\sigma$ is the conductivity of the material, $I$ is the current and $A$ is the cross-sectional area(the area of the surface of the material that the current passes through when you cut the material perpendicularly to the direction of the current) of the material. So if $A$ is larger, the charges are more spread out, and the current density is lower. $I= \frac{dQ}{dt}$, where $Q$ is the total charge that passes through the cross-sectional area $A$ in time $t$. 
The stronger the electric field, the larger the current density. The conductivity $\sigma$ is a measure of how easily charges can move through a material when subjected to an electric field. It depends on the number of charge carriers (electrons or holes) available for conduction and their mobility within the material. 
$\sigma$ has units of $\frac{S}{cm} = \frac{1}{\Omega cm}$, where $S$ is Siemens and $\Omega$ is Ohm.
An ideal conductor presents: $\sigma \to \infty$.
An ideal insulator presents: $\sigma = 0$.
##### Potential Energies 
- Isolated Atom: The potential energy of an electron in an isolated atom is quantized, meaning it can only take on specific discrete and stable energy levels. From Pauli exclusion principle, no two electrons can occupy the same quantum state simultaneously, which leads to the formation of distinct energy levels. These energy levels are determined by the electrostatic attraction between the negatively charged electrons and the positively charged nucleus, following the Coulomb potential. The potential energy is negative, indicating that the electron is bound to the nucleus with a $\approx \frac{1}{|x|}$ dependence. These are called localized states because the electron is confined to a specific region around the nucleus.
- 2 Atoms Far from Each Other: If they are far enough, they do not interact and the potential energy is just the sum of the individual atoms.
- 2 Atoms Close to Each Other: When two atoms are brought close together, their outer electron orbitals start to overlap. Due to the Pauli exclusion principle, no two electrons can occupy the same quantum state. As a result, the discrete energy levels of individual atoms broaden into a continuous range of energy levels known as energy bands when you have a large concentration of atoms like in a solid. These are called delocalized states because the electron is no longer confined to a specific atom but can move throughout the crystal lattice.
##### Energy Bands in Crystals
For a crystal made of $N >> N_A$ atoms, where $N_A$ is the number of Avogadro, each isolated energy level of an atom will split into $N$ closely spaced energy levels due to the interactions between atoms. For a crystal of elements of group IV, like Silicon or Germanium, which have 4 valence electrons, the outermost energy levels will merge to form two main energy bands: the valence band and the conduction band, each of magnitude $4N$. 
We also define a crystal forbidden band, or band gap, $E_g$, which is which is the the energy range between the valence band and the conduction band where no electron states can exist.
Since each atom provides 4 electrons from its outer shell to be put in the bands, we must find a place for $4N$ electrons. At $T=0K$ all electrons will occupy the lowest available energy states, filling up the valence band completely with $4N$ electrons, while the conduction band remains empty. This is the ground state of the crystal, where $\sigma = 0$. 
If we apply a strong enough electric field, we can provide enough energy to some electrons to jump from the valence band to the conduction band, creating free electrons in the conduction band and holes the valence band. This creates a non-equilibrium state where $\sigma \neq 0$. The force on the electrons due to the electric field will be $\vec{F} = -q \vec{E}$, where $-q$ is the charge of the electron and $q= 1.6 \times 10^{-19} C$.
Conduction is the valence band is interpreted as the movement of holes in the field direction $\vec{F} = +q \vec{E}$, where $+q$ is the charge of the hole.
## References
