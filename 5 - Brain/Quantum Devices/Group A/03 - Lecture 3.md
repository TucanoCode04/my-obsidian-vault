
2025-10-14 15:25

Status: 

Tags:

# Lecture 3
In order to provide a better understanding of the Fermi Energy level, we will see the graphical representation of the Fermi-Dirac distribution function.
![[Pasted image 20251016091018.png]]
We can first identify some asymptotes:
- For very high energy values, the probability of occupation tends to 0
- For very low energy values the probability of occupation tends to 1, meaning that all states are occupied
- At the Fermi level the probability of occupation is $\frac{1}{2}$
- The span of the transition region is $\approx 3kT$

The transition is monotonic, meaning that the probability of occupation decreases as the energy increases. 
The value of $T$ determines the slope of the transition region, the higher the temperature the smoother the slope $T_2 > T_1 = 300K$, the lower the temperature the steeper the slope $T_3 < T_1 = 300K$. 
When the temperature $T \to 0K$ the transition becomes a step function, in fact at $0K$ all the states below $E_F$ are occupied and all the states above it are empty. 

We now have all factors to get an expression for the populations of electrons in the conduction band and holes in the valence band at thermal equilibrium.
$$
n = \int_{E_C}^{\infty} \gamma_n \sqrt{E - E_C} \cdot \frac{1}{1 + e^{\frac{E - E_F}{kT}}} dE \quad , \quad n=n(E_F)
$$
$$
p = \int_{-\infty}^{E_V} \gamma_p \sqrt{E_V - E} \cdot \frac{1}{1 + e^{- \frac{E - E_F}{kT}}} dE \quad , \quad p=p(E_F)
$$
So the density of electrons and holes are integrals over energy that multiplies the density of states by the probability of occupation(Fermi-Dirac function).
We write $n = n(E_F)$ and $p = p(E_F)$ to highlight that the populations depend on the Fermi energy level.
We now have a system of 2 equations with 3 variables, $n$, $p$ and $E_F$.
$E_F$ depends on $n$ and $p$ at equilibrium, $n$ and $p$ depend on doping, so $E_F$ depends on doping. Because it influences the number of carriers, doping influences the Fermi level.
For zero doping, the semiconductor is intrinsic so we use the intrinsic carrier concentration $n_i$:
$$
n = n_i = n(E_{F_i}) \quad , \quad p = n_i = p(E_{F_i}) \quad \Rightarrow \quad n_i^2 = n(E_{F_i}) \cdot p(E_{F_i})
$$
Where $E_{F_i}$ is the intrinsic Fermi level.
Since doping changes the population from $n_i$ to $n$ and $p$, the Fermi level shifts from $E_{F_i}$ to $E_F$.
If we concentrate for example on the n-type doping, the number of carriers in modified to $n > n_i$, causing the Fermi level to shift up $E_F > E_{F_i}$, but $E_F$ is a also a variable in the expression for $p$, so there should be a corresponding decrease in the number of hole $p < n_i$. 
This correlation is $\sqrt{np} = n_i$ and is called the mass action law. We will see that this correlation stands only when the doping does not exceed a certain limit(the semiconductor is not degenerate(to check)).
A semiconductor is non-degenerate if $E_V < E_F < E_C$.
This guarantees that the Fermi level is in the band gap, so we can use the Boltzmann approximation to simplify the equations for $n$ and $p$.
1. For electrons:
$$E > E_F \quad \forall E \in CB \quad \Rightarrow \quad E - E_F > 0 \quad \Rightarrow \quad  e^{\frac{E - E_F}{kT}} >> 1$$
	So we can approximate the Fermi-Dirac distribution function as:
$$
f_n(E) \approx e^{- \frac{E - E_F}{kT}} = A e^{- \frac{E}{kT}}$$
	this is called the Boltzmann distribution, where $A = e^{\frac{E_F}{kT}}$ is a constant. 
	So we can rewrite the expression for $n$:
$$
n = N_C e^{- \frac{E_C - E_F}{kT}}$$
	this is called the Boltzmann relation, where $N_C$ is the effective density of states in the conduction band, which is a property of the material and depends on temperature:
$$
N_C = \gamma_n (kt)^{\frac{3}{2}} \frac{\sqrt{\pi}}{2}$$
If the Fermi level lies well within the band gap, the carriers population behaves as a classical gas, obeying Boltzmann statistics rather than Fermi-Dirac statistics, and the quantum nature of electrons can be neglected.
2. For holes:
$$E < E_F \quad \forall E \in VB \quad \Rightarrow \quad E - E_F < 0 \quad \Rightarrow \quad  e^{- \frac{E - E_F}{kT}} >> 1$$
	So we can approximate the Fermi-Dirac distribution function as:
$$
f_p(E) \approx e^{\frac{E - E_F}{kT}} = B e^{\frac{E}{kT}}$$
	this is called the Boltzmann distribution, where $B = e^{- \frac{E_F}{kT}}$ is a constant. 
	So we can rewrite the expression for $p$:
