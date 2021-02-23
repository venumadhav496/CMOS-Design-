# Day5 : CMOS power supply and device variation robustness evaluation

In this we will look at all the power supply scaling, spice modeling for thhe cmos inverter from strong PMOS weak NMOS to Strong NMOS and Weak PMOS. The device fabrication and 
characteristics which will effect the VTC curve.

We will look at the spice file for automatically simulating the gain values when the CMOS is used at 2.5v and CMOS used at 0.5V. The gain can be calculated with Vout/Vin. 

Here we will look into the advantages and disadvantages of using teh CMOS device at a low power supply.

# Advantages of using CMOS at lower power supply

1. Gain increased to 50%, from the energy equation i.e. 1/2 cv^2 we can see that when there is reduction in voltage then there is reduction in energy lost so we have very high gain and less energy is lost.

# Disadvanatges 

1. When we reudce the supply voltage you are not giving enough time to charge and discharge the capacitor, this is effecting the rise time and fall time of the circuit. When the supply volatge is really small the device is nto able to charge or discharge the capacitor load. This will impact the performance.

# Sources of variations in a CMOS Inverter 

1. Etching Process
2. Oxide Thickness 

# Etching: 
Here we observed the layout of a typical CMOS inverter, the actual W/L and the fabricated W/L are very much different and this will effect the W/L and there wil be distortion. This will indirectly effect the delay of the inverter. 

Mutiple gate circuits are shown for reference, the circuit in the middel are not as much prone to these errors, but the circuit in the ends are much prone to thse errors.

# Oxide thickness: 
This is related to the gate oxide thickness, in general the gate oxide layer is constant thought the whole cell, but the oxide thickness will vary from one inverter to anaother i a set of inverters, The Cox in the Id equation will be effected, So Id might be effected.

# Simulations 

In Ngpsice we will simualate the VTC from strong PMOS weak NMMOS to Strong MOS and weak PMOS, The Wp and Wn are varied in order to observe the VTC and see how by varying the width we can vary the VTC curve towards left or right.

The switching thresholds are observed for various wp and wl.

# Observations

1. For strong NMOS and weak PMOS, the vTC curve shifts left, for Strong PMOS and weak NMOs the VTC curve further shifts right.
2. CMOS is a robust device and the device characteristics stays pretty much the same.

