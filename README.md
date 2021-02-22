# CMOS-Design

# Difference between Circuit Design and Spice 
  A basic difference between a circuit design and a spice simualtion would be, the circuit design would consist of logic gates and inverter blocks made up of pmos and nmos, and the Psice simulation would be a simulation tool which would involve simualting the circuits and verifying the output waveforms when an input waveform is provided. 

# Purpose of Spice tool 
The basic purpose of any simuation would be to have a better understanding of the circuit behaviour, how the circuit will produce an output with any change in the input waveforms. Let us look at an example in which, In order to change the delay for a cmos inverter we need to adjust the W/L of PMOS and NMOS, this W/L will effect the current flow i.e. Ids in the circuit, this will eventually decide the delay of the inverter circuit, so in order to adjust the delay we need to work on the W/L ratio and for this we need Spice Simulations.  

# Circuit Basic Element: NMOS & PMOS
Mos stands for metal oxide semi conductor, and there are of two types one would a P-channel Mosfet and the other one would be an N-channel Mosfet. In P-channel the majority charge carriers are holes but in NMOS the majority carrier are electrons. We can look at the working of an NMOS and an inversed version would be a PMOS. Mosfet generally has 4 terminals i.e. gate, source, drain and bulk. Normally bulk is usually ignored but any change in the bulk potential will impact the threshold voltage. So therefore in Nmos the Bulk voltage is connected to ground, and Pmos the bulk terminal is connected to VDD. 
<img width="429" alt="PMOS and NMOS Device" src="https://user-images.githubusercontent.com/78948002/108134473-e4645100-707b-11eb-9482-ac66136a9c88.PNG">

# Working of a NMOS Transistor 
As there are three terminals in a mosfet, when no volatge is applied to all the terminals i.e. when gate source ad drain are gounded then there is huge resitance between drain and source stopping the current flow. Now when we supply a postive voltage to the gate there will be negative charge being build up below the gate, this region is also reffered as depletion region or strong inversion layer which is similar to PN junction diode. When a postive voltage is applied at the gate the Sio2 layer acts a dielectric medium and forms a capacitor circuit and now due to this all the postive p type are repelled from the surface leaving behind the n type holes, Due to this depletion region is formed. As we increase the gate voltage there are two widths that needs to be taken into consideration. 
1. Depletion width 
2. Channel width 

When we increase the gate voltage then depletion width increases, we increase it to a point where there is no further postive ions to repell, so thats when we have a complete n type layer under the gate with almost zero p type ions left, this is also refereed as strong inversion. The gate voltage at which this strong inversion occurs is called as threshold voltage. When Vgs= Vth the channel is formed, the resistance is minimum which allows the current to pass from source to drain. 

# Importance of Bulk Voltage
There are two scenarios that needs to be taken into consideration when we look at bulk voltage,i.e.
1. Vsb= 0 
2. Vsb = +ve 

the following oberservations have been made from the two diagrams i.e. the depletion width when Vsb=0 is much smaller than Vsb= +ve. This is due to the additional reverse bias voltage on top of the gate voltage, this reverse bias causes the depletion region to increase in the latter case. The inversion layer is a bit delayed in the case of Vsb= +ve. The most important one would be due to a different bias to source voltage there is an increase in the gate to source voltage or threshold volatge. 

In PMOS the bulk is connected to the power supply and in NMOS the bulk terminal is connected to ground. 

# Things I learnt from Day1 
1. threshold voltage can be given by 
  ![image](https://user-images.githubusercontent.com/78948002/108152748-58fcb700-709f-11eb-834f-e71cf37d7a5b.png)  
3. For strong inversion in a Nmos the Vgs should be positive i.e. when the gate voltage is increased then the depletion region increases and an strong inversion occurs
4. the delay in the circuit will be different for same skew rate.
5. From the spice simualtions we can obtain the delay of the circuit and PMOS and NMOS device characteristics 
6. There are two types of mosfet based on channel length i.e. long channel and short channel. Short channel mosfet are generally reffered if the channel length will be below 25u, If the channel length is greater than 25u then it can be reffered to as long channel. 

# Types of operation region in NMOS 

There are three operating regions in a NMOS transistor i.e.

1> Cut off Region  (vgs<vt)
2> Resistive region (vds<vgs-vt)
3> Saturation Region (vds>vgs-vt)

The drain current can be represented by 


# References
1. https://allthingsvlsi.wordpress.com/2013/04/04/nmos-and-pmos-operating-regions/
