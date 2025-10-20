
2025-10-20 11:46

Status: 

Tags:

# Lecture 6
##### A different way to build the equilibrium band diagram 
We separate two pieces of crystal, one p type and one n type, of the non homogeneous device(like we did before at $t<0$). 
The only energy shared at this point in the system is a free electron energy level, defined as the minimum energy required to bring a free electron outside its subsystem.
![[Pasted image 20251019184435.png]]
##### For example in Metals
The $q\phi_M$ is the energy required to bring an electron from the Fermi level inside the metal to the vacuum level just outside the metal surface. The only levels that are occupied are the ones below the Fermi level, inside the material, this meaning an abundance of free electrons. The large number of electrons is due to the fact that in metals the conduction band and valence band overlap, so there is no energy gap, so many electrons from the valence band can occupy states in the conduction band, basically detaching themselves from the atoms and becoming a sea of free electrons.
![[Pasted image 20251020115350.png]]
##### Continuing from the second step
In the secondo step we compare the values of $E_F$ in the two regions. At the time of contact($t=0$) free carriers flow according to the concentration gradients: electrons from the material with larger $E_F$ to the material with smaller $E_F$, and holes in the opposite direction. This flow of carriers creates charged regions close to the junction($\rho \neq 0$), generating a built-in electric field and built-in voltage that opposes the diffusion currents, required to restore the equilibrium condition of detailed balance. 
A prediction on $\rho(x)$ becomes now possible, since the flow of electrons and holes will leave behind ionized impurity atoms in the depletion region. 
Far from the junction, the material remains neutral($\rho = 0$), since the free carrier densities are very high compared to the ionized impurity densities. So the number of holes equals the number of ionized acceptors in the p region, and the number of electrons equals the number of ionized donors in the n region. Near the junction, we will have a region with $\rho < 0$ on the p side, since electrons have diffused into the p region leaving behind negatively ionized acceptor atoms, and a region with $\rho > 0$ on the n side, since holes have diffused into the the n region leaving behind positively ionized donor atoms. Global neutrality is still valid $\int_{x_1}^{x_2} \rho(x) dx = 0$, with $x_1$ and $x_2$ far from the junction.
The shape depends on how the charges distribute close to the junction, but we can approximate it with the depletion approximation used before.
To finalize the band diagram at equilibrium, we draw the constant Fermi level $E_F$ across the device, we then add the $x$ axis with the relevant points characterizing the charge distribution $\rho(x)$.
![[Pasted image 20251020122600.png]]
In the neutral regions the band diagram satisfies Poisson's equation for electrostatic energy for electrons:
$$\frac{d^2 U}{d x^2}= q\frac{\rho(x)}{\epsilon} = 0 \quad \Rightarrow \quad \frac{d U}{d x} = -q \frac{d \psi}{d x} = q \varepsilon$$
Meaning that $U(x)$ is linear with constant slope in the neutral regions.
In the depletion region, the band diagram satisfies Poisson's equation with $\rho(x) \neq 0$, leading to parabolic shapes as before.
$$\frac{d^2 U}{d x^2}= q\frac{\rho(x)}{\epsilon} \quad \Rightarrow \quad \begin{cases} \text{concave down for } \rho(x) < 0 \\ \text{concave up for } \rho(x) > 0 \end{cases}$$
![[Pasted image 20251020123036.png]]
Now we need to calculate the built-in voltage $V_{bi}$, using the work functions of the two regions:
$$q V_{bi} = q\phi_{s_p} - q\phi_{s_n}$$ Where $q\phi_{s_p}$ is the work function of the p region and $q\phi_{s_n}$ is the work function of the n region. The work function is defined as the energy required to bring an electron from the Fermi level inside the material to the vacuum level just outside the material surface.
$$q V_{bi} = [q \chi + \frac{E_g}{2} + kt\ln(\frac{N_A}{n_i})] - [q \chi + \frac{E_g}{2} + kt\ln(\frac{N_D}{n_i})] = kt \ln(\frac{N_A N_D}{n_i^2})$$ where $q \chi$ is the electron affinity of the semiconductor, which is the energy required to bring an electron from the conduction band minimum inside the material to the vacuum level just outside the material surface, $E_g$ is the energy gap of the semiconductor, $k$ is the Boltzmann constant, $t$ is the temperature in Kelvin, $N_A$ and $N_D$ are the acceptor and donor doping concentrations respectively, and $n_i$ is the intrinsic carrier concentration of the semiconductor. So we evaluated the built-in voltage $V_{bi}$ in function of the doping concentrations and intrinsic properties of the semiconductor.
$$V_{bi} = \frac{kt}{q} \ln(\frac{N_A N_D}{n_i^2})$$
$\frac{kt}{q} = V_T$ is the thermal voltage, which at room temperature(300K) is approximately 25.9 mV, which is the energy scale associated with thermal energy at a given temperature.
Now we can use this expression for $V_{bi}$ to find the depletion region widths $x_n$ and $x_p$ as before.
$$\begin{cases}
q \phi_p = E_o(-x_p) - E_o(0) = q [\psi(0) - \psi(-x_p)] \quad \Rightarrow \quad \phi_p = \frac{q N_A}{2 \epsilon} x_p^2 \\
q \phi_n = E_o(0) - E_o(x_n) = q [\psi(x_n) - \psi(0)] \quad \Rightarrow \quad \phi_n = \frac{q N_D}{2 \epsilon} x_n^2
\end{cases}$$
Where $E_o(x)$ is the electron potential energy in function of position $x$.
$$\begin{cases}
V_{bi} = \phi_n + \phi_p = \frac{q N_D}{2 \epsilon} x_n^2 + \frac{q N_A}{2 \epsilon} x_p^2 \\
N_A x_p = N_D x_n
\end{cases} \quad \Rightarrow \quad V_{bi} = \frac{q N_D}{2 \epsilon} \left(\frac{N_D}{N_A} +1\right) x_n^2$$
 where $\left(\frac{N_D}{N_A} +1\right) = \frac{N_A + N_D}{N_A}$, which leads to:
 $$x_n^2 = \frac{2 \epsilon}{q N_D} \cdot \frac{N_A}{N_A + N_D} V_{bi}$$
  we multiply by $\frac{N_D}{N_D}$, so we can use the $N_{eq} = \frac{N_A N_D}{N_A + N_D}$ equivalent doping concentration since the $N_A \parallel N_D$ is a parallel association of doping concentrations:
  $$x_n =  \frac{1}{N_D} \sqrt{ \frac{2 \epsilon}{q} N_{eq} V_{bi}} \quad \Rightarrow \quad \begin{cases} x_p = \frac{1}{N_A} \sqrt{ \frac{2 \epsilon}{q} N_{eq} V_{bi}} \\ x_d = x_n + x_p = \left(\frac{1}{N_A} + \frac{1}{N_D}\right) \sqrt{ \frac{2 \epsilon}{q} N_{eq} V_{bi}} \end{cases}$$
   where $x_d$ is the total depletion region width.
