
2025-12-30 10:33

Status: 

Tags:

# Thermodynamics Basis
The aim of classical thermodynamics is to describe the macroscopic, so portion of matter physically separated from its surroundings by boundaries, called a system. In particular, it wants to describe the transformation it undergoes when it exchanges energy and matter with other systems or the external environment.
A macroscopic description means that we specify the fundamental and measurable properties of the system, called thermodynamic properties, without considering the microscopic details of the system, such as the position and velocity of each particle that composes it.
The state of a macroscopic system at equilibrium is completely specified by a set of thermodynamic properties called state variables, such as pressure, volume, temperature, and composition. These properties or coordinates are interrelated by equations of state that express the constraints imposed by the laws of thermodynamics(time is not a state variable in classical thermodynamics).
##### Thermodynamic Systems
By analyzing the way of exchanging energy and matter with the surroundings, we can classify thermodynamic systems into three categories:
1. Isolated systems: they do not exchange heat, matter, or work with the surroundings.
2. Closed systems: they can exchange energy (heat and work) but not matter with the surroundings. When a system exchanges heat, work or both with the surroundings, it can be classified by the properties of the boundaries that separate it from the surroundings:
	 - Adiabatic system: it does not exchange heat with the surroundings.
	 - Diathermic system: it can exchange heat with the surroundings.
	 - Rigid system: it does not exchange work with the surroundings.
	 - Non-rigid system: it can exchange work with the surroundings.
3. Open systems: they can exchange both energy (heat and work) and matter with the surroundings. A boundary that allows the exchange of matter is called permeable; otherwise, it is called impermeable.
##### Thermodynamic Transformations
A thermodynamic transformation is the process by which a system changes from one equilibrium state to another. During a transformation, the system may exchange energy and matter with the surroundings. We can classify thermodynamic transformations into two categories:
1. Reversible transformations: the process is performed in such a way that the system and surroundings can be restored to their initial states without any net change in the universe. Reversible transformations are idealized processes that occur infinitely slowly, allowing the system to remain in equilibrium throughout the transformation.
2. Irreversible transformations: the process cannot be reversed without leaving a net change in the universe. Irreversible transformations occur spontaneously and involve dissipative effects, such as friction, unrestrained expansion, mixing of different substances, and heat transfer across a finite temperature difference.
#### The Laws of Thermodynamics
One can distinguish three fundamental laws of thermodynamics that govern the behavior of thermodynamic systems, plus the zeroth law, which establishes the concept of temperature.
##### Zeroth Law of Thermodynamics
We start by defining what the equilibrium state is and what thermal equilibrium between two systems means: 
- Equilibrium state: a system is in an equilibrium state when its coordinates (thermodynamic properties) remain constant as long as the external conditions do not change.
- Thermal equilibrium: two systems are in thermal equilibrium when they are in contact through a diathermic boundary and no heat exchange occurs between them. It is characterized by restricted values of their coordinates(instead, two system separated by and adiabatic boundary can have any values of their coordinates, since they do not exchange heat).

The zeroth law of thermodynamics states that if two systems are each in thermal equilibrium with a third system, then they are in thermal equilibrium with each other. This law establishes the basis for the concept of temperature and the use of thermometers to measure it. 
So we can define temperature as the property that determines whether two systems are in thermal equilibrium when they are in contact through a diathermic boundary.
This laws explains the fact that two bodies in thermal contact reach the same temperature after some time. In the kinetic formulation of thermodynamics, the zeroth law explains the tendency to reach the same average kinetic energy of the particles of the bodies between which heat exchange occurs, resulting in the same temperature(temperature is proportional to the average kinetic energy of the particles of a system).
The efficiency of the energy exchange between two systems determines the specific heats of the materials composing them.

Heat is defined as a form of energy that can be converted into mechanical work and stored in the form of internal energy, but it is not a material substance. Heat is transferred between systems due to a temperature difference, flowing from the system at higher temperature to the system at lower temperature until thermal equilibrium is reached.

**Work:** work is defined as the energy transfer that occurs when a force is applied to a system, causing it to move or change its configuration. Work can be done on or by a system, and it is a way of transferring energy between systems.
**Heat:** heat is defined as the energy transfer that occurs due to a temperature difference between two systems. 

