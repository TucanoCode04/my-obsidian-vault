
2025-10-09 10:39

Status: 

Tags:

# Lecture 2
##### Some Fundamental Concepts
In a single atom the electrons occupy a discrete set of energy levels. When When atoms are brought together to form a solid, their outer electron orbitals start to overlap. Due to Due to the Pauli exclusion principle, no two electrons can occupy the same quantum state. As a result, the discrete energy levels of individual atoms broaden into a continuous range of energy levels known as energy bands when you have a large concentration of atoms like in a solid. 

There are two main types of energy bands in a solid:
1. **Valence Band**: This is the highest range of electron electron energies where electrons are normally present at absolute zero temperature. The valence band is typically filled with electrons. These electrons are bound to atoms but can still move within bonds between atoms.
2. **Conduction Band**: This is the range of electron energies higher than the valence band. The conduction band is typically empty at absolute zero temperature. Electrons in the conduction band are free to move throughout the material, allowing them to conduct electric current.

Between the valence band and the conduction band, there is a region called the **band gap** where no electron states can exist. The size of the band gap determines the electrical properties of the material:
- **Conductors**: In conductors (like metals), the valence band overlaps with the conduction band, allowing electrons to move freely and conduct electricity.
- **Semiconductors**: In semiconductors (like silicon), there is a small band gap. At absolute zero, the valence band is full and the conduction band is empty. However, at higher temperatures or when doped with impurities, electrons can gain enough energy to jump across the band gap into the conduction band, enabling electrical conductivity.
- **Insulators**: In insulators (like diamond), the band gap is large, making it difficult for electrons to jump from the valence band to the conduction band. As a result, insulators do not conduct electricity under normal conditions.

