# CMOS-Design
In this workshop, I have understood the concepts of CMOS inverter device characterstics and the effects of delay in CMOS inverter. I understood the concepts of velocity saturation and also derived the voltage transfer characteristcs using the Id vs Vds graphs of PMOS and NMOS. We used sky130 technology and simulated the circuit files using ngspice software. We also looked to understand the robustness of a CMOS Inverter by switching threshold, Noise margin and power supply variation.

Switching threshold: In the VTC curve where Vout = Vin, i.e. when the gate voltage would be equal to the drain voltage. In order to obtain the switching threshold both the PMOS and NMOS are in saturation region 

Noise Margin: This defines the robustness of CMOS Inverter which is immune to noise depending on the noise margin, There are nmH and nmL. The input and the output voltages if they are not in the margin then the input or output is charecterized by undefined, it might be a 0 or 1. In order for the inverter to detect a 1, it should be within the nmH, for the inverter to detect a 0, it should be within nmL. We looked at varying the width of PMOS to see how that effects the noise margin.

Power supply variations: there are many flucations in the input power supply, we looked at different instances where the inputs are varied and we observed how the CMOS output behaviour was not much effected by the changes in input.

# Overview of workshop
Day1 : Basics of NMOS Drain current (Id) vs Drain-to-source Voltage (Vds)
Day2 : Velocity saturation and basics of CMOS inverter VTC
Day3 : CMOS Switching threshold and dynamic simulations
Day4 : CMOS Noise Margin robustness evaluation
Day5 : CMOS power supply and device variation robustness evaluation

# Important commands used in Linux Terminal

1. Cd: This fucntion is used to change directories, it will list the folders or files in a folder.
2. ls: This is used to obtain the list of files in that particular directory.
3. sky130/designs: this was the folder which would navigate to the spice files and library files in a directory.
4. less: In order to view a file, we used a command called less<filename> in order to view the file.
5. vim <file name>, this command would be used in order to make any edit to the file 
6. in order to edit the spice file, we need use "i" in order to chagne the command mode to insert, then you can edit the file.
7. esc command is used in order to come out of insert mode and we use :q command to exit the present folder. 
8. :wq command is used in order to save the file we have edited.   
9. cd ../ this command is used to go back to a different directory 
10. ngspice <spice file> this command is used in order to simualate a spice file.
11. plot <out vs in >would give us the graphical representation between input and output.


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
7. There are different types of corner i.e. typical corner, slow slow, fast fast, fast slow and slow fast corner. The represenation is based on PMOS and NMOS, it displays the speed of NMOS and PMOS.
8. The W/L generally used for nmos is 2.5, we also looked at the Id vs Vds characteristics by varying Vgs.

# Types of operation region in NMOS 

There are three operating regions in a NMOS transistor i.e.

1> Cut off Region  (vgs<vt)
2> Resistive region (vds<vgs-vt)
3> Saturation Region (vds>vgs-vt)

The drain current can be represented by 


# References
1. https://allthingsvlsi.wordpress.com/2013/04/04/nmos-and-pmos-operating-regions/
