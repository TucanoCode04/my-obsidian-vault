
2025-10-01 08:23

Status: 

Tags: [[Silicon]], [[Crystal Structure]], [[Bravais Lattice]], [[Wigner-Seitz Cell]], [[FCC]], [[BCC]], [[Diamond Cubic]], [[C60]], [[Van der Waals Interactions]], [[Radial Distribution Function]]

# Introduction to the Crystal Structure
##### Crystal Lattice and Bravais Lattice
The crystal lattice is made of ions structures periodically repeated in a long range order.
Some example of these crystals can be NaCl, Urea and Ice.

The Bravais lattice is a geometrical and mathematical model to describe the periodicity and the physical formation of a crystal lattice.
- Geometrical: equivalent(meaning that whatever atom you choose, you will see always the same structure around it) points arranged periodically in an array
- Mathematical: linear combination of basis vectors multiplied by a coefficient: $$\vec{R_n} = n_1 \vec{a_1} + n_2 \vec{a_2} + n_3 \vec{a_3}, \quad n_i \in \mathbb{Z}$$
Primitive cell: smallest volume that, when translated through all the vectors of the Bravais lattice, fills all the space without overlapping or voids. It contains only one lattice point. 

Lattice point: position in space where the basis is located. 

For example if you have an atom with 4 nearest neighbors, the primitive cell will contain 1/4 of each atom, so in total it will contain 1 atom.

The difference between primitive cell and unit cell is that the unit cell is not necessarily the smallest volume, but it reflects the symmetry of the lattice. It can contain more than one lattice point.

We have a total of 14 Bravais lattices in 3D. The FCC and BCC do not respect the definition of primitive cell, but they are used because they reflect the symmetry of the lattice. 
##### Wigner-Seitz Cell
The Wigner-Seitz cell is a type of primitive cell that is constructed by drawing lines to connect a lattice point to all its nearest neighbors, then drawing the perpendicular bisectors of these lines. The region enclosed by these bisectors is the Wigner-Seitz cell. It reflects the symmetry of the lattice and is often used in solid state physics. In 3d it is constructed by planes instead of lines.

It is also referred as the region of points closer to a given lattice point than to any other lattice point.
##### How do we obtain the crystal structure from the Bravais lattice?
The Bravais lattice describes the underlying periodicity of the crystal, but it does not specify the actual arrangement of atoms within the lattice. To obtain the crystal structure, we need to add a basis to each lattice point. The basis is a group of atoms associated with each lattice point. By placing the basis at each lattice point and repeating it throughout the lattice, we can construct the full crystal structure.

We can have different crystal structures based on the same Bravais lattice by changing the basis. 

For example, Silicon is based on a FCC Bravais lattice, but it it has a basis of 2 atoms per lattice point. This basis creates the diamond cubic crystal structure. Another example is $C_{60}$, which is also based on a FCC Bravais lattice, but it has a basis of 60 atoms per lattice point, creating a completely different crystal structure.

FCC lattices contain 12 nearest neighbors per each atom, while BCC lattices contain 8 nearest neighbors per each atom. But when we add the basis, the number of nearest neighbors can change. For example, in the diamond cubic structure of Silicon, each atom has 4 nearest neighbors, despite being based on a FCC Bravais lattice and in Fullerene $C_{60}$, each atom has 3 strong covalent bonds with its nearest neighbors and a number of weaker van der Waals interactions with other nearby atoms.

Van der Waals interactions are weak attractive forces that occur between molecules or atoms due to temporary fluctuations in their electron distributions. These interactions are much interactions are much weaker than covalent or ionic bonds, which involve the sharing or transfer of electrons between atoms.

##### Creating Silicon
The Bravais lattice of Silicon is FCC:
$$\vec{R_{Si}} = x_1 \vec{a_1} + x_2 \vec{a_2} + x_3 \vec{a_3}, \quad 0 \leq x_i < 1$$
The basis is made of 2 atoms:
- Atom 1: ($0, 0, 0)$
- Atom 2: ($\frac{1}{4}$, $\frac{1}{4}$, $\frac{1}{4}$)

Which are called fractional coordinates.

