
2026-01-05 17:59

Status: 

Tags:

# 05 - 4He Cryostats
![[Pasted image 20260105204103.png]]
In this cryostats design, low temperature are obtained by evaporating liquid helium $^4$He. 
The main issues are:
- the isolation of cold parts from warm parts is done using vacuum, so the cryotechnlogy always depends on good vacuum technology(soldering techniques, leak detection, welding, gluing, etc)
- there's an extreme mechanical stress due to the large thermal gradients and different thermal expansion coefficients of materials
- it's built and tested at room temperature, but it has to work at low temperature
- containers filled with cryogenic liquids have to handle high pressure due to evaporation of the liquid, and they must have the right safety features to avoid accidents
- safety regulations enforced by law must be followed
##### Usage of liquid $^4$He
Liquid helium-4 is used in almost every refrigeration system that reaches temperatures below 10K either for cooling or precooling. But, since it's very expensive, we need to minimize its consumption.
**Cool Down Phase:** the heat of vaporization of $^4$He transforming liquid to gas is about 2.6 kJ/L at 4.2 K, but if we utilize the enthalpy of the gas from 4.2 K to room temperature, we can recover about 200 kJ/L of liquid helium. For example is 1 W is applied continuously during the cool down phase, 1.41 L/h of liquid helium is needed without recovery, but only 0.017 L/h is needed with recovery.
So it's very important to use the enthalpy of the cooled helium gas after the liquid helium has has evaporated when cooling down the system. The gas should leave the cryostat at room temperature to maximize the enthalpy recovery.
In addition, if we precool with nitrogen from room temperature to 77 K, we can save about 70 kJ/L of liquid helium, since liquid nitrogen has about 60 times the latent heat of vaporization of liquid helium and it's much cheaper.
**Running Phase of the Experiment:** when the equipment is at the required low temperature, to maintain the temperature even when there are heat transfers from the environment, the cooling power is provided by the evaporation of liquid helium. 
![[Pasted image 20260105205715.png]]

##### Double Walled Glass Dewars
![[Pasted image 20260105211536.png]]
The main advantages of glass dewars are:
- low costs
- low thermal conductivity of glass
- transparent to see the liquid level
The main disadvantages are:
- fragile, the glass can break easily due to small leaks to the vacuum space. Air may enter and condensate on the cold surfaces, on warming the system the condensed air will evaporate, and if it cannot escape fast enough, the pressure will rise and the glass may shatter.

At room temperature helium diffuses through the glass walls, so the vacuum space must be periodically pumped with helium gas from the inner volume after warming up the dewar to maintain good vacuum insulation.
Normally we use nitrogen to precool the system, before inserting liquid helium we need to make sure to remove all nitrogen from the inner volume, otherwise since it has a rather large specific heat capacity, it would take much more liquid helium to cool down the system.
##### Metal Dewars
![[Pasted image 20260105211822.png]]
Metal dewars are more robust than glass dewars, they can withstand higher pressures and mechanical shocks. They can also be manufactured in more complex shapes to accommodate different experimental setups. It obviously doesn't have the diffusion problem of glass dewars.
One of the main disadvantages is the price, since its made of stainless steel or aluminum, and also it doesn't have two vacuum spaces like glass dewars, so the thermal insulation is not as good.
Nowadays most cryostats don't use liquid nitrogen for precooling, since they cause vibrations during the constant boiling of nitrogen, which can be detrimental for sensitive experiments, so in this case a superinsulation layer is used.
Superinsulation is a thin plastic film coated with a reflective material like aluminum (through evaporation) to give an emissivity of about 0.06. Multiple layers of this film are wrapped around the liquid Helium vessel to act as radiation shields, reducing radiative heat transfer from the outer ones to the inner ones.
For further insulation, a metallic radiation shield is often placed between the outer wall and the helium vessel, which is cooled by the evaporated helium gas before it exits the cryostat. 
A good helium dewar design should have an evaporation rate of less than 0.1 L/h.
##### He gas-flow Cryostats
![[Pasted image 20260105213218.png]]
For measurements at $T> 4.2K$, it is inefficient to use liquid helium baths, since the evaporation rate would be too high. In this case we can use a helium gas-flow cryostat evaporating liquid helium to cool helium gas, and take advantage of the enthalpy of the cold gas to cool down the sample space. In this way the storage vessel of liquid helium is separated from the sample space, and we can control the temperature of the sample space by adjusting the helium gas flow rate, this is done using a needle valve.
The advantages of this design are:
- lower helium consumption
- temperature range variable from 4.2 K to 300 K
- the apparatus can be cooled down and warmed up faster

##### Dipper Probes
![[Pasted image 20260105213622.png]]
Again, for measurements at $T> 4.2K$, we can use a dipper probe, which is a simpler and cheaper solution than a full cryostat. It consists of a long tube that can be dipped into a liquid helium dewar, with a small chamber at the bottom where the sample is placed. 
It has a variable temperature insert that allows us to control the temperature of the sample chamber by adjusting the helium gas flow rate. 
Basically by varying the height of the probe above the liquid helium level, the temperature of the sample chamber can be adjusted due to the temperature stratification that occurs naturally in the vapor space above the liquid helium, from 4.2 K at the liquid surface to room temperature at the top of the dewar.
The temperature gradient is normally really long so it can be calibrated easily, by carefully moving up and down the insert we can set the desired temperature.
This system uses the enthalpy of the helium gas to cool down the insert and therefore the helium consumption is really low. It's one of the simplest and most cost-effective cryostat designs for experiments that require temperatures above 4.2 K.
One other advantage is that it can be easily inserted into a storage dewar without the need for complex vacuum seals or insulation.
##### Cryostats with Variable Temperatures for $1.3K < T < 4.2K$
![[Pasted image 20260105214306.png]]


## References
