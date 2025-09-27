<h1>Day 1: Introduction to Verilog RTL Design and Synthesis</h1>
<hr>
<p>This document outlines the concepts and labs completed on Day 1, covering the fundamental steps of Verilog RTL design, open-source simulation, and logic synthesis.</p>
<hr>
<h2>1. Verilog Simulation with iverilog and GTKWave</h2>
<p>The first part of the day focused on getting familiar with an open-source toolchain for digital design. We used <b>iverilog</b> for Verilog simulation and <b>GTKWave</b> for waveform analysis.</p>
<h3>Lab Objective</h3>
<p>The goal was to simulate a simple Verilog design and verify its behavior using waveforms.</p>
<h3>Lab Description</h3>
<ul>
    <li><b>Design:</b> A basic Verilog module was created to perform a simple function.</li>
    <li><b>Testbench:</b> A corresponding testbench was written to instantiate the design under test (DUT), provide stimulus to its inputs, and generate a Value Change Dump (<code>.vcd</code>) file for waveform visualization.</li>
</ul>
<h3>Terminal Commands</h3>
<pre><code>
iverilog -o sim.out design.v testbench.v
vvp sim.out
gtkwave dump.vcd
</code></pre>
<hr>
<h2>2. Logic Synthesis with Yosys and Sky130 PDK</h2>
<p>The second half of the day introduced logic synthesis, the process of converting a high-level RTL design into a gate-level netlist using a technology library. We used <b>Yosys</b> as the synthesis tool and the <b>Sky130 PDK</b> as the target technology.</p>
<h3>Lab Objective</h3>
<p>The goal was to synthesize our Verilog design and generate a gate-level netlist based on the Sky130 technology library.</p>
<h3>Lab Description</h3>
<p>The same Verilog design from the simulation lab was used. We wrote a Yosys script or used a series of commands to read the RTL, perform synthesis, and generate a final netlist that is optimized for the Sky130 technology.</p>
<h3>Terminal Commands</h3>
<pre><code>
yosys -p "read_verilog design.v; synth_sky130 -top my_module; write_verilog -top my_module netlist.v"
</code></pre>
<hr>
<h3>Summary of Key Learnings</h3>
<p>Day 1 provided a comprehensive introduction to the foundational steps of the RTL design flow. We successfully learned how to: write synthesizable Verilog code, use an open-source toolchain for simulation and waveform analysis (iverilog and GTKWave), and perform logic synthesis to convert an RTL design into a gate-level netlist using an open-source synthesis tool (Yosys) and a specific technology library (Sky130).</p>
