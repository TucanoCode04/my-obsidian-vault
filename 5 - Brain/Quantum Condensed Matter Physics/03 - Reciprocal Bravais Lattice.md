
2025-10-08 10:50

Status: 

Tags:

# Reciprocal Bravais Lattice
We can associate a Bravais lattice in real space to a crystal structure. 
$$\vec{R_n} = n_1 \vec{a_1} + n_2 \vec{a_2} + n_3 \vec{a_3}, \quad n_i \in \mathbb{Z}$$
where $\vec{a_i}$ are the basis vectors of the lattice.

We can also define a new collection of vectors $\vec{G}$ that satisfy the condition:
$$\vec{R_n} \cdot \vec{G} = 2 \pi m, \quad m \in \mathbb{Z}$$
By further analysis, we can find that the dimension of $\vec{G}$ is $L^{-1}$, because $\vec{R_n}$ has dimension $L$ and the result of the dot product must be dimensionless. We call this new lattice the reciprocal lattice. Not every vector $\vec{G}$ will satisfy the condition, but only a discrete set of them.
The reciprocal lattice is defined by its own basis vectors $\vec{g_i}$, which need to satisfy the condition:
$$\vec{a_i} \cdot \vec{g_j} = 2 \pi \delta_{ij}$$
where $\delta_{ij}$ is the Kronecker delta, which is 1 if $i=j$ and 0 otherwise. This condition ensures that the basis vectors of the reciprocal lattice are orthogonal to the basis vectors of the real lattice.
The basis vectors of the reciprocal lattice can be calculated using the following formulas:
$$\vec{g_1} = 2 \pi \frac{\vec{a_2} \times \vec{a_3}}{\vec{a_1} \cdot (\vec{a_2} \times \vec{a_3})} $$
$$\vec{g_2} = 2 \pi \frac{\vec{a_3} \times \vec{a_1}}{\vec{a_2} \cdot (\vec{a_3} \times \vec{a_1})} $$
$$\vec{g_3} = 2 \pi \frac{\vec{a_1} \times \vec{a_2}}{\vec{a_3} \cdot (\vec{a_1} \times \vec{a_2})} $$
So the reciprocal lattice is defined as:
$$\vec{G}= h \vec{g_1} + k \vec{g_2} + l \vec{g_3}, \quad h,k,l \in \mathbb{Z}$$ where $h,k,l$ are integers that define the position of the vector in the reciprocal lattice.
The volume of the primitive cell in the reciprocal lattice, called the first Brillouin zone, is given by:
$$\Omega_{rec} = \frac{(2 \pi)^3}{\Omega_{dir}}$$
where $\Omega_{dir}$ is the volume of the primitive cell in the direct lattice, given by:
$$\Omega_{dir} = \vec{a_1} \cdot (\vec{a_2} \times \vec{a_3})$$
We can also calculate the volume of the primitive cell in the reciprocal lattice using the basis vectors of the reciprocal lattice:
$$\Omega_{rec} = \vec{g_1} \cdot (\vec{g_2} \times \vec{g_3})$$
##### Fourier Series and the Reciprocal Lattice
Since the lattice is periodic there exists observables that have the same periodicity as the underlying lattice. In general any observable $f(\vec{r})$ that respects the periodicity of the lattice must satisfy:
$$f(\vec{r}) = f(\vec{r} + \vec{R_n})$$
where $\vec{R_n}$ is a vector of the direct lattice.
That means we can express the observable as a Fourier series:
$$f(\vec{r}) = \sum_{\vec{k}} c_{\vec{k}} e^{i \vec{k} \cdot \vec{r}}$$ where $\vec{k}$ are the wave vectors of the Fourier series and have a dimension of $L^{-1}$.
The periodicity of the observable implies that:
$$f(\vec{r}) = f(\vec{r} + \vec{R_n}) \Rightarrow \sum_{\vec{k}} c_{\vec{k}} e^{i \vec{k} \cdot \vec{r}} = \sum_{\vec{k}} c_{\vec{k}} e^{i \vec{k} \cdot (\vec{r} + \vec{R_n})} = \sum_{\vec{k}} c_{\vec{k}} e^{i \vec{k} \cdot \vec{r}} e^{i \vec{k} \cdot \vec{R_n}}$$
This implies that:
$$e^{i \vec{k} \cdot \vec{R_n}} = 1 \Rightarrow \vec{k} \cdot \vec{R_n} = 2 \pi m, \quad m \in \mathbb{Z}$$
This is the same condition that defines the reciprocal lattice, so we can conclude that the wave vectors $\vec{k}$ must be vectors of the reciprocal lattice $\vec{G}$.
##### From Direct Lattice to Reciprocal Lattice
If we start from a direct lattice, we can calculate the basis vectors of the reciprocal lattice using the formulas provided above. We can construct the direct lattice using these general basis vectors:
$$\vec{R_n} = n_1 \vec{a_1} + n_2 \vec{a_2}, \quad n_i \in \mathbb{Z}$$
Now we can calculate the basis vectors of the reciprocal lattice:
$$\vec{a_1} \cdot \vec{g_1} = 2 \pi \Rightarrow |a_1||g_1| \cos(\theta) = 2 \pi \Rightarrow |g_1| = \frac{2 \pi}{|a_1|}$$
where $\theta$ is the angle between $\vec{a_1}$ and $\vec{g_1}$. Since they are parallel, $\cos(\theta) = 1$.
$$\vec{a_1} \cdot \vec{g_2} = 0 \Rightarrow |a_1||g_2| \cos(\theta) = 0 \Rightarrow \cos(\theta) = 0$$
where $\theta$ is the angle between $\vec{a_1}$ and $\vec{g_2}$. Since they are orthogonal, $\cos(\theta) = 0$.
Similarly we can find that:
$$\vec{a_2} \cdot \vec{g_1} = 0, \quad \vec{a_2} \cdot \vec{g_2} = 2 \pi \Rightarrow |g_2| = \frac{2 \pi}{|a_2|}$$
So the basis vectors of the reciprocal lattice are:
$$\vec{g_1} = \frac{2 \pi}{|a_1|} \hat{a_1}$$
$$\vec{g_2} = \frac{2 \pi}{|a_2|} \hat{a_2}$$
where $\hat{a_i}$ are the unit vectors in the direction of $\vec{a_i}$.
## References
