
2025-11-12 18:00

Status: 

Tags:

# Josephson Effect and Quantum Superconducting Devices
Tunneling is a quantum mechanical phenomenon where particles pass through a potential barrier that they classically shouldn't be able to cross. This is due to the wave-like nature of of particles, allowing them to have a non-zero probability of being found on the other side of the barrier.
For normal electrons, tunneling can occur in tunneling junctions, where two conductors are separated by a thin insulating barrier. Classically tunnel junctions have infinite impedance at zero frequency, but quantum mechanically, if the barrier is thin enough, electrons can tunnel through it, allowing a small DC(direct current) to cross the junction(It is possible even for AC(alternating current) to cross the junction due to tunneling, but the DC case is more straightforward to understand).
We now first want to analyze a junction made of one conductor, the insulator and a superconductor. 
##### S-I-N(Superconductor-Insulator-Normal metal) Junction
![[Pasted image 20251112221444.png]]
The S-I-N junction consists of a superconductor(S) and a normal metal(N) separated by a thin insulating barrier(I). A voltage V is applied across the junction, with the superconductor at a higher potential than the normal metal, so basically the current flows from the normal metal to the superconductor.
In a S-I-N junction, the superconductor has a gap in its density of states around the Fermi level, while the normal metal has a continuous density of states. When a voltage is applied across the junction, electrons from the normal metal can tunnel into the superconductor only if they have enough energy to overcome the superconducting gap. This results in a characteristic I-V(current-voltage) curve with a threshold voltage corresponding to the superconducting gap.
More specifically Cooper-pairs in the superconductor cannot tunnel into the normal metal as single electrons, they need to break up into two single electrons, each having energy at least equal to the superconducting gap $\Delta$. Therefore, no current flows until the applied voltage V exceeds $\frac{\Delta}{e}$, where e is the electron charge. Beyond this threshold, the current increases as more electrons gain enough energy to tunnel into the superconductor.
![[Pasted image 20251112221522.png]]
So figuratively, the valence band of the normal metal aligns with the conduction band of the superconductor when the voltage exceeds $\frac{\Delta}{e}$, allowing electrons to tunnel through the barrier. In the second figure we can appreciate how we see current flowing only after the voltage exceeds $\frac{\Delta}{e}$.
##### S-I-S(Superconductor-Insulator-Superconductor) Junction and the Josephson Effect
![[Pasted image 20251112222939.png]]
The S-I-S junction consists of two superconductors separated by a thin insulating barrier. In this case, Cooper pairs must be broken in both superconductors for normal electron tunneling to occur. It even requires double the energy compared to the S-I-N junction, to align the valence band of one superconductor with the conduction band of the other superconductor. Therefore, no current flows until the applied voltage V exceeds $\frac{2\Delta}{e}$.
![[Pasted image 20251112223238.png]]
However, a small zero-bias(meaning no voltage applied) current was experimentally observed in S-I-S junctions, which was unexpected based on the probability of normal electron tunneling. This phenomenon is still very unlikely since it's the joint probability of two electrons tunneling simultaneously(direct tunneling of Cooper-pair).
![[Pasted image 20251113105458.png]]
The upper part of the graph shows various regions:
- $|I| < I_c$ and $V= 0$: This is the DC Josephson effect region, where a supercurrent flows without any voltage across the junction, due to the tunneling of Cooper pairs.
- $|I| \leq I_c$ and $0 < V < \frac{2\Delta}{e}$: This is the AC Josephson effect region, where a voltage is applied to the junctions causing the phase difference between the superconductors to change over time, resulting in an alternating supercurrent between the superconductors.
- $|I| \leq I_c$ and $V \geq \frac{2\Delta}{e}$: The voltage is high enough to break Cooper pairs in both superconductors, allowing both normal electron tunneling and Cooper pair tunneling to occur.
- $|I| > I_c$: The current exceeds the critical current, leading to a resistive state where normal electron tunneling dominates.
## References
