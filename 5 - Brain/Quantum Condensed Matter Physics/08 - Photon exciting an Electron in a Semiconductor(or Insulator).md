
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
Where $\vec{E_{ph}} = \vec{E_0}(e^{i (\vec{k} \cdot \vec{r} - \omega t)} + e^{-i (\vec{k} \cdot \vec{r} + \omega t)})$ is the electric field vector, with $\vec{E_0}$ being the amplitude of the electric field, $\vec{k}$ the wave vector, and $\omega$ the angular frequency. 
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


## References
