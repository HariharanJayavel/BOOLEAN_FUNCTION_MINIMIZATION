# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**TRUTHTABLE**

![image](https://github.com/HariharanJayavel/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870546/b04fb7de-85ad-45fb-9007-0432fb178dc1)

**Program:**
```c
Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
Developed by: HARIHARAN J
RegisterNumber: 212223240047

module Booleanfunction(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u,v,w1,w2,x1,x2,y1,y2,z1,z2;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(w1,a,b,c);
and(w2,~a,~b,~c);
or(f2,w1,w2);
endmodule
```

**RTL realization**

![image](https://github.com/HariharanJayavel/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870546/5deab625-cfdd-4b5c-ba8c-70d3ab17bf01)

**Timing Diagram**

![image](https://github.com/HariharanJayavel/BOOLEAN_FUNCTION_MINIMIZATION/assets/144870546/663e5386-9a8c-4691-a22e-6cb2030633af)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

