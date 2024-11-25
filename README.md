# Verilog-Code-for-Swapping-Three-Numbers
Aim
To design and simulate a Verilog HDL code for swapping the values of three numbers without using any temporary variables, and verify the correctness of the swapping operation through a testbench using the Vivado 2023.1 simulation environment.
module swap_three_numbers( input [7:0] a, b, c, output reg [7:0] a_out,
b_out, c_out );
always @(*) begin
a_out = b;
b_out = c;
c_out = a; end
endmodule
Testbench for Swapping Three Numbers:
module tb_swap_three_numbers;
reg [7:0] a, b, c; wire
[7:0] a_out, b_out, c_out;
swap_three_numbers dut (
.a(a),
 .b(b),
 .c(c),
 .a_out(a_out),
 .b_out(b_out),
 .c_out(c_out) ); initial
begin a = 8'd10; b =
8'd20; c = 8'd30; #10;
$display("First swap completed.");
a = 8'd50; b = 8'd60; c =
8'd70; #10; $finish;
end endmodule

Conclusion
In this experiment, a Verilog HDL code for swapping three numbers was designed and successfully simulated. The testbench verified the swapping operation, showing that the values of three input numbers (a, b, and c) were swapped correctly without the use of temporary variables. This experiment demonstrated the effectiveness of Verilog in implementing logical operations and control mechanisms such as swapping values. The simulation results confirm the correct functionality of the design.
