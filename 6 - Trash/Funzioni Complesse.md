
2025-09-16 13:52

Status: 

Tags: [[Numeri Complessi]] 

# Funzioni Complesse
### 1.1 Numeri complessi

I numeri complessi sono stati inventati per dare significato all'espressione $\sqrt{-1}$. 
I numeri complessi $z \in \mathbb{C}$ sono combinazioni lineare di una parte reale $x$ e una parte immaginaria $y$:
$$
z = x + iy
$$
con $x, y \in \mathbb{R}$.
Definiamo il complesso coniugato di un numero complesso come:
$$
z^*=x - iy
$$
Possiamo quindi immaginare la parte reale e immaginaria come le coordinate cartesiane del punto rappresentante il numero complesso, chiamata **forma cartesiana**.
Un punto può essere anche descritto in coordinate polari, questo ci porta alla descrizione dei numeri complessi in termini di una coordinata radiale $\rho$ e una coordinata angolare $\theta$. Esse sono legate alle coordinate $x, y$ da:
$$
\begin{cases}
x = \rho \cos \theta \\
y = \rho \sin \theta
\end{cases}
\Rightarrow
\begin{cases}
\rho = |z| = \sqrt{x^2 + y^2} & \text{modulo di z} \\
\theta = \arg z = \arctan \frac{y}{x} + 2k\pi & \text{argomento(o fase) di z}
\end{cases}
$$
Quindi, possiamo scrivere:
$$
z = \rho \cos \theta + i \rho \sin \theta
$$
Il numero complesso di argomento $\arg z= \theta + 2k\pi$ per qualunque $k \in \mathbb{Z}$ coincide, per la periodicità di seno e coseno al numero complesso $z$. 

Ricordiamo le espansioni in serie di seno e coseno
$$
\begin{align*}
\cos \theta = \sum_{k=0}^{\infty} \frac{(-1)^k \, \theta^{2k}}{(2k)!}
\\
\sin \theta = \sum_{k=0}^{\infty} \frac{(-1)^k \, \theta^{2k+1}}{(2k+1)!}
\end{align*}
$$
Entrambe, convergenti su tutto $\mathbb{R}$, il che ci porta all'**identità di Eulero**. 
$$
e^{i\theta} = \cos \theta + i \sin \theta
$$
Da cui discende che ogni numero complesso può essere rappresentato nella forma polare:
$$
z = \rho e^{i\theta} = |z| e^{i \arg z}
$$
Dove il suo complesso conigiuato sarà:
$$
z^* = \rho e^{-i\theta} = |z| e^{-i \arg z}
$$
Da cui, se $\theta \in \mathbb{R}$:
$$
|e^{i\theta}| = 1
$$

### 1.2 Funzioni di variabile complessa

Considerando un sottinsieme $\mathcal{M} \subseteq \mathbb{C}$. Una funzione complessa è una legge che associa un numero $w \in \mathbb{C}$ a un numero $z \in \mathcal{M}$:
$$
f: \mathcal{M} \rightarrow \mathbb{C}, \quad w = f(z) \quad \text{univoca (a un sol valore o monodroma)}
$$
Ponendo $z = x + iy$ e $w = u + iv$:
$$
f(z) = u(x,y) + iv(x,y) \quad u,v: \mathbb{R}^2 \rightarrow \mathbb{R}^2
$$
Quindi i concetti di limite e continuità sono ereditati da quelli delle funzioni $\mathbb{R}^2 \rightarrow \mathbb{R}^2$.

**Definizione.** Un numero $A \in \mathbb{C}$ è detto limite di $f$ per $z$ che tende ad $a \in \mathbb{C}$ e si scrive:
$$
A = \lim_{z \to a} f(z)
$$
se per ogni intorno $U_A$ di $A$ piccolo a piacere esiste un introno 4U_a$ di $a$ tale che $\forall z \in U_a \Rightarrow f(z) \in U_A$, ovvero per $\forall \epsilon > 0$ (piccolo a piacere) $\exists \delta > 0$ tale che
$$
0 < |z - a| < \delta \;\;\Rightarrow\;\; |f(z) - A| < \varepsilon
$$
Ovviamente
$$
\lim_{z \to a} f(z) = A \;\;\Leftrightarrow\;\;
\begin{cases}
\lim_{z \to a} \Re(f(z)) = \Re A \\
\lim_{z \to a} \Im(f(z)) = \Im A
\end{cases}
$$
**Definizione.** Una funzione $f(z)$ è continua in $a$ se
$$
\lim_{z \to a} f(z) = f(a)
$$
Per avere funzioni complesse ben definite è necessario provare che tali serie siano convergenti in un opportuno dominio.
Può essere dimostrato nel piano complesso, come già nell'insieme dei reali, un criterio di convergenza di Cauchy.

**Teorema.** La successione delle ridotte di una serie è convergente se:
$$
|S_N(z) - S_M(z)| < \varepsilon
$$

### 1.3 Differenziabilità e olomorfismo

Come abbiamo visto, una funzione in $\mathbb{C}$ è un caso particolare delle funzioni $\mathbb{R}^2 \rightarrow \mathbb{R}^2$.

**Definizione.** *Differenziabilità in $\mathbb{R}^2$*. Sia $\Omega$ un insieme aperto di $\mathbb{R}^2$ e sia $f: (x,y) \in \Omega$. Allora si dice che $f$ è differenziabile in $(x_0, y_0) \in \Omega$ se esiste una forma lineare $\alpha\Delta x + \beta \Delta y$ detta differenziabile, tale che:
$$
f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0) = \alpha \Delta x + \beta \Delta y + \omega(\Delta x, \Delta y) \sqrt{\Delta x^2 + \Delta y^2}
$$
con $\omega(\Delta x, \Delta y) \to 0$ per $\Delta x, \Delta y \to 0$.

Se $f$ è differenziabile in $(x_0, y_0)$, allora esistono le derivate parziali:
$$
\frac{\partial f}{\partial x}(x_0, y_0) = \alpha, \quad \frac{\partial f}{\partial y}(x_0, y_0) = \beta
$$
che vanno a formare il differenziale:
$$
df = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy
$$
Nel caso complesso si deve però soddisfare anche una condizione aggiuntiva:
$$
\Delta z = \Delta x + i \Delta y
$$
Il che ci porta a dover introdurre il concetto di olomorfismo.

**Definizione.** *Olomorfismo.* 




## References
[[Capitolo 1 Fisica Teorica]]
