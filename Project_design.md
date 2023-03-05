# Project Design
The voltage level shifter will be designed using a regulated cross-coupled pull up 
network. The design will consist of a cross-coupled pull-up network and a regulated 
pull-up network.

<h3>The overall design idea of the voltage level shifter is shown in the "Design_Code_Idea" file.</h3>
This code defines a module voltage_level_shifter that takes an input signal in and 
outputs a signal out. The voltage level shifter consists of a cross-coupled pull-up 
network and a regulated pull-up network.
The cross-coupled pull-up network is implemented using four nMOS transistors n1 to n4, 
which are connected in a cross-coupled fashion to form a latch. The latch provides a 
stable output voltage level that is midway between the power supply voltages.
The regulated pull-up network is implemented using two pMOS transistors p1 and p2, 
and one nMOS transistor n5. The gate of p1 is controlled by the input signal in, such that 
when in is high, p1 is turned on and provides a strong pull-up to the output signal out.
Similarly, the gate of p2 is controlled by the complement of in, such that when in is low,
p2 is turned on and provides a strong pull-up to out. The nMOS transistor n5 provides a 
weak pull-up to out at all times, to ensure that out is not left floating when neither p1 nor
p2 is turned on.
Overall, this voltage level shifter provides a rapid, low power, and reliable means of 
converting a signal from one voltage level to another.