When an electron gains enough energy (for example, from thermal excitation or photon absorption), it can jump from the valence band to the conduction band, leaving behind a "hole" in the valence band. This hole can be thought of as a positive charge carrier because it represents the absence of an electron.
##### Intrinsic Carrier Concentration in Semiconductors
By construction, the population of electrons in the conduction band $n$ is equal to the population of holes in the valence band $p$. So the number of electrons promoted equals the number of holes left behind.
$$n = p$$
In pure(intrinsic) crystals, we have that:
$$n = p = n_i$$ where $n_i$ is the intrinsic carrier concentration, which depends on the material(band gap) and temperature. The larger the band gap $E_g$, the harder it is for electrons to jump from the valence band to the conduction band, resulting in a lower intrinsic carrier concentration.
$$
\text{Sn(tin)(Conductor)} \quad n_i \approx 10^{22} cm^{-3} \quad E_g \approx 0.1 eV 
$$
$$
\text{Si(Silicon)(Semiconductor)} \quad n_i \approx 1.45 \times 10^{10} cm^{-3} \quad E_g \approx 1.12 eV 
$$
$$
\text{Diamond(Insulator)} \quad n_i \approx 10 cm^{-3} \quad E_g \approx 5.47 eV 
$$
The $E_g$ values for semiconductors range normally from $1 eV$ to $4 eV$, while for insulators it is typically greater than $5 eV$.
The typical atomic density in solids is around $10^{22} cm^{-3}$, so in conductors almost all atoms contribute to electrical conduction, while in semiconductors only a small fraction of atoms contribute, and in insulators almost none do. The atomic density is given by:
$$d = \frac{\text{\# atoms}}{cm^3}$$
##### Silicon
If we analyze, specifically, Silicon is an element of the IV group in the periodic table, which means it has 4 valence electrons. Each atom can create up to 4 covalent bonds with neighboring atoms. In a pure Silicon crystal, each atom shares its 4 valence electrons with 4 neighboring atoms, forming a stable tetrahedral structure. All atoms that create a bond contribute to the valence band. When a hole is created in the valence band, that represents a broken bond, and the hole can move through the lattice as neighboring electrons fill the hole, effectively allowing the hole to move in the opposite direction.
The higher the temperature, the more thermal energy is available to excite electrons across the band gap, increasing the number of holes and increasing the intrinsic carrier concentration.
##### Semiconductor Doping
Introduction/substitution of impurities into a pure semiconductor can significantly alter its electrical properties. The perturbation needs to be small enough to not disrupt the overall crystal structure but sufficient to introduce additional charge carriers:
$$N << d$$
where $N$ is the concentration of dopant atoms and $d$ is the atomic density of the semiconductor.
There are two main types of doping:
1. **Doping with Pentavalent(Group V) Elements(n-type Doping)**: When a pentavalent element (like Phosphorus, Arsenic, or Antimony) is introduced into Silicon, it has 5 valence electrons. Four of these electrons form covalent bonds with neighboring Silicon atoms, and the fifth electron becomes a free electron in the conduction band. This creates a new energy level just below the conduction band, making it easier for electrons to be excited into the conduction band, called Dopant Energy Level $E_D$. This energy level is specific to the dopant and the crystal. When this energy level is occupied by an electron, is bond to remain close to the dopant atom, but it can be easily excited into the conduction band with minimal energy input. A good dopant has $\Delta E = E_C - E_D$ small, so that with minimal thermal energy, the electron can jump, emptying $E_D$, to the conduction band. This results in an increase in the number of free electrons in the conduction band $n$, thereby increasing the electrical conductivity of the material. Since electrons are negatively charged, this type of doping is called n-type doping. We define the donor concentration $N_D$ as the number of pentavalent dopant atoms per unit volume and we specify that:
	 $$N_D = \frac{\text{\# donor atoms}}{cm^3}, \quad N_D << d_{Si} \approx 10^{22} cm^{-3}$$
	 Doping should be large enough to modify significantly the population of the conduction band: 
	 $$1.45\times 10^{10} cm^{-3} \approx n_i << N_D << d \approx 10^{22} cm^{-3}$$
	 Now the dopant atom is ionized, meaning it has lost its extra electron and has a positive charge. The ionized dopant atom remains fixed in the lattice, while the free electron can move through the crystal, contributing to electrical conduction.
	 $$As \rightarrow As^{+} + e^{-}$$
	 where $As^{+}$ is the ionized Arsenic atom with a fixes charge $+q$ and $e^{-}$ is the free electron with charge $-q$ in the conduction band.
2. **Doping with Trivalent(Group III) Elements(p-type Doping)**: When a trivalent element (like Boron, Aluminum, or Gallium) is introduced into Silicon, it has 3 valence electrons. It can only form 3 covalent bonds with neighboring Silicon atoms, leaving one bond incomplete and creating a hole in the valence band. This creates a new energy level just above the valence band, making it easier for electrons from the valence band to jump into this hole, effectively creating more holes in the valence band, to fill the bond. This new energy level is called the Acceptor Energy Level $E_A$. When an electron from the valence band fills this hole, it leaves behind behind a new hole in the valence band, allowing for increased hole mobility and electrical conductivity. Since holes are positively charged, this type of doping is called p-type doping. We define the acceptor concentration $N_A$ as the number of trivalent dopant atoms per unit volume and we specify that: $$n_i<< N_A << d_{Si} \approx 10^{22} cm^{-3}$$ Now the dopant atom is ionized, meaning it has accepted an electron from the valence band and has a negative charge. The ionized dopant atom remains fixed in the lattice, while while the hole can move through the crystal, contributing to electrical conduction. 
	 $$B \rightarrow B^{-} + h^{+}$$
	 where $B^{-}$ is the ionized Boron atom with a fixed charge $-q$ and $h^{+}$ is the hole with charge $+q$ in the valence band, this is define as a virtual charge carrier because it represents the absence of an electron, not a physical particle.
##### Evaluation of n,p in Doped Material at Equilibrium
Equilibrium means that there are no external perturbations, so no energy exchange is possible. The system is in a steady state, and all macroscopic properties are constant over time. In a doped semiconductor at equilibrium, we define:
- Energy Distribution Function(for electrons in the conduction band):$$d_n = d_n (E) dE$$ where $d_n$ is the density of states function, which gives the number of available electron states per unit volume per unit energy range at a given energy $E$. The density of states function depends on the material and its band structure. $$n = \int_{E_C}^{E_{TOP}}d_n (E) dE \approx \int_{E_C}^{\infty}d_n (E) dE$$ where $E_{TOP}$ is the maximum energy of the conduction band, but we can approximate it to infinity because the density of states function decreases rapidly with increasing energy.
- Energy Distribution Function(for holes in the valence band):$$d_p = d_p (E) dE$$ where $d_p$ is the density of states function, which gives the number of available hole states per unit volume per unit energy range at a given energy $E$. The density of states function depends on the material and its band structure. $$p = \int_{E_{BOTTOM}}^{E_V}d_p (E) dE \approx \int_{-\infty}^{E_V}d_p (E) dE$$ where $E_{BOTTOM}$ is the minimum energy of the valence band, but we can approximate it to negative infinity because the density of states function decreases rapidly with decreasing energy.
$$d_n (E) = N_n (E) f_n(E)$$
$$d_p (E) = N_p (E) f_p(E)$$ where $N_n (E)$ and $N_p (E)$ are the crystal density of states functions for electrons for electrons and holes, respectively, given by the number of available states per unit volume per unit energy range at a given energy $E$. The functions $f_n(E)$ and $f_p(E)$ are the probability that a state at energy $E$ is occupied by an electron or a hole, respectively. These functions are only easily expressed in equilibrium conditions, since they depend on the Fermi level $E_F$, which is the energy level at which the probability of finding an electron is 50%. The Fermi level depends on the doping concentration and the temperature. That makes:
$$f_n(E) + f_p(E) = 1$$
Because we define the hole as a non-occupied electron state. 
In the end we only need to evaluate 3 functions: $N_n (E)$, $N_p (E)$ and $f_n(E)$.
##### Density of States for a 3D Crystal
The density of states function for electrons in the conduction band is given by:
$$N_n (E) = \gamma_n \sqrt{E - E_C}$$ where $\gamma_n$ is a constant that depends on the material and its band structure, given by:
$$\gamma_n = \frac{4 \pi (2 m_n^{*})^{3/2}}{h^3}$$ where $m_n^{*}$ is the effective mass of electrons in the conduction band, which takes into account the interaction of electrons with the crystal lattice, and $h$ is the Planck constant.

The density of states function for holes in the valence band is given by:
$$N_p (E) = \gamma_p \sqrt{E_V - E}$$ where $\gamma_p$ is a constant that depends on the material and its band structure, given by:
$$\gamma_p = \frac{4 \pi (2 m_p^{*})^{3/2}}{h^3}$$ where $m_p^{*}$ is the effective mass of holes in the valence band, which takes into account the interaction of holes with the crystal lattice, and $h$ is the Planck constant.
##### Effective Mass Theorem(Semi-Classical Motion of Free Particles)
Electrons in the conduction band and holes in the valence band move following the laws of classical mechanics($F = m a$) as free(the interaction with the environment is 0) particles, where $m$ is replaced by the effective mass $m^{*}$ of the particle under the condition of a perfectly periodic crystal.

It's counterintuitive because the attraction between the electron and the nucleus is not 0, but the interaction with the crystal lattice is 0 because of the periodicity of the crystal if we use the effective mass.
$$\text{Si:} \quad m_n^{*} \approx 1.15 m_0, \quad m_p^{*} \approx 1.07m_0$$ where $m_0 = 9.8 \times 10^{-31} kg$ is the mass of a free electron.
##### Probability of Occupation
The probability that an electron state at energy $E$ is occupied by an electron is given by the Fermi-Dirac distribution function:
$$f_n(E) = \frac{1}{1 + e^{\frac{E - E_F}{kT}}}$$ where $k$ is the Boltzmann constant and $T$ is the absolute temperature in Kelvin. The Fermi level $E_F$ depends on the doping concentration and the temperature. $kT$ is a normalizing factor used in statistical mechanics to express energy in terms of temperature. At room temperature ($T \approx 300 K$), $kT \approx 0.0259 eV$.
The probability that an electron state at energy $E$ is occupied by a hole is given by:
$$f_p(E) = 1 - f_n(E) = \frac{1}{1 + e^-{\frac{E - E_F}{kT}}}$$
## References
