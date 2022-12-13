# Tutorial 5 -Quantum simulation with cold atoms


In the previous lessons we talked about [trapped ions](qhw3) and [superconducting qubits](qhw4). They are the leading platforms for the creation of **universal quantum computers**, which hold the premise of exponential speed-up for a variety of NP-hard problems. However, this universality usually comes at the price of algorithmic overhead for a wide range of tasks which generally leads to worse overall fidelity. If we give up the constraint of a universal quantum computer, we can build specialized quantum hardware for the problems of interest. Such systems are called quantum simulators. Cold atoms have become a leading platform of such quantum simulators at a large scale. Already demonstrated applications involve an enormous variety of condensed-matter problems like e.g. the [Hubbard model](https://journals.aps.org/rmp/abstract/10.1103/RevModPhys.80.885), topological systems, [superfluidity](https://www.sciencedirect.com/science/article/abs/pii/S1049250X06540017?via%3Dihub) and [disorder](https://physicstoday.scitation.org/doi/10.1063/1.3206091). More recently, cold atoms started to find applications to [Ising models](https://arxiv.org/abs/2002.07413) and [high-energy physics](https://royalsocietypublishing.org/doi/full/10.1098/rsta.2021.0064). 

## Summary for the cold atoms hardware 

Ultracold atoms are gases that are well isolated from the environment and are cooled to near zero and in this regard quite close to trapped ion systems, which also heavily draw on the experimental techniques of atomic physics and optics. At such low temperatures, quantum effects are dominant in the behavior of the gas cloud. Thanks to their precise control and flexibility, they are now a well-established platform for the quantum simulation of complex quantum problems. 

The high precision and versatility have made cold atoms one of the dominating quantum hardware platforms in the European academic research sector. To underline the fact, in Heidelberg alone there are four research groups working with cold atoms. Munich, Hamburg and Bonn have similar numbers. France has at least 20 research groups on cold atoms, 1 on trapped ions and a handful on superconducting qubits. Similar numbers hold for Italy. 

## Qubits based on Rydberg atoms

- **Use case**: The same as trapped ions and superconducting qubits
- **Companies**: Pasqal, Quera, Atom Computing, ColdQuanta, planqc
- **Research Groups**: Paris, Harvard, Caltech, Munich, Heidelberg, … 

The situation, which is closest to superconducting qubit systems are Rydberg quantum simulators. In these systems the atoms are confined in optical tweezer and strongly interact when they are excited into Rydberg states , as such implementing interacting qubit systems. They share many of features, which are similar to ions and superconducting qubits. The Hamiltonian, which is implemented in these systems, is a complex Ising type model:

$H=\sum_i\hat{\sigma}_{x,i}+\sum_iU_{ij}\hat{n}_i\hat{n}_j $, with $\hat{\sigma}_{x,i}=| r⟩⟨g​|_i+| g⟩⟨r​|_i$ and $\hat{n}_i=|r⟩⟨r​|_i$.

They are currently, well established candidates for the quantum simulation of maximum-independent set problems, which already let to the foundation of the start-ups [Pasqal](https://pasqal.io/), [Quera](https://www.quera.com/), [Atom Computing](https://atom-computing.com/), [ColdQuanta](https://coldquanta.com/) or [planqc](https://www.planqc.eu/).

## Itinerant particles built from cold atoms

- **Use case**: Condensed matter, chemistry
- **Research Groups**: Munich, Heidelberg, Zurich, Harvard, … 
- **Representable as circuit**: Yes

The most widely used configuration of cold atoms are moving atoms in some external optical potential. The atomic clouds are typically trapped by focused laser beams, which can be shaped in a flexible fashion. As such a wide variety of systems exists:

- Traps with hundreds of thousands of atoms, which emulate superfluid behavior and Bose-Einstein condensation.
- Traps with hundreds of atoms for the study of continuous variables and large-scale entanglement.
- Optical lattices from the interference of laser beams are now widely used for the study of lattice models in condensed matter with system sizes well above the 100 sites and atoms.

Additionally, the quantum statistics can be tuned widely:

- Working with fermionic or bosonic isotopes the atoms can directly emulate fermionic or bosonic problems.
- If a large number of bosons are condensed into a single spatial mode they can form large collective spins, i.e. continuous variables, from their internal degrees of freedom.
- The connection between moving particles and spin degrees leads to a variety of exotic behaviors like topological band structures, if needed.

The particles are interacting in various ways:

- Most Alkali based system are described through a simple contact interaction.
- Alkaline-earth atoms and Rydberg systems have long range interactions.

The readout of the system can be performed in various fashion:

- Spatially resolved fluorescence imaging provides a destructive, state-sensitive readout. 
- Depending on the measurement protocol momentum or position can be measured.
- [Dispersive measurements allow for weak measurement protocols.

If the external potential is an optical lattice they provide a synthetic realization of strongly correlated lattice models as visualized in Figure 2.

Nowadays, the systems are used for the study of quantum dynamics with quench protocols very similar to quantum computation systems as visualized on the right-hand side of the figure. Those experiments realize the Hubbard model:

$H= -J\sum_i(\hat{c}_{i+1}^\dagger \hat{c}_i+h.c.) +\frac{U}{2}\sum_i \hat{n}_i(\hat{n}_i-1)$

As such they have been widely employed for the study of many-body problems, which come originally from condensed matter. In the early stages this was used to study ground state properties of complex systems like unitary fermions or strongly correlated lattice systems. Importantly, experiments have gone well into the regime of non-perturbative theories. They are therefore well-established benchmarks for sophisticated numerical techniques, which would be otherwise uncontrolled.

Currently, this kind of quench experiments have to be completely programmed at the hardware level. However, with [qiskit-cold-atoms](https://qiskit-extensions.github.io/qiskit-cold-atom/tutorials/03_fermionic_tweezer_hardware.html) it is now possible to emulate such problems and a hardware integration seems only like a question of time.

## Application to quantum chemistry

As IBM already demonstrated beautifully in previous experiments, molecular systems are made for the study of NISQ devices. However, the translation of the fermionic electrons on Qubits currently involves complex transformations like the Jordan-Wigner transformation. These can lead to substantial overhead and substantially increase the required circuit depth. Using fermionic atoms in microtraps, we directly emulate the chemistry problem onto the hardware.

In these systems the molecule is translated into its orbital basis. Each orbit is then represented by the occupation of a fermion of an optical tweezer. These fermionic systems are described by a hopping term HJand a non-commuting interaction term HU. As such they become a potential resource for variational algorithms, which again would heavily benefit from an integration.

These systems are also excellent candidates for the quantum simulation of chemistry problems as they naturally realize interacting fermions on different spatial orbits.

Mixed integer problems in atomic mixtures

Use cases: High-energy physics. Power plant optimization

Research Groups: MIT, Heidelberg, Karlsruhe, Harvard, JILA 

Atomic mixtures are an extension to cold atoms as the provide the ability to let two independent atomic species interact. As such they are an ideal platform to study complex problems, which are defined on complex computational sectors as we describe for lattice gauge theories. 

In the fundamental laws of physics, gauge fields mediate the interaction between charged particles. An example is quantum electrodynamics—the theory of electrons interacting with the electromagnetic field—based on U(1) gauge symmetry. Solving such gauge theories is in general a hard problem for classical computational techniques. While quantum computers suggest a way forward, it is difficult to build large-scale digital quantum devices required for complex simulations. In cold atoms, we work on a fully scalable analog quantum simulator of a U(1) gauge theory in one spatial dimension. Some experiments demonstrated the experimental realization of the elementary building block as a key step towards a platform for large-scale quantum simulations of continuous gauge theories.

In the experiments one atomic species emulates the gauge fields described by the Hamiltonian $H_g$ and the other species the matter field with Hamiltonian $H_m$, interacting through a coupling Hamiltonian $H_{mg}$. In the typical experiments the gauge field is tuned through an x-rotation and then the system is left to evolve under the full Hamiltonian $H=H_g+H_m+H_{mg}$ :

$H= \chi \sum_ i\hat{L}_{z,i}^2+M\sum_i (-1)^i\hat{n}_i+J\sum_i(\hat{c}_{i+1}^\dagger\hat{L}_{+,i}\hat{c}_i+h.c. )$

These Hamiltonian are extremely demanding computationally as the gauge field is defined on the Hilbert space of a [continuous variable](qhw2) $L$ and the matter field on the Hilbert space of itinerant fermions. As such it presents a physical example of a NP-hard mixed-integer problem.

Again, this kind of experiments have to be completely programmed at the hardware level. Quite importantly, this translation currently requires a good knowledge of the hardware from all participants, even high-energy physicists. This makes the experiments currently extremely cumbersome to translate from atomic physics to high-energy physics and back. As such they are one of the interesting use cases that drove the development of [qiskit-cold-atoms](https://github.com/Qiskit-Extensions/qiskit-cold-atom).

## Machine learning and power plant optimization

Machine learning algorithms heavily draw on similar problems like chemistry as they attempt to optimize energy functionals. However, in those problems some of the variables are typically [continuous variables](qhw2) and some [binary](qhw1). These mixed-integer optimization problems are NP hard to solve on classical hardware. The continuous variables on the other hand make them extremely resource intensive for qubit-based systems. Cold atoms show a way forward to employ continuous variables and qubits directly into the system and employ a variational algorithm on them. Similar problems arise for power plant optimizations, when the power plant can give certain power outputs above a certain threshold. Both topics are under active investigation, but currently suffer from the lack of an intermediate programming layer between the users and the hardware developers.

## Summary

This is the last lesson of this course. You learned:

- That cold atoms have become one of the leading quantum simulation platforms.
- Rydberg atoms can implement qubit systems, which are similar to trapped ions of superconducting qubits.
- Cold atoms can easily tackle complex problems with itinerant particles.