# CMOS-Design

# Difference between Circuit Design and Spice 
  A basic difference between a circuit design and a spice simualtion would be, the circuit design would consist of logic gates and inverter blocks made up of pmos and nmos, and the Psice simulation would be a simulation tool which would involve simualting the circuits and verifying the output waveforms when an input waveform is provided. 

# Purpose of Spice
The basic purpose of any simuation would be to have a better understanding of the circuit behaviour, how the circuit will produce an output with any change in the input waveforms. Let us look at an example in which, In order to change the delay for a cmos inverter we need to adjust the W/L of PMOS and NMOS, this W/L will effect the current flow i.e. Ids in the circuit, this will eventually decide the delay of the inverter circuit, so in order to adjust the delay we need to work on the W/L ratio and for this we need Spice Simulations.  

# Circuit Basic Element: NMOS 
Mos stands for metal oxide semi conductor, and there are of two types one would a P-channel Mosfet and the other one would be an N-channel Mosfet. We can look at the working of an NMOS and an inversed version would be a PMOS. Mosfet generally has 4 terminals i.e. gate, source, drain and bulk. Normally bulk is usually ignored but any change in the bulk potential will impact the threshold voltage. So therefore in Nmos the Bulk voltage is connected to ground, and Pmos the bulk terminal is connected to VDD. 
<img width="429" alt="PMOS and NMOS Device" src="https://user-images.githubusercontent.com/78948002/108134473-e4645100-707b-11eb-9482-ac66136a9c88.PNG">







# References
1. https://allthingsvlsi.wordpress.com/2013/04/04/nmos-and-pmos-operating-regions/
