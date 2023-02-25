# RoundRobinArbiter
RR-Arbiter: Verilog implementation of a fair, rotating grant selector for multiple request sources. Allows equal access to shared resource.

Arbiter
This is a verilog code for a 4-requests arbitrer, which selects one of the four requesters at a time, and grants it access to a shared resource.

How it Works
The arbiter has four request inputs: req3, req2, req1, req0, and four grant outputs: gnt3, gnt2, gnt1, gnt0. The arbiter selects one request input to grant access based on a priority encoding scheme.

The output signals are determined by a combinational logic circuit. The circuitry takes into account the status of the requests, and latches the selected grant.

![image](https://user-images.githubusercontent.com/79183768/221335940-6cb65576-a6d5-40ee-bed3-c781bab13523.png)

Inputs and Outputs
Inputs
clk: The system clock signal.
rst: The reset signal, used to reset the arbiter.
req3: The request signal from the highest priority requester.
req2: The request signal from the second highest priority requester.
req1: The request signal from the third highest priority requester.
req0: The request signal from the lowest priority requester.
Outputs
gnt3: The grant signal for the highest priority requester.
gnt2: The grant signal for the second highest priority requester.
gnt1: The grant signal for the third highest priority requester.
gnt0: The grant signal for the lowest priority requester.

![image](https://user-images.githubusercontent.com/79183768/221336289-a441bc13-d170-421e-9cc1-7011377a0a60.png)

File Structure
arbiter.v: The verilog source file.
top.v: A top-level verilog module that instantiates the arbiter module.
Makefile: A makefile for building the design.
How to Use
Clone the repository
Use the Makefile to build the design: make
Run the simulation: ./sim
The simulation outputs the request and grant signals for the arbiter.
Acknowledgements
This code was written by [Your Name] as part of a verilog tutorial. It is based on the classic 4-requests arbitrer design.












