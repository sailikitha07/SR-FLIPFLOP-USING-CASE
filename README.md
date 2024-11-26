![Screenshot 2024-11-26 110337](https://github.com/user-attachments/assets/33191abb-bee9-4aea-abc9-3eaedf7fd123)# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

```

/*
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

 */

```

**PROGRAM**

```

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:sai likitha.ch RegisterNumber:24009865
module exp6(q, qbar, s, r, clk);
input s,r,clk; 
output q, qbar;
wire nand1_out; // output of nand1 
wire nand2_out; // output of nand2 
nand (nand1_out,clk,s); 
nand (nand2_out,clk,r); 
nand(q,nand1_out,qbar);
nand(qbar,nand2_out,q);
endmodule 
*/

```

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-11-26 110337](https://github.com/user-attachments/assets/8af3fa07-0911-40fe-ac57-5e3f79bcf29f)

**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-11-26 113913](https://github.com/user-attachments/assets/ba7d0635-1610-4700-987f-ab5daffc47ce)

**RESULTS**
Thus to implement SR flipflop using verilog and validating their functionality using their functional tables are done successfully.
