NAME: YUVASHREE R

REG NO: 212224040378
# SERIAL IN SERIAL OUT SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1.Write the Verilog module with inputs clk, reset, serial_in, and output serial_out.

2.Implement logic to shift input bits into the register on every clock pulse.

3.Create a Verilog testbench to apply input sequences and generate clock signals.

4.Simulate the design and observe the output waveforms using a simulator.

5.Compare simulation results with the functional table to validate correctness.

**PROGRAM**

```
module siso(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
```

**RTL LOGIC FOR SISO Shift Register**


![Screenshot 2025-05-14 131719](https://github.com/user-attachments/assets/e084be80-a83a-4d11-a909-6fb9d4bb627e)


**TIMING DIGRAMS FOR SISO Shift Register**

![Screenshot 2025-05-14 132811](https://github.com/user-attachments/assets/ecf934cf-ea05-4e5d-86b8-3d6537739f8d)


**RESULTS**

Thus THE-SERIAL-IN-SERIAL-OUT-SHIFTREGISTER was successfully verified.
