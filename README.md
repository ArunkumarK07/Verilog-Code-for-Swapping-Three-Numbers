# Verilog-Code-for-Swapping-Three-Numbers
Aim
To design and simulate a Verilog HDL code for swapping the values of three numbers without using any temporary variables, and verify the correctness of the swapping operation through a testbench using the Vivado 2023.1 simulation environment.

Apparatus Required
Vivado 2023.1 or equivalent Verilog simulation tool.

Procedure
Launch Vivado 2023.1:

Open Vivado and create a new project.
Write the Verilog Code for Swapping:

Write the Verilog code that swaps the values of three numbers (a, b, and c) using basic arithmetic or bitwise operations without using temporary variables.
Create the Testbench:

Write a testbench to simulate the swapping operation. The testbench should initialize three numbers, trigger the swapping module, and check if the values are swapped correctly.
Add the Verilog Files:

Add the Verilog module and the testbench file to the Vivado project.
Run Simulation:

Run the behavioral simulation in Vivado to verify the swapping operation.
Observe the Waveforms:

Examine the waveform to confirm that the values of the three numbers are swapped as expected.
Save and Document Results:

Capture the waveform output and include the results in your report for verification.

Verilog Code:

module swap_three_numbers(
input [7:0] a, b, c,   
output reg [7:0] a_out, b_out, c_out 
);

always @(*) begin
    a_out = b;   
    b_out = c;   
    c_out = a;   
end

endmodule


Testbench for Swapping Three Numbers:

module tb_swap_three_numbers;
    reg [7:0] a, b, c;    
    wire [7:0] a_out, b_out, c_out;
    swap_three_numbers dut (
        .a(a), 
        .b(b), 
        .c(c),
        .a_out(a_out), 
        .b_out(b_out), 
        .c_out(c_out)
    );
     initial begin
        a = 8'd10;
        b = 8'd20;
        c = 8'd30;
        #10;
        $display("First swap completed.");
        a = 8'd50;
        b = 8'd60;
        c = 8'd70;
        #10;
        $finish;
    end

endmodule

output

![swap](https://github.com/user-attachments/assets/42e7ed56-f4d4-4687-906d-95f23dd75171)


Conclusion
In this experiment, a Verilog HDL code for swapping three numbers was designed and successfully simulated. The testbench verified the swapping operation, showing that the values of three input numbers (a, b, and c) were swapped correctly without the use of temporary variables. This experiment demonstrated the effectiveness of Verilog in implementing logical operations and control mechanisms such as swapping values. The simulation results confirm the correct functionality of the design.
