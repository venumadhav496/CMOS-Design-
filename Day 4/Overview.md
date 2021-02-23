# Day4 : CMOS Noise Margin robustness evaluation

# Overview
The glitches and cross talk are typically observed in lower technology node, These can be avaoided using noise margin.

This defines the robustness of CMOS Inverter which is immune to noise depending on the noise margin, There are nmH and nmL. The input and the output voltages if they are not in the margin then the input or output is charecterized by undefined, it might be a 0 or 1. In order for the inverter to detect a 1, it should be within the nmH, for the inverter to detect a 0, it should be within nmL. We looked at varying the width of PMOS to see how that effects the noise margin.

As the noise margin reduces the device is more prone to noise. As the delay decreases the performance will be improved.

At vdd/2 we can see that it will switch from logic 1 to 0, Ideally the slope would be infinite, we can look at the almost practical case and pure practical case and will get a better understanding of Noise margin. 

When the Input is between Voh and Vih then the input will be considered as 1 i.e. NMH= Voh-Vih. This is also used in digital circuit as logic 1
When the input is between Vol and Vil then the input will be considered as 0 i.e. NML= Vil-Vol. This is also used in digital circuit as Logic 0

Wider Noise margin is better to avoid any power supply fluctuations.

If the values are between NMH and NML then the values are undefined, it can be 1 or 0, Astable state. This is used in analog design as it is close to infinite gain.

The slope at which Voh is considered is -1.

# Simualtion 

1. We will be varying the width of PMOS to see the Noise margin and how the values are effected.
Wn= 0.36u and Wp is varied from 0.42 to 1.68 and we will simulate the NMH and NML for these values.

# Observation 

1. Even with the change in the width of PMOS, the Noise margin is increased first but is not much effected with the increase in the width of PMOS further.
