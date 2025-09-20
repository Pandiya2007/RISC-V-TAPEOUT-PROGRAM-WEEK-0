<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Day 1 - RISC-V SoC Tapeout</title>
<style>
    body { font-family: Arial, sans-serif; background: #f9f9f9; margin:0; padding:0;}
    header { background:#1e2a38; color:white; text-align:center; padding:2rem 1rem;}
    h1, h2, h3 { color:#2c3e50; }
    .container { max-width:1200px; margin:2rem auto; padding:1rem; background:white; border-radius:10px; box-shadow:0 0 10px rgba(0,0,0,0.1);}
    pre { background:#eee; padding:1rem; overflow-x:auto; border-radius:5px;}
    img { max-width:100%; margin:1rem 0; border-radius:10px; }
    table { border-collapse: collapse; width:100%; margin:1rem 0;}
    th, td { border:1px solid #ccc; padding:0.5rem; text-align:center;}
    code { background:#eee; padding:2px 5px; border-radius:3px;}
</style>
</head>
<body>

<header>
<h1>🌟 RISC-V SoC Tapeout – Day 1</h1>
<p>Digital VLSI SoC Design & Tool Installation Documentation</p>
</header>

<div class="container">
<h2>1️⃣ Tools Installation</h2>
<h3>Yosys</h3>
<img src="" alt="Yosys Screenshot">

<h3>Icarus Verilog</h3>
<img src="assets/iverilog.png" alt="Icarus Verilog Screenshot">

<h3>GTKWave</h3>
<img src="assets/gtkwave.png" alt="GTKWave Screenshot">

<hr>
<h2>2️⃣ Verilog Design - Full Adder</h2>
<h3>full_adder.v</h3>
<pre><code>module full_adder(
    input a, b, cin,
    output sum, cout
);
assign sum  = a ^ b ^ cin;
assign cout = (a & b) | (b & cin) | (a & cin);
endmodule</code></pre>

<h3>tb_full_adder.v</h3>
<pre><code>`timescale 1ns/1ps
module tb_full_adder;
reg a,b,cin;
wire sum,cout;
full_adder uut(.a(a),.b(b),.cin(cin),.sum(sum),.cout(cout));
initial begin
    $dumpfile("full_adder.vcd");
    $dumpvars(0,tb_full_adder);
    $display("A B Cin | Sum Cout");
    a=0;b=0;cin=0;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    a=0;b=0;cin=1;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    a=0;b=1;cin=0;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    a=0;b=1;cin=1;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    a=1;b=0;cin=0;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    a=1;b=0;cin=1;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    a=1;b=1;cin=0;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    a=1;b=1;cin=1;#10;$display("%b %b %b | %b %b",a,b,cin,sum,cout);
    $finish;
end
endmodule</code></pre>

<h2>3️⃣ Waveform Output</h2>
<img src="assets/waveform.png" alt="Full Adder Waveform">

<hr>
<h2>4️⃣ Truth Table</h2>
<table>
<tr><th>A</th><th>B</th><th>Cin</th><th>Sum</th><th>Cout</th></tr>
<tr><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>0</td><td>0</td><td>1</td><td>1</td><td>0</td></tr>
<tr><td>0</td><td>1</td><td>0</td><td>1</td><td>0</td></tr>
<tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
<tr><td>1</td><td>0</td><td>0</td><td>1</td><td>0</td></tr>
<tr><td>1</td><td>0</td><td>1</td><td>0</td><td>1</td></tr>
<tr><td>1</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
<tr><td>1</td><td>1</td><td>1</td><td>1</td><td>1</td></tr>
</table>

<footer style="text-align:center; margin:2rem 0;">
<p>📌 Day 1 - RISC-V SoC Tapeout | Created by Your Name</p>
</footer>
</div>
</body>
</html>
