
2026-01-10 16:14

Status: 

Tags:

# Assignment Adami

### Exercise 1
![[Pasted image 20260110162940.png]]
The space of states of a particle is:
$$\mathcal{H} = L^2(\mathbb{R})$$
Meaning that the wave function $\psi(x)$ must be square integrable:
$$\int_{-\infty}^{\infty} |\psi(x)|^2 dx < \infty$$

The self-adjoint operators representing observables are:
**Position operator $\hat{x}$:**$$(\hat{X}\psi)(x) = x \psi(x)$$Which is not bounded, since:
$$\|\hat{X}\psi\|^2 = \int_{-\infty}^{\infty} |x \psi(x)|^2 dx$$
It's defined on the domain:
$$D(\hat{X}) = \{\psi \in L^2(\mathbb{R}) | \int_{-\infty}^{\infty} |x \psi(x)|^2 dx < \infty\}$$
**Momentum operator $\hat{p}$:**$$(\hat{P}\psi)(x) = -i \hbar \frac{d}{dx} \psi(x)$$Which is also not bounded, since:
$$\|\hat{P}\psi\|^2 = \int_{-\infty}^{\infty} \left| -i \hbar \frac{d}{dx} \psi(x) \right|^2 dx = \hbar^2 \int_{-\infty}^{\infty} \left| \frac{d}{dx} \psi(x) \right|^2 dx$$
It's defined on the domain:
$$D(\hat{P}) = \{\psi \in L^2(\mathbb{R}) | \frac{d}{dx} \psi(x) \in L^2(\mathbb{R})\}$$
**Kinetic energy operator $\hat{T}$:**$$(\hat{T}\psi)(x) = -\frac{\hbar^2}{2m} \frac{d^2}{dx^2} \psi(x)$$Which is also not bounded, since:
	
## References

