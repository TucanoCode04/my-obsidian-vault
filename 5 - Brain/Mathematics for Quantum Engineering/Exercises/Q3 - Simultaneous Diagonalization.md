
2025-10-27 08:41

Status: 

Tags:

# Simultaneous Diagonalization
Check whether the two matrices:
$$S = \begin{pmatrix}
10 & 7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) \\
7(1 - i \sqrt{3}) & 10 & 7(1 + i \sqrt{3}) \\
7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) & 10
\end{pmatrix}$$
and
$$T = \begin{pmatrix}
2 & -1 & -1 \\
-1 & 2 & -1 \\
-1 & -1 & 2
\end{pmatrix}$$
can be simultaneously diagonalized by and orthonormal basis of $\mathbb{C}^3$. If so, write such a basis and provide a geometric interpretation.
### Solution
To determine whether the matrices $S$ and $T$ can be simultaneously diagonalized by an orthonormal basis of $\mathbb{C}^3$, we need to check if they commute, i.e., if $ST = TS$.
First, we compute the product $ST$:
$$ST = S \cdot T = \begin{pmatrix}
10 & 7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) \\
7(1 - i \sqrt{3}) & 10 & 7(1 + i \sqrt{3}) \\
7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) & 10
\end{pmatrix} \cdot \begin{pmatrix}
2 & -1 & -1 \\
-1 & 2 & -1 \\
-1 & -1 & 2
\end{pmatrix}$$
Calculating the entries of $ST$:
$$ST = \begin{pmatrix}
6 & - 3 + 21 i \sqrt{3} & - 3 - 21 i \sqrt{3} \\
-3 - 21 i \sqrt{3} & 6 & -3 + 21 i \sqrt{3} \\
-3 + 21 i \sqrt{3} & -3 - 21 i \sqrt{3} & 6
\end{pmatrix}$$

