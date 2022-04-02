# LogicGatesEDAPlayground
In this Lab, we shall start Verilog. To run Verilog, we shall use http://www.edaplayground.com. After opening you will find Design or Testbench window pane. In the Design window you need write the Verilog Code and in the Testbench window, the testbench verification code will be written
1.	Write a Verilog code to implement AND gate. Write the corresponding Testbench code for the verification of your Verilog code.
Truth Table of AND Gate:

A	B	Y
1	1	1
1	0	0
0	1	0
0	0	0
ANS. 
 
 
 



 AND GATE (Design Bench.sv)
module andgate(a,b,c);
  input a;
  input b;
  output c;
  assign c = a & b;
endmodule
AND GATE (Test Bench.sv)
module tb_andgate();
  reg A,B,D,E,G,H,J,K;
  wire C, F,I,L;
//print
//Ayushman Pranav E21cseu0245
andgate a1(.a(A),.b(B),.c(C));
  initial begin
  A=1; B=1; #5;
    $display("And gate");
    $display("A B Result");
    $display("%b %b   %b",A,B,C);
  A=1; B=0; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=1; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=0; #5;
    $display("%b %b   %b",A,B,C);
  end 
// EP wave
  initial begin
    $dumpfile("dump.vcd");
  	$dumpvars(1);
  end
endmodule
  2)Write a Verilog code to implement OR gate. Write the corresponding Testbench code for the verification of your Verilog code.
Truth Table of OR Gate:

A	B	Y
1	1	1
1	0	1
0	1	1
0	0	0
ANS. 
 


 
 
 
OR GATE (Design bench.sv)
module Orgate(a,b,c);
  input a;
  input b;
  output c;
  assign c = a | b;
endmodule

OR GATE (Test bench.sv)
module tb_Orgate();
  reg A,B;
  wire C;
//print
//Ayushman Pranav E21cseu0245
Orgate a1(.a(A),.b(B),.c(C));
  initial begin
  A=1; B=1; #5;
    $display("Or gate");
    $display("A B Result");
    $display("%b %b   %b",A,B,C);
  A=1; B=0; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=1; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=0; #5;
    $display("%b %b   %b",A,B,C);
  end 
// EP wave
  initial begin
    $dumpfile("dump.vcd");
  	$dumpvars(1);
  end
endmodule
3)Write a Verilog code to implement XOR gate. Write the corresponding Testbench code for the verification of your Verilog code.
Truth Table of XOR Gate:

A	B	Y
1	1	0
1	0	1
0	1	1
0	0	0
ANS. 
 
 
 
XOR GATE (Design bench.sv)
module Xorgate(a,b,c);
  input a;
  input b;
  output c;
  assign c = a ^ b;
endmodule
XOR GATE (Test bench.sv)
module tb_Xorgate();
  reg A,B;
  wire C;
//print
//Ayushman Pranav E21cseu0245
Xorgate a1(.a(A),.b(B),.c(C));
  initial begin
  A=1; B=1; #5;
    $display("Or gate");
    $display("A B Result");
    $display("%b %b   %b",A,B,C);
  A=1; B=0; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=1; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=0; #5;
    $display("%b %b   %b",A,B,C);
  end 
// EP wave
  initial begin
    $dumpfile("dump.vcd");
  	$dumpvars(1);
  end
endmodule
4) Write a Verilog code to implement NOR gate. Write the corresponding Testbench code for the verification of your Verilog code.
Truth Table of NOR Gate:

A	B	Y
1	1	0
1	0	0
0	1	0
0	0	1
 
 
 
Nor Gate( Design bench )
module Norgate(a,b,c);
  input a;
  input b;
  output c;
  assign c = a ~| b;
endmodule
Nor Gate( Test Bench )
module tb_Norgate();
  reg A,B;
  wire C;
//print
//Ayushman Pranav E21cseu0245
Norgate a1(.a(A),.b(B),.c(C));
  initial begin
  A=1; B=1; #5;
    $display("Nor gate");
    $display("A B Result");
    $display("%b %b   %b",A,B,C);
  A=1; B=0; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=1; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=0; #5;
    $display("%b %b   %b",A,B,C);
  end 
// EP wave
  initial begin
    $dumpfile("dump.vcd");
  	$dumpvars(1);
  end
endmodule
5)	Write a Verilog code to implement NAND gate. Write the corresponding Testbench code for the verification of your Verilog code.
Truth Table of NAND Gate:

A	B	Y
1	1	0
1	0	1
0	1	1
0	0	1
 
 
 
Nand Gate (Design Bench)
module Norgate(a,b,c);
  input a;
  input b;
  output c;
  assign c = a ~| b;
endmodule
Nand Gate (Test bench )
module tb_Norgate();
  reg A,B;
  wire C;
//print
//Ayushman Pranav E21cseu0245
Norgate a1(.a(A),.b(B),.c(C));
  initial begin
  A=1; B=1; #5;
    $display("Nor gate");
    $display("A B Result");
    $display("%b %b   %b",A,B,C);
  A=1; B=0; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=1; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=0; #5;
    $display("%b %b   %b",A,B,C);
  end 
// EP wave
  initial begin
    $dumpfile("dump.vcd");
  	$dumpvars(1);
  end
endmodule
  
  
6)	Write a Verilog code to implement XNOR gate. Write the corresponding Testbench code for the verification of your Verilog code.
Truth Table of XNOR Gate:

A	B	Y
1	1	1
1	0	0
0	1	0
0	0	1
 
 
 
XnorGate ( Design Bench)
module Xnorgate(a,b,c);
  input a;
  input b;
  output c;
  assign c = a ~^ b;
endmodule
  XnorGate ( Test Bench)
module tb_Xnorgate();
  reg A,B;
  wire C;
//print
//Ayushman Pranav E21cseu0245
Xnorgate a1(.a(A),.b(B),.c(C));
  initial begin
  A=1; B=1; #5;
    $display("Xnorgate gate");
    $display("A B Result");
    $display("%b %b   %b",A,B,C);
  A=1; B=0; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=1; #5;
    $display("%b %b   %b",A,B,C);
  A=0; B=0; #5;
    $display("%b %b   %b",A,B,C);
  end 
// EP wave
  initial begin
    $dumpfile("dump.vcd");
  	$dumpvars(1);
  end
endmodule