In the cubic structure the basis vectors have all the same length $|\vec{a_i}| = 4.5 \text{Å}$ and they are orthogonal to each other $(\vec{a_i} \cdot \vec{a_j} = 0, i \neq j)$.
##### Amorphous Structures
There exists even amorphous structures, which do not present a long range order, but only a short range order. An example is amorphous Silicon(a-Si), which is used in thin film transistors for LCD displays and in photovoltaic cells. It still tries to create 4 covalent bonds per atom, but the angles between these bonds are not the ideal tetrahedral angle of 109.5°. This creates dangling bonds, which are unsatisfied covalent bonds that can trap charge carriers and affect the electronic properties of the material.
##### Radial Distribution Function
The radial distribution function (RDF) describes how the density of atoms varies as a function of distance from a reference atom. It is defined as: 
$$g(\vec{r})) = \frac{\rho(\vec{r})}{\langle{\rho}\rangle}$$
where $\rho(\vec{r})$ is the local density at a distance $\vec{r}$ from the reference atom and $\langle{\rho}\rangle$ is the average density of the system(which depends on the number of atoms and the volume of the system).
The RDF provides information about the short-range order of the system. In a crystalline solid, the RDF will show sharp peaks at specific distances corresponding to the positions of neighboring atoms. In an amorphous solid, the RDF will show broader peaks, indicating a lack of long-range order but still some short-range order and it will approach 1 at large distances, indicating that the density becomes uniform on average.

We calculate the RDF by taking a reference atom and counting the number of atoms in a spherical shell of thickness $d\vec{r}$ at a distance $r$ from the reference atom. 
##### Point Defects
In thermodynamics it's said that at room temperature, every crystal will have some defects. These defects influence the properties of the material, such as its electrical conductivity, mechanical strength, and diffusion behavior.

In Ionic solids, we can have:
- Schottky Defect: pair of vacancies, one cation and one anion, to maintain charge neutrality
- Frenkel Defect: cation vacancy and cation interstitial, maintaining charge neutrality

Creating vacancies and interstitials requires a lot of energy.

Interstitial points and vacancies create ionic conductivity in ionic crystals.

There is direct evidence that in ionic crystals charged is carried by ions and not by electrons(like in metals). It's easily demonstrated using electrodes, cause the ions will move towards the oppositely charged electrode, where we can find a neutral atom created by the ion that captured a charge from the electrode.

It requires less energy to move vacancies than to force an ion through the lattice. In ionic crystals, where Schottky defects are common, ionic conductivity is often due to the movement of vacancies. It is obtained by moving successively positively charged ions into neighboring vacancies, effectively causing the vacancies to move in the opposite direction. 
##### Point defects: color centers
Alkali-halide crystals(one first column and one seventh column of the periodic table) are transparent. 

NaCl is an example of alkali-halide crystal, but in powder form it is white, because the small crystals scatter the light.  

This crystals can be colored in different ways:
- By adding chemical impurities
- By irradiation with Gamma rays, X-rays or electrons/neutrons bombardment
- By electrolysis
- By heating the crystal in a reducing atmosphere creating an excess of metal ions(NaCl heated in Na vapor will create Na2Cl, which is yellow)

The color centers are called this way cause they absorb light in the visible range, creating color in the crystal.
##### Color centers: F-centers
When excess alkali atoms are added to an alkali-halide crystal, a corresponding number of halide ion(negative) vacancies are created to maintain charge neutrality. The electrons from the excess alkali atoms can become trapped in these halide ion vacancies, forming F-centers.

They are called F-centers from the German word "Farbe", meaning color, because they can absorb visible light and give color to the crystal.
##### Point defects in Diamond Cubic Structures
In diamond cubic structures, such as silicon and diamond, point defects can significantly impact the material's properties. Two common types of point defects in these structures are:
- Nitrogen-Vacancy (NV) Centers: These defects consist of a nitrogen atom substituting for a carbon atom adjacent to a vacancy. NV centers are of particular interest in quantum computing and quantum sensing due to their unique electronic and spin properties.
- Silicon-Vacancy (SiV) Centers: SiV centers involve a silicon atom substituting for 2 vacancies in the diamond lattice. 
## References