Now we have all the parameters to evaluate the band diagram of the pn junction at equilibrium using this different approach. 
$$ \begin{cases} 
x_n = x_d \frac{N_A}{N_A + N_D} \\
x_p = x_d \frac{N_D}{N_A + N_D}
\end{cases} \quad \Rightarrow \quad \begin{cases}
\phi_n = V_{bi} \frac{N_A}{N_A + N_D} \\
\phi_p = V_{bi} \frac{N_D}{N_A + N_D}
\end{cases}$$
We can easily see a correlation between the doping concentrations and the depletion region widths and potential differences: the region with higher doping concentration has a smaller depletion width and smaller potential difference.
$$ \frac{\phi_n}{\phi_p} = \frac{x_n}{x_p}$$
We can derive from this relationship, the behavior of the band diagram when we change the doping concentrations, for example for strongly asymmetric doping:
$$ N_A \gg N_D \iff p^+n\text{ junction} \quad \Rightarrow \quad \begin{cases} x_n \approx x_d \rightarrow x_p \ll x_d \\ \phi_n  \approx V_{bi} \rightarrow \phi_p \ll V_{bi} \end{cases}$$
$$ N_D \gg N_A \iff pn^+ \text{ junction} \quad \Rightarrow \quad \begin{cases} x_p \approx x_d \rightarrow x_n \ll x_d \\ \phi_p  \approx V_{bi} \rightarrow \phi_n \ll V_{bi} \end{cases}$$
## References