Next, we compute the product $TS$:
$$TS = T \cdot S = \begin{pmatrix}
2 & -1 & -1 \\
-1 & 2 & -1 \\
-1 & -1 & 2
\end{pmatrix} \cdot \begin{pmatrix}
10 & 7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) \\
7(1 - i \sqrt{3}) & 10 & 7(1 + i \sqrt{3}) \\
7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) & 10
\end{pmatrix}$$
Calculating the entries of $TS$:
$$TS = \begin{pmatrix}
6 & - 3 + 21 i \sqrt{3} & - 3 - 21 i \sqrt{3} \\
-3 - 21 i \sqrt{3} & 6 & -3 + 21 i \sqrt{3} \\
-3 + 21 i \sqrt{3} & -3 - 21 i \sqrt{3} & 6
\end{pmatrix}$$
Since $ST = TS$, the matrices $S$ and $T$ commute. Therefore, they can be simultaneously diagonalized by an orthonormal basis of $\mathbb{C}^3$.
To find such a basis, we can diagonalize one of the matrices and then check if the eigenvectors are also eigenvectors of the other matrix. Let's diagonalize $T$ first.
The characteristic polynomial of $T$ is given by:
$$\text{det}(T - \lambda I) = \text{det}\begin{pmatrix}
2 - \lambda & -1 & -1 \\
-1 & 2 - \lambda & -1 \\
-1 & -1 & 2 - \lambda
\end{pmatrix} = 0$$
Calculating the determinant:
$$\text{det}(T - \lambda I) = (2- \lambda) \left((2 - \lambda)^2 - 1\right) + 1 \left(-1(2 - \lambda) + 1\right) - 1 \left(-1 + (2 - \lambda)\right) = 0$$
$$ \Rightarrow (2 - \lambda)((2 - \lambda)^2 - 1) + 2 - 2\lambda = 0$$
$$ \Rightarrow (2 - \lambda)(\lambda^2 - 4\lambda + 3) + 2 - 2\lambda = 0$$
$$ \Rightarrow (2 - \lambda)(\lambda - 1)(\lambda - 3) + 2 - 2\lambda = 0$$
$$ \Rightarrow -\lambda^3 + 6\lambda^2 - 9\lambda = 0$$
Factoring out $\lambda$, we get:
$$ \lambda(\lambda^2 - 6\lambda + 9) = \lambda(\lambda - 3)^2 = 0$$
Thus, the eigenvalues of $T$ are $\lambda_1 = 0$ and $\lambda_2 = 3$ (with multiplicity 2).
Next, we find the eigenvectors corresponding to these eigenvalues.
For $\lambda_1 = 0$:
$$ (T - 0I)\mathbf{v} = 0 \Rightarrow T\mathbf{v} = 0 $$
Solving the system, we find that one eigenvector is:
$$Tv = 0 \Rightarrow \begin{cases}
2x - y - z = 0 \\
-x + 2y - z = 0 \\
-x - y + 2z = 0
\end{cases} \Rightarrow \mathbf{v_1} = \begin{pmatrix}1 \\ 1 \\ 1
\end{pmatrix}$$
For $\lambda_2 = 3$:
$$ (T - 3I)\mathbf{v} = 0 \Rightarrow \begin{pmatrix}
-1 & -1 & -1 \\
-1 & -1 & -1 \\
-1 & -1 & -1
\end{pmatrix}\mathbf{v} = 0 $$
Solving the system, we find that two linearly independent eigenvectors are:
$$\begin{cases}
x + y + z = 0
\end{cases} \Rightarrow x = -(y + z) \Rightarrow \mathbf{v_2} = \begin{pmatrix}1 \\ -1 \\ 0
\end{pmatrix}, \quad \mathbf{v_3} = \begin{pmatrix}1 \\ 0 \\ -1
\end{pmatrix}$$
If we normalize these eigenvectors, we get an orthonormal basis:
$$\mathbf{u_1} = \frac{1}{\sqrt{3}}\begin{pmatrix}1 \\ 1 \\ 1
\end{pmatrix}, \quad \mathbf{u_2} = \frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ -1 \\ 0
\end{pmatrix}, \quad \mathbf{u_3} = \frac{1}{\sqrt{2}}\begin{pmatrix}1 \\ 0 \\ -1
\end{pmatrix}$$
Now we do the same for matrix $S$:
The characteristic polynomial of $S$ is given by:
$$\text{det}(S - \lambda I) = \text{det}\begin{pmatrix}
10 - \lambda & 7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) \\
7(1 - i \sqrt{3}) & 10 - \lambda & 7(1 + i \sqrt{3}) \\
7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) & 10 - \lambda
\end{pmatrix} = 0$$
Calculating the determinant:
$$ \Rightarrow (10 - \lambda)((10 - \lambda)^2 - |7(1 + i \sqrt{3})|^2) + \ldots = 0$$
$$ \Rightarrow (10 - \lambda)(\lambda^2 - 20\lambda + 49) = 0$$
$$ \Rightarrow -\lambda^3 + 30\lambda^2 - 249\lambda + 490 = 0$$
Factoring, we find the eigenvalues of $S$ are $\lambda_1 = 0$, $\lambda_2 = 7$, and $\lambda_3 = 21$.
Next, we find the eigenvectors corresponding to these eigenvalues.
For $\lambda_1 = 0$:
$$ (S - 0I)\mathbf{v} = 0 \Rightarrow S\mathbf{v} = 0 $$
Solving the system, we find that one eigenvector is:
$$\mathbf{v_1} = \begin{pmatrix}1 \\ 1 \\ 1
\end{pmatrix}$$
For $\lambda_2 = 7$:
$$ (S - 7I)\mathbf{v} = 0 \Rightarrow \begin{pmatrix}
3 & 7(1 + i \sqrt{3}) & 7(1 - i \sqrt{3}) \\
7(1 - i \sqrt{3}) & 3 & 7(1 + i \sqrt{3}) \\








## References