It is experimentally proven that heat and work have a correspondence: each calorie of heat equals 4.186 joules of work.
##### First Law of Thermodynamics
The first law of thermodynamics, also known as the law of energy conservation, states that energy cannot be created or destroyed in an isolated system. There can be no machine that produces work without consuming an equivalent amount of energy from another source, if it existed it would produce perpetual motion of the first kind.
Mathematically, the first law can be expressed as:
$$\Delta U = Q - W$$
where:
- $\Delta U$ is the change in internal energy of the system, which is the sum of the kinetic and interaction energies of the particles that compose the system,
- Q is the heat exchanged between the system and the surroundings, positive when supplied to the system,
- W is the work done by the system, positive when done by the system.
- the minus sign before W indicates that when the system does work on the surroundings, it loses energy.
##### Second Law of Thermodynamics
The second law of thermodynamics states that there are limitations on the conversion of heat into work. There are two main formulations of the second law:
1. Kelvin-Planck statement: it is impossible to construct a heat engine that operates in a cycle and converts all the heat absorbed from a high-temperature reservoir into work without any other effect on the surroundings. In other words, no heat engine can have 100% efficiency. 
2. Clausius statement: it is impossible to construct a refrigerator that operates in a cycle and transfers heat from a low-temperature reservoir to a high-temperature reservoir without any external work input. In other words, heat cannot spontaneously flow from a colder body to a hotter body.

They basically mean that every time we convert heat into work, some energy is lost to the surroundings as waste heat, which cannot be used to perform useful work. This waste heat increases the entropy of the surroundings, which is a measure of the disorder or randomness of a system.
##### Third Law of Thermodynamics
The third law of thermodynamics states that as the temperature of a system approaches absolute zero (0 Kelvin or -273.15 degrees Celsius), the entropy of a perfect crystalline substance approaches zero. In other words, it is impossible to reach absolute zero through any finite number of processes.
#### Entropy
Entropy is introduced with the second law of thermodynamics as a state function that quantifies the irreversibility of natural processes and the degree of disorder or randomness in a system. In the International System of Units (SI), entropy is measured in joules per kelvin (J/K).
It was observed that transformations occurred in one direction only, for example, heat flows spontaneously from a hotter body to a colder body, but not the other way around, that is the direction of maximum disorder.
So time acquires a direction, called the arrow of time, because natural processes tend to move towards a state of greater disorder or randomness.
Obviously, disorder, so entropy are concepts relative to a reference state, for example vapor has more entropy than liquid water at the same temperature and pressure, but both have more entropy than ice.
Isolated systems or systems plus surroundings experiencing irreversible processes tend to increase their total entropy over time, reaching a maximum value at equilibrium.
##### Thermodynamic Definition of Entropy
The thermodynamic definition of entropy change for a reversible process is given by the equation:
$$dS = \frac{\partial Q_{rev}}{T} \equiv \Delta S = \int_{rev} \frac{\partial Q}{T}$$
where:
- dS is the infinitesimal change in entropy,
- $\partial Q_{rev}$ is the infinitesimal amount of heat exchanged in a reversible process, it is not an exact differential,
- T is the absolute temperature at which the heat exchange occurs.

**Note:** exact differentials are those that depend only on the initial and final states of a system, while inexact differentials depend on the path taken between the two states. For example, dS is an exact differential only if the second law of thermodynamics is satisfied, while $\partial Q$ is an inexact differential because the heat exchanged depends on the specific process undergone by the system, but dividing it by T makes it an exact differential.
##### Increase in Entropy
The second law of thermodynamics can be expressed in terms of entropy as follows:
$$\Delta S_{universe} \geq 0$$
where:
- $\Delta S_{universe}$ is the total change in entropy of the universe, which is the sum of the changes in entropy of the system and its surroundings.
- the $>$ sign applies to irreversible processes, while the $=$ sign applies to reversible processes.
This means that in any natural process, the total entropy of the universe either increases (for irreversible processes) or remains constant (for reversible processes). 
So it not only implies that energy cannot be created or destroyed (first law), but neither that it can be converted entirely from one form to another without losses (second law) in the form of heat.
##### Mathematical Description
The mathematical description treats entropy as a state function of temperature. As a continuous and monotonic increasing function of temperature, admitting absolute minimum and maximum values, according to Weierstrass theorem, to which the universe converges continuously.
##### Entropy and the Universe
The concept of entropy has profound implications for the fate of the universe. According to the first and second laws of thermodynamics, the total energy of the universe remains constant, but the total entropy of the universe tends to increase over time. The initial state of the universe was one of low entropy, since entropy doesn't depends on or gives information about the path taken to reach a certain state we can't calculate a final entropy state but we can infer that the universe will eventually reach a state of maximum entropy. This state is often referred to as the "heat death" of the universe, where all energy is evenly distributed, and no useful work can be extracted from any system. In this scenario, all processes that increase entropy will have ceased, and the universe will be in a state of thermodynamic equilibrium, since we have finite mass and energy in the universe but infinite time.
##### Statistical Definition
In statistical mechanics, entropy is the mean to obtain macroscopic properties from microscopic states. A certain macroscopic state can be realized by many different microscopic configurations of the particles that compose the system. The statistical definition of entropy is given by the Boltzmann equation, where microstates are definied in the phase space:
$$S = k_B \ln \Gamma$$
where:
- S is the entropy of the system,
- $k_B$ is the Boltzmann constant, approximately equal to $1.38 \times 10^{-23}$ J/K,
- 



## References