$$
p = N_V e^{- \frac{E_F - E_V}{kT}}$$
	this is called the Boltzmann relation, where $N_V$ is the effective density of states in the valence band, which is a property of the material and depends on temperature:
$$
N_V = \gamma_p (kt)^{\frac{3}{2}} \frac{\sqrt{\pi}}{2}$$

For an intrinsic material at equilibrium we have:
$$
n = n_i = N_C e^{- \frac{E_C - E_{F_i}}{kT}} = p = n_i = N_V e^{- \frac{E_{F_i} - E_V}{kT}}$$
From which we can derive:
$$
e^{\frac{E_{F_i} - E_C}{kT}} \cdot e^{\frac{E_{F_i} - E_V}{kT}} = \frac{N_V}{N_C} = \frac{\gamma_p}{\gamma_n} = \left( \frac{m_p^*}{m_n^*} \right)^{\frac{3}{2}}$$
We now that $\frac{m_p^*}{m_n^*}$ is very close to 1 for the mass action law to hold, sow e can approximate>
$$
e^{\frac{2E_{F_i} - (E_C + E_V)}{kT}} \approx 1 \quad \Rightarrow \quad \frac{2E_{F_i} - (E_C + E_V)}{kT} \approx \ln(\frac{N_V}{N_C} \approx 1) \approx 0 \quad \Rightarrow \quad E_{F_i} \approx \frac{E_C + E_V}{2} + \frac{kT}{2} \ln(\frac{N_V}{N_C})$$
So the intrinsic Fermi level lies close to the middle of the band gap, with a small correction negligible in semiconductors term that depends on temperature and the effective masses of electrons and holes.
If the Fermi energy level is exactly in the middle of the band gap, that's the best for degenerate semiconductors, because it maximizes the energy required for an electron to jump from the valence band to the conduction band, minimizing thermal generation of carriers.

We now want to verify the assumption:
$$
\begin{cases}
n = N_C e^{- \frac{E_C - E_F}{kT}} \\
p = N_V e^{- \frac{E_F - E_V}{kT}}
\end{cases} \quad \Rightarrow \quad np = N_C N_V e^{- \frac{E_C - E_V}{kT}} = N_C N_V e^{- \frac{E_g}{kT}}$$
The conjugate population $np$ does not depend on the Fermi level, even though it changes with doping, their product is not influenced. 
We use this relation, we use the simplest case where the dopant is 0, to define the mass action law, a relation between the instrinsic carrier concentration and the effective density of states in the conduction and valence band:
$$
np = n_i^2 = N_C N_V e^{- \frac{E_g}{kT}}$$
 where $N_CN_V \approx T^3$, explaining why semiconductors at high temperatures become more conductive, because the intrinsic carrier concentration increases and the doping effect is less relevant(to fact check).
##### Shockley's Equations $\Leftrightarrow$ Boltzmann Relations
Shockley's equations provide a physical meaning to the Boltzmann relations, maintaining their mathematical sense.
$$
\begin{cases}
n = N_C e^{- \frac{E_C - E_F}{kT}} \\
p = N_V e^{- \frac{E_F - E_V}{kT}}
\end{cases} \quad \xRightarrow{\text{Intrinsic case}} \quad \begin{cases}
n_i = N_C e^{- \frac{E_C - E_{F_i}}{kT}} \\
n_i = N_V e^{- \frac{E_{F_i} - E_V}{kT}}
\end{cases} \quad \Rightarrow \quad \begin{cases}
N_C = n_i e^{\frac{E_C - E_{F_i}}{kT}} \\
N_V = n_i e^{\frac{E_{F_i} - E_V}{kT}}
\end{cases} $$
Then we substitute in the original equations:
$$
\begin{cases}
n = n_i e^{\frac{E_C - E_{F_i}}{kT}} e^{- \frac{E_C - E_F}{kT}} = n_i e^{\frac{E_F - E_{F_i}}{kT}} \\
p = n_i e^{\frac{E_{F_i} - E_V}{kT}} e^{- \frac{E_F - E_V}{kT}} = n_i e^{\frac{E_{F_i} - E_F}{kT}}
\end{cases} \quad \Rightarrow \quad \begin{cases}
n-\text{TYPE} \leadsto E_F > E_{F_i} \\
p-\text{TYPE} \leadsto E_F < E_{F_i}
\end{cases}$$
The equations show that the carrier concentration depends exponentially on the difference between the Fermi level and the intrinsic Fermi level. Thus, the Fermi level moves upward in n-type materials and downward in p-type materials, telling us the number of carriers in the semiconductor, it can be viewed as a center of mass for our system.
$E_F$ grows as we increase doping in n-type semiconductors, while it decreases as we increase doping in p-type semiconductors. 
We exit from the general assumption as the doping increases, because the Fermi level can enter the conduction band in n-type semiconductors or the valence band in p-type semiconductors.  When this happens, the semiconductor is called degenerate, and we can no longer use the Boltzmann approximation, because $E_F$ is no longer in the band gap.

