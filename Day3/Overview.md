# Day3 : CMOS Switching threshold and dynamic simulations

Here in this we will look the W/L ratio of PMOS and NMOS, the applications where the W/L should be same for both and W/L of PMOS should be 2 or 3 times of NMOS. 
We will understand how to write a netlist for PMOS and NMOS, we will simulate the output waveforms when (W/L)p= (W/L)n and the 2nd case as well and we can observe that the when the W/L is the different. The inversion occurs exactly at the middle when PMOS to be twice as of NMOS, but if we have same W/L then we can see that the VTC curve is shifted to the left.
We look at the switching threshold value at which vout and Vin are equal. Switching threshold occurs when PMOS and NNMOS are in saturation region. The rise and fall delay are also observed and simulated in Ngspice. By changing the W/L of PMos and NMOS we can vary the switching threshold, Rise delay and fall delay 

There are two types of analysis
1. DC analysis 
2. Transient Analysis

Dc analysis is required in order to obtain VTC characteristcs and transient analysis is required to obtain the rise and fall delay. 

We can see that when (W/L)p = 2* (W/L)n, then the VTC is exactly at the middle, this can be best used in buffer circuits.

# VTC characteristics 
In the VTC curve, the point where the inversion happens, is a very criitical area, The CMOS has 5 regions operation,, out of them three main important ones are PMOS on NMOS off
PMOS and NMOS on, and NMOS on PMOS off. Switching threshold is at a point where Vout will be equal to Vin, this is also a point where both the PMOS and NMOS are on and they are in saturation region. This is the point where the Vdd is connected directly to ground and the device will have power dissipation and a lot of leakage current.

# Advantages of CMOS

1. The switching threshlold would not vary much even when it is based on PMOS and NMOS size, Due to the W/L of PMOS 2* that of NMOS we can actually see the exact clock waveform.
2. The bigger W/L are used in complex blocks where it depends on rise time and fall time requirements 

# Lab simualtion 

In this lab we will be varying the W/L of NMOS to a higher value and we will observe the rise and fall delay of the inverter and the switching threshold voltage i.e. vm. We observe that the rise time and fall time is almost equal when Pmos W/L is 2* W/L of NMOS.When the W/L of PMOS becomes 3 times or increases further then the VTC curve would shift to the right. The switching threshold voltage also increases when we increase the W/L of Nmos.

1. For Wp=0.36 and Wn= 0.84 and Lp=Ln= 0.15 we will observe the effect of switching threshold voltage in TT and SS cases 
2. We will keep the L of PMOS and NMOS constant and we will vary the length of PMOS and observe the rise delay, fall delay and Switching threshold Volatge.

# observations:

1. The switching threshold did not change much which explains the robusteness of the CMOS devcie.
2. The (W/L)p= 2* (w/L)n then we can see that the rise time is almost equal to fall time which makes the best use of CMOS inverter as a buffer.
3. When we increase the width of PMOS we can see that the VTC curve will be shifting to the right.
