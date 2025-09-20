<h1 align="center">🌟 RISC-V SoC Tapeout – Week 0</h1> 
<br><br><br>
## 🚀 Getting Started with Digital VLSI SoC Design & Planning  
<p align="center">

<img width="1656" height="231" alt="Screenshot 2025-09-20 123854" src="https://github.com/user-attachments/assets/c8c14098-91a7-4859-b262-37d8eaaa46d2" />
</p>
 🟢 Step 1: Application & Chip Modeling  

    ```
    O0 == O1   → chip specification is valid 👍
   
    ```
## 🏗️ Step 2: RTL Development 
<p align="center">

<img width="1135" height="155" alt="Screenshot 2025-09-20 143448" src="https://github.com/user-attachments/assets/d06e460b-8e67-4387-8ff7-6cf88e57d9b2" />
</p>
## ⚙️ Step 3: ASIC Flow – Processor & Peripherals  

<p align="center">

<img width="1000" height="496" alt="Screenshot 2025-09-20 143607" src="https://github.com/user-attachments/assets/2685ef65-b896-43f2-9c95-cdc80e583341" />
</p>
## 🛠️ Step 4: OpenLane Flow (RTL → GDSII) 
<p align="center">
<img width="1011" height="559" alt="Screenshot 2025-09-20 143811" src="https://github.com/user-attachments/assets/3ccc9d02-cded-449c-a31b-e14c9b674b61" /></p>

- 🏗️ **OpenLane** is the open-source ASIC flow used for **tapeout preparation**.  
- 🔄 Flow includes:  

    ```text
    RTL → Netlist → Floorplan → Placement → Routing → GDSII
    ```

- 🖼️ **GDSII** = Final chip mask layout used for fabrication.  



<header>
<h1>🌟 RISC-V SoC Tapeout – Day 1</h1>
<p>Digital VLSI SoC Design & Tool Installation Documentation</p>
</header>

<div class="container">
<h2>1️⃣ Tools Installation</h2>
<h3>Yosys</h3>
<img width="976" height="327" alt="yosys inlcude" src="https://github.com/user-attachments/assets/ea223d58-c8ee-4c33-ab59-15e82579d3b4" />

<h3>Yosys version <img width="883" height="55" alt="Screenshot 2025-09-20 162459" src="https://github.com/user-attachments/assets/a00b97d7-c820-4b8c-98b1-6ead4ae5c093" /> </h3>






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

<img width="1872" height="682" alt="gtkwaveoutput" src="https://github.com/user-attachments/assets/061e6ebe-d58f-48b3-9782-18c9ea476cdd" />

<hr>
<h2>4️⃣ Truth Table</h2>
<img width="1919" height="275" alt="Screenshot 2025-09-20 170759" src="https://github.com/user-attachments/assets/a17c763a-136a-46d4-abf1-30c157ad2a13" />





<footer style="text-align:center; margin:2rem 0;">
<p>📌 Day 1 - RISC-V SoC Tapeout | Pandiyarajan.S</p>
</footer>
</div>
</body>
</html>
