
2025-09-25 14:33

Status: 

Tags: [[Monocrystal]] [[Polycrystal]] [[Amorphous]] [[Silicon]] 

# Crystallography and Crystalline Defects

### Crystal Structure
Atoms are arranged on a regular grid called lattice, there are only 14 configurations(Bravais Lattices) and they differ in the angles between sides or the length between sides.
The most famous is the cubic structure, Silicon for example follows this structure.
The cubic structure presents 3 substructures: 
- simple cubic: which is the easiest structure but also the rarest. Only Polonium follow this structure
- body centered cubic(bcc): it presents an atom in the center of the cubic structure
- face centered cubic(fcc): it presents 6 atoms in the center, one for each face

To better identify the material we use the lattice parameter $a_0$ that tells us the length of a cube side. It's important for expitaxy for example.
### Silicon Lattice

The crystalline structure of Si(and Ge) is called Diamond(C). It's basically the interpenetration of 2 fcc lattices along the diagonal of the cube stopped at $\frac{1}{4}$ of the diagonal.
In this type of structure all atoms are equal and each of them is surrounded by 4 other atoms at the same distance forming a tetrahedron.

There exists a structure similar to the diamond structure called Zincblende, which is the interpenetration of 2 fcc lattices but with different atoms. For example GaAs and InP follow this structure.

Most semiconductors follow either the diamond or zincblende structure. One example of a semiconductor that doesn't follow this structure is SiC.
### Miller Indices

To fabricate quantum devices are rarely used thick materials, we normally use 2D thin layers which are obtained by cutting a bulky one. Depending on how you cut the material you will obtain different topographies which result in different properties. To describe the orientation of a cut, crystal plane, we use Miller indices. 

The process to determine this indices in the following:
- Determine the intercepts of the plane with the crystallographic axes in terms of the lattice parameters $(x_0, y_0, z_0)$. For example if the plane intercepts the x-axis at $2$, the y-axis at $-3$ and the z-axis at $4$, the intercepts are $(2, -3, 4)$.
- Take the reciprocals of these intercepts $\left(\frac{1}{x_0}, \frac{1}{y_0}, \frac{1}{z_0}\right)$. Following the previous example, the reciprocals are $\left(\frac{1}{2}, -\frac{1}{3}, \frac{1}{4}\right)$.
- Reduce these reciprocals to the smallest set of integers by multiplying by a common factor if necessary and then clear fractions. In the example, we first get $\left(\frac{6}{12}, -\frac{4}{12}, \frac{3}{12}\right)$ and then we get $(6, -4, 3)$.

The 3 most common planes for Si are:
- (100): it has the lowest number of dangling bonds(atoms which are not bonded to other atoms). The atoms whose present the dangling bonds are called surface atoms and they tend to react and capture O2 molecules from the air. So this type of configuration is used when we want to limit the contamination of the surface.
- (110)
- (111): it has the highest number of dangling bonds and is the most reactive surface. This configuration oxydizes the fastest, 70% faster than configuration (100).

In the etching process if you cut the same material along the 100 or the 111 configuration you will get completely different results.

We now understand that the analysis process of a crystal is very long and complex. We first need to determine whether the material is monocrystalline, polycrystalline or amorphous. Then we need to determine the crystalline structure and finally the Miller indices of the cut planes.
### Crystalline Defects
We distinguish 4 types of defects:
1. Point defects(0D)
2. Line defects(1D)
3. Surface defects(2D)
4. Volume defects(3D)
##### Point Defects
- Self Interstitial: an atom of the same type is located in an interstitial position(wrong place of the lattice). The effects it creates is of displacement of the neighboring atoms and the creation of stress fields that locally alter electronic properties.
- Vacancy: an atom is missing from its lattice site. The effects are similar to the self interstitial.
- Simple Interstitial: an atom of a different type is located in an interstitial position. There's an external contaminant, normally metal in case of Si. It's a pretty dramatic defect.
- Substitutional Defect: an atom of a different type replaces an atom in the lattice. This is the basis of doping. 

To dope a material you normally ionize the dopant atoms and accelerate them towards the substrate. When they hit the surface they penetrate it and occupy interstitial positions. The you heat the material to make the dopant atoms occupy vacancies.

These were the possible point defects for mono elements, if we were to analyze GaAs, we could find other type of defects, like:
- Antisite: an atom occupies a lattice site normally occupied by a different type of atom. For example a Ga atom occupies an As site.

No material is perfect, just by being in contact with the environment it will create point defects. For example if the teacher touches the wafer with his hands, he will introduce alkali metals like Na and K which are very mobile and will diffuse through the material creating substitutional defects.
##### Line Defects
- Edge Dislocation: an extra half-plane of atoms is inserted in a crystal(like the neck of the ingot in the CZ Process). This creates a compression in the region above the dislocation and a tension in the region below it. This isn't considered a plane defect because the distortion is limited the edge of the plane, layer by layer the distress decreases, so the defective region is only a line.

The defects are usually not fixed in position, they can move under the effect of stress or temperature. For example if you apply a shear stress to a crystal with an edge dislocation, the dislocation will move in the direction of the applied stress. Or even the dislocation during the CZ Process moves from the neck creating the full diameter of the ingot.
##### Surface Defects
- Grain Boundaries: interface between two grains or crystallites in a polycrystalline material. The grains can be of different materials or orientations. The boundaries have different properties than the grains themselves, like higher electrical resistivity or different chemical reactivity. It's important to know the average grain size to understand the properties of the material, because the smaller the grains, the more grain boundaries there are, which can significantly affect the material's properties.
##### Volume Defects
Whenever you put too much sugar in you coffee, so if the solute is greater than the solvent, if you don't heat the solution, the excess solute will precipitate out of the solution. The same thing happens in crystals. At high T, the solubility of impurities in a crystal increases. When the crystal cools down, the solubility decreases and the excess impurities precipitate out of the crystal, forming clusters or particles. 
Silicon is usually doped with Boron, Gallium or Indium because its solubility is high, so you have an higher range of freedom for the doping concentration. Even though these chemicals are from different groups in the Mendeleev table, they have a high solubility in Si. 

Micropipes are hollow tubes that can extend through the entire crystal, they are a killer defect causing short circuits in power devices. They are solved with Carbide, creating SiC.
## References
