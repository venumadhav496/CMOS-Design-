We Simulated the spice model of the NMOS circuit and we observed the Id vs Vds characteristics when we vary Vgs. We can look at the spice setup in order to obtain the Id vs Vds Characteritsics below 

# code
![lab 1 code](https://user-images.githubusercontent.com/78948002/108807677-99aa7380-756a-11eb-946c-56dc389e6ecc.png)

Here . param will include the parameter in the spice file. In a spice file you will have a netlist which will descibe the connection of components, you will have a library file and you have simulations commands based on a dc analysis and transient analysis.

# Netlist generation 

For a Nmos the netlist would consist of gate resistor, a mosfet and voltage supplies, In the nelist we need to look at nodes and based on the nodes we would write a netlist for the device
M1 vdd n1 0 0 sky130_fd_pr_nfet_01v8 w=0.65 L=0.25 [ Mosfet name drain gate sorce and substrate]
M1 would be the code for general mosfet description
vdd n1 0 0 would be the nodes in between where the nmos is connected ( vdd is the terminal connected to drain, n1 would be connected to gate, 0 would be connected to source and 0 is connected to substrate/bulk)

# Types of Corners in CMOS Design.

When we try to build the actual circuit desin on a real chip, due to manufacturing there will be variations, these can also be reffered to as on chip variations, we would like to simulate the worst case scenarios so that we can simulate the best possible result. There are 3 categories where we would simulate the nmos characteristics in NGSpice
1. TT (Typical Corner)
2. SS ( Slow Slow corner)
3. FF ( fast fast corner)

More details are explained in this 
https://personal.utdallas.edu/~zhoud/EE%207v88/lect%209/Design%20Automation%20of%20Analog%20VLSI%20Lect9.pdf

# Things I learnt from Day1 
1. threshold voltage can be given by 
  ![image](https://user-images.githubusercontent.com/78948002/108152748-58fcb700-709f-11eb-834f-e71cf37d7a5b.png)  
3. For strong inversion in a Nmos the Vgs should be positive i.e. when the gate voltage is increased then the depletion region increases and an strong inversion occurs
4. the delay in the circuit will be different for same skew rate.
5. From the spice simualtions we can obtain the delay of the circuit and PMOS and NMOS device characteristics 
6. There are two types of mosfet based on channel length i.e. long channel and short channel. Short channel mosfet are generally reffered if the channel length will be below 25u, If the channel length is greater than 25u then it can be reffered to as long channel. 
7. There are different types of corner i.e. typical corner, slow slow, fast fast, fast slow and slow fast corner. The represenation is based on PMOS and NMOS, it displays the speed of NMOS and PMOS.
8. The W/L generally used for nmos is 2.5, we also looked at the Id vs Vds characteristics by varying Vgs.

# Observations 

We looked at the the drain current in TT, FF and SS corner and observed that that for Vgs= 1.4v, Vds= 1V, W=0.65 and L=0.25 then Id would be more in FF corner around 155uA, second would be TT corner around 121uA, and the third would be SS conrner where Id would be around 86uA. The chnage in Id is due to the configuration of NMOS. Based on the speed of the mosfet the Id would be varying, Id will also be dependent on W/L. A list of simulations were done in order to undertand the Ngspice setup and Id would be decreasing with the decrease in channel length.


