
2025-10-27 16:28

Status: 

Tags:

# Photon exciting an Electron in a Semicondutor(or Insulator)
We consider a photon with energy $E = \hbar \nu$ incident on a solid material. The photon can interact with the electrons in the solid, potentially exciting an electron from a lower energy state to a state whose gap is equal to the photon energy. The presence of energy gaps is due to the semiconductor(or insulator) physical properties.
The electrons in the solid feel an attractive potential from the positively charged atomic nuclei, which modifies their energy levels compared to free electrons. 
$$
\vec{p} = e \cdot \vec{r}
$$
This force is called dipole force. Where $e$ is the charge of the electron and $\vec{r}$ is the position vector from the nucleus to the electron. 
Classically the dipole force causes the electron to oscillate at the frequency of the incident electromagnetic wave $\nu$.
$$\Delta V = - \vec{p} \cdot \vec{E} \quad \Rightarrow \quad V(t) = - \vec{p} \cdot \vec{E_{ph}}$$
Where $\vec{E}$ is the electric field vector of the incident wave(the photon), that oscillates in time. $\Delta V$ is the change in potential energy of the electron due to the interaction with the electric field of the photon. That give us the time-dependent classical potential $V(t)$.
In quantum mechanics, we use operators to describe physical quantities. The potential energy operator $\hat{V}(t)$ corresponding to the classical potential $V(t)$ is given by:
$$\hat{V}(t) = -e \cdot \vec{r} \cdot \vec{E_{ph}}$$
Where $\vec{E_{ph}} = \vec{E_0}(e^{i (\vec{k} \cdot \vec{r} - \omega t)} + e^{-i (\vec{k} \cdot \vec{r} + \omega t)})$ is the electric field vector, with $\vec{E_0}$ being the amplitude of the electric field, $\vec{k}$ the photon wave vector(different from the $\vec{k}$ of the previous lesson), and $\omega$ the angular frequency. 
$$e^{i (\vec{k} \cdot \vec{r} - \omega t)} + e^{-i (\vec{k} \cdot \vec{r} + \omega t)} \propto \cos(\vec{k} \cdot \vec{r} - \omega t) $$
Represents plane waves propagating through space and oscillating in time. 
$$ \hat{V}(t) = -e \cdot \vec{r} \cdot \vec{E_0}(e^{i (\vec{k} \cdot \vec{r} - \omega t)} + e^{-i (\vec{k} \cdot \vec{r} + \omega t)})$$
Where the two exponential terms correspond to the absorption and emission of photons, respectively. This operator is the perturbation operator specific to a photon heating an electron in a solid.
##### Transition Rate Calculation
We will start by expanding the perturbation operator in the formula we derived in the previous lecture for the coefficient $c_f(t)$:
$$ V_{fi}(t) = \bra{\psi_f} \hat{V}(t) \ket{\psi_i} \quad \Rightarrow \quad c_f(t) = - \frac{1}{i \hbar} \int_0^t \bra{\psi_f} \hat{V}(t') \ket{\psi_i} e^{i E_{fi} t' / \hbar} dt' $$
Substituting the expression for $\hat{V}(t)$, we get:
$$ c_f(t) = -\frac{1}{i \hbar} \int_0^t \bra{\psi_f}e \vec{r} \cdot \vec{E_0}(e^{i (\vec{k} \cdot \vec{r} - \omega t)} + e^{-i( \vec{k} \cdot \vec{r} + \omega t)}) \ket{\psi_i} e^{i E_{fi} t' / \hbar} dt' $$
We will now rewrite the expression by separating the two exponential terms in positive and negative exponentials:
$$ c_f(t) = -\frac{1}{i \hbar} \int_0^t \bra{\psi_f}e \vec{r} \cdot \vec{E_0} e^{i \vec{k} \cdot \vec{r}} e^{-i \omega t'} \ket{\psi_i} e^{i E_{fi} t' / \hbar} dt' -\frac{1}{i \hbar} \int_0^t \bra{\psi_f}e \vec{r} \cdot \vec{E_0} e^{-i \vec{k} \cdot \vec{r}} e^{i \omega t'} \ket{\psi_i} e^{i E_{fi} t' / \hbar} dt' $$
We can factor out the time-independent terms from the integrals, since they depend only on position $\vec{r}$:
$$ c_f(t) = -\frac{1}{i \hbar} \bra{\psi_f}e \vec{r} \cdot \vec{E_0} e^{i \vec{k} \cdot \vec{r}} \ket{\psi_i} \int_0^t e^{- i\omega t'} e^{i E_{fi} t' / \hbar} dt' -\frac{1}{i \hbar} \bra{\psi_f}e \vec{r} \cdot \vec{E_0} e^{-i \vec{k} \cdot \vec{r}} \ket{\psi_i} \int_0^t e^{i \omega t'} e^{i E_{fi} t' / \hbar} dt' $$
We now define:
$$ M_{fi} = \bra{\psi_f}e \vec{r} \cdot \vec{E_0} e^{i \vec{k} \cdot \vec{r}} \ket{\psi_i}, \quad M_{fi}^* = \bra{\psi_f}e \vec{r} \cdot \vec{E_0} e^{-i \vec{k} \cdot \vec{r}} \ket{\psi_i} $$
Where $M_{fi}$ is the matrix element for the absorption of a photon, and $M_{fi}^*$ is the matrix element for the emission of a photon.
After solving the integral we can now calculate the transition probability $|c_f(t)|^2$, and successively the transition rate $R_{i \to f}$ by taking the derivative with respect to time:
$$ R_{i \to f} = \frac{d}{dt} |c_f(t)|^2 $$
$$ |c_f(t)|^2 = \frac{t^2}{\hbar^2} |M_{fi}|^2 \text{sinc}^2 [(E_{fi} - \hbar \omega) \frac{t}{2 \hbar}] + \frac{t^2}{\hbar^2} |M_{fi}^*|^2 \text{sinc}^2 [(E_{fi} + \hbar \omega) \frac{t}{2 \hbar}] + \text{cross terms} $$
Where $\text{sinc}(x) = \frac{\sin(x)}{x}$ and the cross terms oscillate rapidly and average to zero over time.
As time passes $c_f(t)$ should become larger(even larger than 1 due to the approximation), but physically the probability cannot exceed 1. The dependencies are still $t$ and $|M_{fi}|^2$. We now denominate the first term as $f_1$ and the second term as $f_2$.
![[Pasted image 20251027172948.png]]
The maximum of the function becomes sharper in time and approaches a delta function, near $E_{fi} = \hbar \omega$ for $f_1$. This means that the transition occurs when the energy difference between the final and initial states matches the photon energy, which is the condition for resonance absorption. 
$E_{fi} = \hbar \omega \quad \Rightarrow \quad E_f - E_i = \hbar \omega \quad \Rightarrow \quad E_f = E_i + \hbar \omega$
This condition represents the conservation of energy during the absorption process: the final energy of the electron after absorbing the photon is equal to its initial energy plus the energy of the photon.
![[Pasted image 20251027173410.png]]
For $f_2$, the maximum occurs at $E_{fi} = - \hbar \omega$, which corresponds to the emission of a photon. This is called stimulated emission, where an electron in a higher energy state can drop to a lower energy state by emitting a photon with energy $\hbar \omega$. As we can see in the figure, a photon is entering the system, but another photon is leaving the system, so the net effect is that a photon is emitted with the same energy as the incident photon.
$$ E_f = E_i - \hbar \omega $$
There exists also spontaneous emission, where an electron in a higher energy state can spontaneously drop to a lower energy state and emit a photon without the presence of an incident photon. This process is normally coupled with interactions with phonons or other particles to conserve momentum and energy.
In most practical scenarios, especially in semiconductors under illumination, absorption processes dominate over emission processes. Therefore, we will now focus on the first term $f_1$ related to absorption.
$$ |c_f(t)|^2= \frac{t^2}{\hbar^2} |M_{fi}|^2 \text{sinc}^2 [(E_{fi} - \hbar \omega) \frac{t}{2 \hbar}] $$
We now introduce:
$$\lim_{t \to \infty} \frac{\sin^2(\alpha t)}{\pi \alpha^2 t} = \delta(\alpha) $$
Where $\delta(\alpha)$ is the Dirac delta function. Using this limit we can rewrite the transition probability as:
$$ |c_f(t)|^2 = \frac{\pi t}{\hbar^2} |M_{fi}|^2 \delta(\frac{E_{fi} - \hbar \omega}{2 \hbar}), \quad \text{where} \quad \alpha = \frac{E_{fi} - \hbar \omega}{2 \hbar} $$
One of the properties of the delta function is:
$$ \delta(a x) = \frac{1}{|a|} \delta(x) $$
Using this property we can simplify the expression:
$$ |c_f(t)|^2 = \frac{2 \pi t}{\hbar} |M_{fi}|^2 \delta(E_{fi} - \hbar \omega) $$
This is the probability of transition from state $i$ to state $f$ due to the absorption of a photon with energy $\hbar \omega$. The delta function enforces the energy conservation condition, ensuring that transitions only occur when the energy difference between the initial and final states matches the photon energy.
With this expression for $|c_f(t)|^2$, we can now calculate the transition rate $W_{i \to f}$ by taking the derivative with respect to time:
$$ W_{i \to f} = \frac{d}{dt} |c_f(t)|^2 = \frac{2 \pi}{\hbar} |M_{fi}|^2 \delta(E_{fi} - \hbar \omega) $$
This is Fermi's Golden Rule applied to the case of photon absorption in a semiconductor or insulator. It gives the rate at which electrons transition from an initial state $\ket{\psi_i}$ to a final state $\ket{\psi_f}$ due to the interaction with the electromagnetic field of the photon.
In this expression $|M_{fi}|^2$ represents the perturbation strength, which depends on the overlap between the initial and final states and the interaction with the electric field of the photon. The delta function $\delta(E_{fi} - \hbar \omega)$ ensures that energy is conserved during the transition, meaning that the energy difference between the final and initial states must equal the photon energy $\hbar \omega$ for the transition to occur and is a derivative of space.
We have to consider the fact that there may be multiple coupled $\ket{\psi_i}$ and $\ket{\psi_f}$ states that satisfy the energy conservation condition. The overall transition rate $R_{i \to f}$ from the initial state to all possible final states is obtained by summing over all initial and final states:
$$ W_{i \to f} = \frac{2 \pi}{\hbar} \sum_{i,f} |M_{fi}|^2 \delta(E_{f} - E_{i} - \hbar \omega) $$
Empirically $\sum_{i,f} |M_{fi}|^2$ doesn't vary significantly with energy, so we can take it out of the summation, we can also define $g(\Delta E_{fi})$ as the joint density of states that counts the number of available final states per unit energy at the energy difference $\Delta E_{fi} = E_f - E_i$:
$$ W_{i \to f} = \frac{2 \pi}{\hbar} |M_{fi}|^2 g(\hbar \omega) $$
![[Pasted image 20251027180442.png]]
The difference between the joint density of states and the density of states is that the former considers a difference in energy between initial and final states, while the latter considers the number of available states at a specific energy level. For example in the figure, if we have 10 photons with energy $\hbar \omega$, the joint density of states $g(\hbar \omega)$ counts how many pairs of initial and final states exist such that the energy difference between them equals $\hbar \omega$(4). The density of states $D(E)$ counts how many states are available at a specific available energy level $E$(1 at $E_2$).
The absorption coefficient $\alpha \propto W_{i \to f}$ describes how much light is absorbed by the material per unit distance. We will see how it changes in direct and indirect bandgap semiconductors.
Reminder: now we would use the Fermi-Dirac distribution to account for the occupation probabilities of the initial and final states.
##### Absorption in Direct Bandgap Semiconductors
In direct bandgap semiconductors, the conduction band minimum and valence band maximum occur at the same momentum value in k-space. This means that an electron can directly transition from the valence band to the conduction band by absorbing a photon without any change in momentum.
![[Pasted image 20251027183635.png]]
The absorption changes with the photon energy.
We use the result derived previously for the transition rate:$$ W_{i \to f} = \frac{2 \pi}{\hbar} |M_{fi}|^2 g(\Delta E)$$ And for the potential matrix element representing the perturbation due to the photon:
$$ M_{fi} = \bra{\psi_f}e \vec{r} \cdot \vec{E_0} e^{i \vec{k} \cdot \vec{r}} \ket{\psi_i} $$
Note: here $\vec{k}$ is the photon wave vector, not the electron wave vector(perturbation).
We define the state wavefunctions for the initial and final states as Bloch states:
$$ \psi_i = \frac{1}{\sqrt{V}} e^{i \vec{k_i} \cdot \vec{r}} \mu_i(\vec{r}), \quad \psi_f = \frac{1}{\sqrt{V}} e^{i \vec{k_f} \cdot \vec{r}} \mu_f(\vec{r}) $$
Where $\mu_i(\vec{r})$ and $\mu_f(\vec{r})$ are the periodic parts of the Bloch functions, and $V$ is the normalization volume. 
Note: the electron wave vectors $\vec{k_i}$ and $\vec{k_f}$ are different from the photon wave vector $\vec{k}$.
Substituting these wavefunctions into the matrix element expression, we get:
$$ M_{fi} = \frac{1}{V} \int e^{-i \vec{k_f} \cdot \vec{r}} \mu_f^*(\vec{r}) e\vec{r} \cdot \vec{E_0} e^{i \vec{k} \cdot \vec{r}} e^{i \vec{k_i} \cdot \vec{r}} \mu_i(\vec{r}) d \vec{r}
$$
$$M_{fi} = \frac{1}{V} \int e^{i (\vec{k_i} - \vec{k_f} + \vec{k}) \cdot \vec{r}} \mu_f^*(\vec{r}) e \vec{r} \cdot \vec{E_0} \mu_i(\vec{r}) d \vec{r} $$
This expressions describes: a photon with wave vector $\vec{k}$ and its own momentum $\hbar \vec{k}$ hits an electron in the initial state with wave vector $\vec{k_i}$ and momentum $\hbar \vec{k_i}$. After the interaction, the electron transitions to the final state with wave vector $\vec{k_f}$ and momentum $\hbar \vec{k_f}$. The exponential term $e^{i (\vec{k_i} - \vec{k_f} + \vec{k}) \cdot \vec{r}}$ represents the conservation of momentum during the interaction.
$$ \hbar \vec{k} + \hbar \vec{k_i} = \hbar \vec{k_f} \quad \Rightarrow \quad \vec{k} + \vec{k_i} - \vec{k_f} = 0 $$
So the exponential term becomes $e^{i \cdot 0 \cdot \vec{r}} = 1$.
![[Pasted image 20251027185018.png]]
This can be seen by the vertical line in the first figure, where the electron transitions vertically in k-space without changing its momentum(since the momentum is given by the vertical lines).
Using the conservation of momentum, we can simplify the matrix element expression:
$$ M_{fi} = \frac{1}{V} \int \mu_f^*(\vec{r}) e \vec{r} \cdot \vec{E_0} \mu_i(\vec{r}) d \vec{r} $$
Depending on the symmetry properties of the initial and final states, this integral may be zero or non-zero. If the integral is non-zero, it indicates that the transition is allowed, and the electron can absorb the photon and move from the valence band to the conduction band. This defines the selection rules for optical transitions in direct bandgap semiconductors. For example in the harmonic oscillator model, transitions are allowed between states closed by one energy level. It depends on the symmetry of the wavefunctions.
In the visible light range(optical frequencies), the photon momentum $\hbar \vec{k}$ is much smaller than the typical electron momentum in the crystal. Therefore, we can approximate $\vec{k} \approx 0$ for optical optical transitions. Meaning, as we said before, that the electron momentum doesn't change during the interaction with the photon and it has vertical transition in k-space.
![[Pasted image 20251027192518.png]]
By using the parabolic band approximation near the band edges, we can define the two energy bands as:
$$ E_i = -\frac{\hbar^2 k_i^2}{2 m_h^*}, \quad E_f = E_g + \frac{\hbar^2 k_f^2}{2 m_e^*} $$
Where $m_h^*$ and $m_e^*$ are the effective masses of holes and electrons, respectively, and $E_g$ is the bandgap energy.
So the energy difference between the final and initial states is:
$$ \Delta E = E_f - E_i = E_g + \frac{\hbar^2 k_f^2}{2 m_e^*} + \frac{\hbar^2 k_i^2}{2 m_h^*} = E_g + \hbar^2 k_f^2 (\frac{1}{2 m_e^*} + \frac{1}{2 m_h^*}) $$
Where we used the momentum conservation $\vec{k_f} = \vec{k_i}$.
We can define the reduced effective mass $\mu$ as:
$$ \frac{1}{\mu} = \frac{1}{m_e^*} + \frac{1}{m_h^*} \quad \Rightarrow \quad \mu = \frac{m_e^* m_h^*}{m_e^* + m_h^*} $$
So the energy difference becomes:
$$ \Delta E = E_g + \frac{\hbar^2 k_f^2}{2 \mu} \quad \Rightarrow \quad \Delta E - E_g = \frac{\hbar^2 k_f^2}{2 \mu} $$
$\vec{k_f}$ is still discrete thanks to the periodic boundary conditions, so then we can calculate the number of allowed states($N$) and then the density of states($D(\Delta E)$) and so on.
We remember that $\frac{\text{number of states}}{\text{volume of the system}}= \text{joint density of states}$.
In the analytical calculation we found a dependence of $\sqrt{e}$, for the density of states in 3D systems.
For the joint density of states we have:
$$g(\Delta E) = g(\hbar \omega) = \frac{1}{2 \pi^2} (\frac{2 \mu}{\hbar^2})^{3/2} \sqrt{\hbar \omega - E_g}$$
Where $\hbar \omega$ is the photon energy. Only valid for $\hbar \omega \geq E_g$.
Otherwise $g(\hbar \omega) = 0$.
![[Pasted image 20251027193728.png]]
As we ca see from the graph, the joint density of states starts from zero at the bandgap energy $E_g$ and increases with the square root of the photon energy above the bandgap. This behavior is characteristic of direct bandgap semiconductors, where optical transitions can occur directly between the valence and conduction bands without any change in momentum.
The second graph shows $\alpha^2$ versus photon energy, which results in a linear relationship above the bandgap energy. This linearity is often used experimentally to determine the bandgap energy of direct bandgap semiconductors by extrapolating the linear portion of the $\alpha^2$ plot to the photon energy axis.
##### Resume
- the eigenfunctions of the unperturbed Hamiltonian of the semiconductor are Bloch functions, this represents the energy states of the electrons in the crystal lattice.
- the eigenvalues represent the energy levels energy levels associated with these Bloch functions, and are calculated using the parabolic band approximation near the band edges.
- the transition in direct bandgap semiconductors occurs vertically in k-space, meaning that the electron's momentum does not change during the transition.
- Matrix element $M_{fi}$ determines the probability amplitude for the transition between initial and final states, but it doesn't change much with energy.
- the selection rules for optical transitions depend on the symmetry properties of the initial and final states, for symmetry properties we mean whether the wavefunctions are even or odd functions. So certain transitions may be allowed or forbidden based on these symmetry considerations.
- the joint density of states is equal to the joint density of states of free particles with the reduced effective mass $\mu$.
- the intercept of the linear fit of $\alpha^2$ versus photon energy gives the bandgap energy $E_g$ of the semiconductor.
##### Band Structure of InAs
![[Pasted image 20251029130754.png]]
If you stray away from the band edges the parabolic band approximation is no longer valid, and we have to consider the actual band structure of the material. 
In our model we neglected two important aspects:
1. Excitonic Effects: When an electron is excited from the valence band to the conduction band, it leaves behind a positively charged hole. The electron and hole can form a bound state called an exciton due to their Coulomb attraction. This excitonic effect modifies the absorption spectrum, especially near the band edge, leading to additional absorption peaks below the bandgap energy.
2. Band Non-Parabolicity: The parabolic band approximation assumes that the energy-momentum relationship is quadratic near the band edges. However, in reality, the band structure can deviate from this simple parabolic shape, especially at higher energies. This non-parabolicity affects the density of states and the absorption characteristics, leading to deviations from the predictions based on the parabolic approximation.
##### InAs Optical Absorption Spectrum
![[Pasted image 20251029134923.png]]
##### Indirect Bandgap Semiconductors
In indirect bandgap semiconductors, the conduction band minimum and valence band maximum occur at different momentum values in k-space. This means that an electron cannot directly transition from the valence band to the conduction band by absorbing a photon alone, as this would violate momentum conservation. Instead, the transition requires the involvement of a phonon, which is a quantized lattice vibration that can provide or absorb momentum. 
![[Pasted image 20251029141318.png]]
Phonons are quanta of lattice vibrations in a crystalline solid, to better understand them we can think of them as collective excitations of atoms in the lattice that propagate as waves with their own momenta and energies. 
So the absorption edge(the minimum photon energy required for absorption) is assisted by phonons.
$$ \hbar \vec{k_{f}} = \hbar \vec{k_{i}} \pm \hbar \vec{q} $$
Where $\vec{q}$ is the phonon wave vector, and the plus sign corresponds to phonon absorption while the minus sign corresponds to phonon emission.
$$E_f = E_i + \hbar \omega \pm \hbar \Omega $$
Where $\hbar \Omega$ is the phonon energy. 
Since the process of absorption now involves 3 particles(electron, photon, phonon), the probability of collision is lower compared to direct bandgap semiconductors where only 2 particles are involved(electron and photon). This is called second-order process. The Fermi Golden rules becomes much more complicated since it considers the perturbation from both the photon and the phonon.
The absorption coefficient $\alpha$ is now plotted using the square root instead of the square, due to the more complex nature of the transition.
$$\alpha^{\text{indirect}} \propto (\hbar \omega - E_g \pm \hbar \Omega)^2 $$
![[Pasted image 20251029141349.png]]
Some indirect band gap materials are Silicon and Germanium. In particular Germanium has an indirect band gap of 0.66 eV and a direct band gap of 0.8 eV, so it can also show direct band gap behavior at higher photon energies as we can see in the figure. The indirect band gap absorption plotted in the direct band gap scale in almost zero.
![[Pasted image 20251029141639.png]]
Away from the parabolic band approximation we can see some more energy peaks in the absorption spectrum due to the actual band structure of the material. For example here in Germanium there are peaks $E_1$ and $E_2$ due to the bands being almost parallel one to another, leading to a high joint density of states and so a high absorption at those photon energies.
##### Excitons
In semiconductors and insulators, when an electron is excited from the valence band to the conduction band, it leaves behind a positively charged hole. The electron and hole can form a bound state called an exciton due to their Coulomb attraction. Excitons can significantly influence the optical properties of materials, especially near the band edge.
There are two main types of excitons:
1. Wannier-Mott Excitons(Free Excitons): These excitons have a large radius that extends over several lattice constants. They are typically found in materials with high dielectric constants and low effective masses for electrons and holes, semiconductors. This type of exciton is more delocalized and can move freely through the crystal lattice.
2. Frenkel Excitons(Tightly Bound Excitons): These excitons have a small radius, typically on the order of a lattice constant. They are commonly found in materials with low dielectric constants and and high effective masses for electrons and holes, such as organic semiconductors and molecular crystals, insulators. Frenkel excitons are more localized and are confined to specific lattice sites.
The excitons exists, basically this binding energy exists, if the interaction binding energy is greater than the thermal energy $k_B T$. At room temperature $k_B T \approx 25 meV$, so materials with exciton binding energies larger than this value can sustain excitons at room temperature.
Wannier-Mott excitons typically have binding energies in the range of $1-10 meV$, making them unsustainable at room temperature. They are more likely to exist at lower temperatures where thermal energy is reduced.
Frenkel excitons, on the other hand, can have binding energies ranging from $0.1 eV$ to several electron volts, making them stable at room temperature and even higher temperatures. In fact they are found in insulators.
##### Excitonic Effects on Optical Absorption
We now want to see how excitons affect the optical absorption spectrum of semiconductors.
We can see the exciton as a hydrogen-like system, where the electron and hole are bound together by Coulomb attraction. So can solve basically the Schrödinger equation for the hydrogen atom, but with modified parameters, the eigenvalues will also be discretized depending on the principal quantum number $n$.
The parameters we have to modify are:
1. Reduced Mass ($\mu$): In the exciton system, the reduced mass is given by:
	 $$ \frac{1}{\mu} = \frac{1}{m_e^*} + \frac{1}{m_h^*} $$
	 Where $m_e^*$ and $m_h^*$ are the effective masses of the electron and hole, respectively.
2. Dielectric Constant ($\epsilon_r$): The Coulomb interaction between the electron and hole is screened by the dielectric constant of the material. This reduces the effective Coulomb attraction compared to the hydrogen atom.
The exciton binding energy levels can be expressed as:
$$ E_n = -\frac{\mu}{m_0} \frac{1}{\epsilon_r^2} \frac{R_H}{n^2} = -\frac{R_X}{n^2} $$ Where $R_H$ is the Rydberg constant for hydrogen (approximately 13.6 eV), $m_0$ is the free electron mass, and $R_X$ is the exciton Rydberg energy, which is typically much smaller than $R_H$ due to the reduced mass and dielectric screening($\epsilon_r > \epsilon_0$, so as we can see from the formula the binding energy is reduced).
$$R_X = \frac{\mu}{m_0} \frac{R_H}{\epsilon_r^2}$$
The radius of the exciton can be expressed as:
$$ r_n = - \frac{m_0}{\mu} \epsilon_r n^2 a_H = n^2 a_X $$
Where $a_H$ is the Bohr radius for hydrogen (approximately 0.59 Å), and $a_X = \frac{m_0 \epsilon_r}{\mu} a_H$ is the exciton Bohr radius, which is typically larger than $a_H$ due to the reduced mass and dielectric screening.
So basically as $E_g$ increases, $R_X$ increases because the dielectric constant $\epsilon_r$ decreases. This means that in wide bandgap materials, excitons are more tightly bound and have higher binding energies. And $a_X$ decreases, meaning that the exciton is more localized.
![[Pasted image 20251029181302.png]]
So even after shining light with energy equal to the bandgap $E_g$, we can still have this pair of electron-hole bound states below the bandgap energy, leading to additional absorption peaks in the optical spectrum. To separate them we need energy greater than $\frac{R_X}{n^2}$.
To excite an exciton we will need $\Delta E(n) = E_g - \frac{R_X}{n^2}$. So this states will be below the bandgap energy $E_g$, because of the binding energy.
This means the excitement of excitons requires less energy than exciting free electron-hole pairs across the bandgap. This will lead to additional absorption peaks in the optical spectrum below the bandgap energy. As we said this peaks will only show up if the binding energy is greater than the thermal energy $k_B T$.
![[Pasted image 20251029181904.png]]
At lower energies we will see more excitonic peaks corresponding to different principal quantum numbers $n$. As the photon energy increases and surpasses the bandgap energy $E_g$, the absorption will transition to that of free electron-hole pairs, leading to a continuous absorption spectrum above the bandgap.
This can be seen in the GaAs absorption spectrum, where we can see the excitonic peaks below the bandgap energy $E_g$ and the continuous absorption above it.
![[Pasted image 20251029182029.png]]
Normally wide band gap materials(ex: NaCl, LiF) have Frenkel excitons, so we can't use the hydrogen-like model to describe them, since the electron and hole are tightly bound and localized on the same lattice site. 
![[Pasted image 20251029182429.png]]
##### Bulk Optical Emission
In bulk semiconductors, optical emission occurs when electrons in the conduction band recombine with holes in the valence band. This mechanism differs between direct and indirect bandgap semiconductors. 
In direct bandgap semiconductors, the conduction band minimum and valence band maximum occur at the same momentum value in k-space. This allows electrons to directly recombine with holes by emitting photons without any change in momentum. The emitted photons have energies close to the bandgap energy, resulting in efficient light emission. This property makes direct bandgap semiconductors ideal for optoelectronic applications such as light-emitting diodes (LEDs) and laser diodes.
In indirect bandgap semiconductors, the conduction band minimum and valence band maximum occur at different momentum values in k-space. As a result, the electron and the holes relax to the band edges, this process is called thermalization. As they relax, they lose energy by emitting phonons, which are quanta of lattice vibrations. Once the electrons and holes reach the band edges, there's a competition between luminescence(combination of electron and hole by emission of a photon) and phonon emission.
The process of luminescence can be exploited by injecting carriers(electrons and holes) into the semiconductor using electrical current or optical excitation. When these carriers recombine radiatively, they emit photons with energies close to the bandgap energy. 
![[Pasted image 20251029183144.png]]
The luminescence graph will show a peak at the bandgap energy, with a tail extending to lower energies due to phonon-assisted recombination processes.
![[Pasted image 20251029183132.png]]
## References