For a doped semiconductor, we can easily derive the third equation, allowing for the evaluation of $n$, $p$ and $E_F$, for an homogeneous semiconductor at thermal equilibrium.
At thermal equilibrium the total charge must be 0:
$$
\epsilon \oint_{\varepsilon} \hat{n} \cdot \vec{\varepsilon} d\sigma = \oint_{\Omega} \rho dv = 0$$
 where $\varepsilon$ is a closed surface enclosing a volume $\Omega$, $\hat{n}$ is the unit vector normal to the surface,(indicating the direction of the electric field when applying Gauss's law on the closed surface) $\vec{\varepsilon}$ is the electric field, $\rho$ is the charge density.
 The homogeneity of the semiconductor implies that the electric field is 0 everywhere(local charge neutrality). 
 Now we consider a semiconductor doped with $N_D$ donor atoms and $N_A$ acceptor atoms per unit volume, which are fully ionized at room temperature:
 $$
 \rho = q[p - n + N_D^+ - N_A^-]$$
 where $N_D^+$ is the concentration of ionized donors and $N_A^-$ is the concentration of ionized acceptors and $N^+ = N_D^+ - N_A^-$ is the net doping concentration.
 $N^+ > 0$ means n-type doping cause more donors than acceptors, while $N^+ < 0$ means p-type doping cause more acceptors than donors.
 The expression identifies the net charge density for every semiconductor.
 For a mature technology, we can assume that all dopants are ionized at room temperature:
 $$
 N_D^+ \approx N_D \quad , \quad N_A^- \approx N_A \quad \Rightarrow \quad N^+ = N_D - N_A$$
 So, by knowing the net doping concentration, we can write the charge neutrality condition:
 $$
 p - n + N^+ = 0 $$
 This is the third equation we were looking for.
 So considering a non-degenerate material, combining local neutrality and mass action law, we can solve the system of equations:
 1. For n-type doping, $N^+ > 0$:$$
 \begin{cases}
 n \cdot p = n_i^2 \\
 p - n + N^+ = 0 
 \end{cases} \quad \Rightarrow \quad p = \frac{n_i^2}{n} \quad \Rightarrow \quad n^2 - N^+ n - n_i^2 = 0 \quad \Rightarrow \quad n= \frac{N^+}{2} [1 + \sqrt{1 + \frac{4n_i^2}{(N^+)^2}}]$$
	 We discard the negative solution because the population cannot be negative.
$$
\begin{cases}
\text{if} \ n_i << N^+ \quad \Rightarrow \quad n \approx N^+ \\
\text{if} \ n_i >> N^+ \quad \Rightarrow \quad n \approx n_i
\end{cases}$$
	In the first case the doping is dominant, while in the second case the intrinsic carrier concentration is dominant.
In quantum devices we don't have the charge neutrality condition, because we have very small volumes, so we need to consider the full Poisson equation.
2. For p-type doping, $N^+ < 0$:
$$
\begin{cases}
n \cdot p = n_i^2 \\
p - n + N^+ = 0
\end{cases} \quad \Rightarrow \quad n = \frac{n_i^2}{p} \quad \Rightarrow \quad p^2 - |N^+| p - n_i^2 = 0 \quad \Rightarrow \quad p= \frac{|N^+|}{2} [1 + \sqrt{1 + \frac{4n_i^2}{(|N^+|)^2}}]$$
	We discard the negative solution because the population cannot be negative. And we use the absolute value of $N^+$ because it is negative.
$$
\begin{cases}
\text{if} \ n_i << |N^+| \quad \Rightarrow \quad p \approx |N^+| \\
\text{if} \ n_i >> |N^+| \quad \Rightarrow \quad p \approx n_i
\end{cases}$$
	In the first case the doping is dominant, while in the second case the intrinsic carrier concentration is dominant.

The limits of the net doping grants the usage of the non-degenerate assumption and the Boltzmann approximation.
Let's analyze a more general case.
1. For n-type doping, $N^+ >> n_i$:
$$
\begin{cases}
n \approx N^+ \quad \text{in the order of} 10^{15} cm^{-3} \\
p = \frac{n_i^2}{N^+} = 2.1 \cdot 10^{5} cm^{-3} \quad \text{for Si at RT}
\end{cases}$$
	Here $n$ and $p$ are called majority and minority carriers respectively. From the mass action law we can see that the minority carrier concentration is very low.
	Basically can define the position of $E_F$ using the equation for $n$.
	By combining the Shockley's equation, telling us the position of $E_F$ in respect to $E_{F_i}$:
$$
kt \ln(\frac{n}{n_i}) = E_F - E_{F_i}$$
	and the Boltzmann relation, telling us the position of $E_F$  in respect to $E_C$:
$$
kt \ln(\frac{N_C}{n}) = E_C - E_F$$ 








## References
