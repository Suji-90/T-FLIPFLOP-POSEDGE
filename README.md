## NAME:SUJITHRA.K
## REGISTER NUMBER:212223040212
# T-FLIPFLOP-POSEDGE

## AIM:

To implement  T flipflop using verilog and validating their functionality using their functional tables

## SOFTWARE REQUIRED:

Quartus prime

## THEORY:

## Flip-Flop:

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

## Procedure:
Step 1: Open Quartus II in your laptop.

Step 2: Write code to implement SR flipflop using verilog and validating their functionality using their functional tables.

Step 3: Run compilation to check for errors.

Step 4: Open waveform output and load input values.

Step 5: Run simulation to get the output.

Step 6: Open in RTL viewers to get RTL diagram output.


## PROGRAM:

 Program for flipflops and verify its truth table in quartus using Verilog programming. 
```
module TFLIPFLOPPOSEDGE( input clk, rst_n, input t,
output reg q,
output q_bar
);
always@(posedge clk) 
begin 
if(!rst_n)
q<=0;
else
if(t)
q<=~q;
else
q<=q;
end
assign q_bar = ~q;
endmodule
```
 
## RTL LOGIC FOR FLIPFLOPS:
![325183738-7899a3ad-8f6f-4d52-b2e8-854bea3d276a](https://github.com/Suji-90/T-FLIPFLOP-POSEDGE/assets/150884148/ad74b3bd-b569-48c5-aecf-2d787c62a847)


## TIMING DIGRAMS FOR FLIP FLOPS:
![325183758-c934697c-4e75-4bfa-957b-869da297711d](https://github.com/Suji-90/T-FLIPFLOP-POSEDGE/assets/150884148/6e8fea75-3d41-4e6e-8ba4-03ac724982ed)


## RESULTS:
Hence, T flipflop using verilog and validating their functionality using their functional tables is implemented.
