
2025-10-27 16:28

Status: 

Tags:

# Photon exciting an Electron in a Solid
We consider a photon with energy $E = \hbar \nu$ incident on a solid material. The photon can interact with the electrons in the solid, potentially exciting an electron from a lower energy state to a state whose gap is equal to the photon energy. 
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
$$ |c_f(t)|^2 = `frac`


## References
