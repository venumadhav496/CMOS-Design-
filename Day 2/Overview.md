# Day2 : Velocity saturation and basics of CMOS inverter VTC

Switching threshold: In the VTC curve where Vout = Vin, i.e. when the gate voltage would be equal to the drain voltage. In order to obtain the switching threshold both the PMOS and NMOS are in saturation region.

Here we look at the difference between long channel and short channel, so when we look at the drain current equation which is directly proportional to W/L, but even if we have the same w/l ratio in short channel and long channel we expect the Id to be constant, but that is not the same, there is change in Id current.

# Observations 

1. Drain current quadratically increases with different value of gate to source voltage for constant Vds
2. Anything of channel length below 0.25u is reffered to a short channel 
3. For short channel drain current will be quadratic for lower values of Vgs, for higher values of Vgs the drain current will be linear this is due to velocity saturation.
4. There are 3 regions of operation in a long channel i.e. linear or resistive, cutoff and saturation, but in short channel there is an extra region called velocity saturation region. Velocity saturation causes the device to saturate after the linear region.
5. As Id is inversly proportional to L, when the Id increases L should be decreased, but when L is decreased Id is also reduced due to velocity saturation.
6. Id equation is modeled in such a way to udpate the saturation (vgs-vt), velocity saturation(Vdsat) and Vds (linear). The minimum voltage out of these three will determine where the short channel mosfet device would operate in.
7. We look at VTC i.e. voltage transfer characteristcs of CMOS in order to understand the delay of the CMOS inverter.
8. Working of MOS as a switch, when a postive volatge is connected to the Nmos gate terminal then the switch is on else it is off, For PMOS to act as a switch we need to supply a stong negative potential at the gate terminal for PMOS to turn on.
9. In CMOS the PMOS and NMOS are connected together, where the gate of the two are tied together,the drain termimal of NMOS and PMOS are connected together, the Bulk of PMOS is connected to VDD, and the bulk of NMOS is connected to ground.  
10. When the MOS is turned on we can replace the MOS with an equivalent resistance between drain and source, This resistance is non linear with Id.
11. When the input will be 0 then PMOS would turn on and NMOS would be off, there is path in between Vdd to Vout, so we get 1v, if the Input is 1v then PMOS is off and NMOS is on, making the connection between ground and vout, so the output will be zero.
12. The output load is considered to be a capactive load and when the logic is 1, i.e. NMOS on and PMOS off the current will be flowing from the charged capactior through the NMOS and ground. If the input is a logic 0 then the PMOS would be On and NMOS off then the current flow will be charging the capacitor. So the current eill from Vdd though PMOS and will pass through the capacitor charging it to the max value.  
13. We will find the VTC curve using the ID vs Vds curve of NMOS and PMOS, we will convert the PMOS axis to match with the NMOS axis and we look for the cross over points to form a relation between Vout and Vin.



