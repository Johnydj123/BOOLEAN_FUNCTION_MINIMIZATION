# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Developed by:DINAGARAN JOHNY.S

RegisterNumber:212223220020
```
module Booleanexpressionmin(a,b,c,d,w,x,y,z,f1,f2); 
input a,b,c,d,w,x,y,z; 
output f1,f2; 
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u; 
not(adash,a); 
not(bdash,b); 
not(cdash,c); 
not(ddash,d); 
not(ydash,y); 
and(p,bdash,ddash); 
and(q,adash,b,d); 
and(r,a,b,cdash); 
or(f1,p,q,r); 
and(s,ydash,z); 
and(t,x,y); 
and(u,w,y); 
or(f2,s,t,u); 
endmodule
```

**RTL realization**

![WhatsApp Image 2024-09-13 at 14 17 26_f5ba0901](https://github.com/user-attachments/assets/846ffdcc-57d8-454f-91be-aad73345b600)

**Output:**


![WhatsApp Image 2024-09-13 at 14 18 25_e08755c7](https://github.com/user-attachments/assets/aca66712-5bdc-4b97-a10e-b43d43b37879)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

