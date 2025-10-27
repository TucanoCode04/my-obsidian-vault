
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
24 & -7(1 + i \sqrt{3}) & -7(1 - i \sqrt{3}) \\
-7(1 - i \sqrt{3}) & 24 & -7(1 + i \sqrt{3}) \\
-7(1 + i \sqrt{3}) & -7(1 - i \sqrt{3}) & 24
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




## References
