# Week 3 Task: Post-Synthesis GLS & STA Fundamentals

### Objective

The goal of this task is to perform a **Gate-Level Simulation (GLS)** on the BabySoC design after the synthesis process. This involves validating the design's functionality at the gate level and ensuring that the synthesized netlist behaves identically to the original functional simulation. The deliverables include synthesis logs, GLS waveform screenshots, and a short note confirming that the outputs match

---

### Part 1: Post-Synthesis GLS

#### 1. Synthesis of BabySoC Design

This phase uses Yosys to convert the high-level RTL (Register-Transfer Level) code into a gate-level netlist, which consists of basic logic gates and their interconnections.

**Steps:**

* **Load Design Files:** The process begins by launching Yosys and loading the main Verilog modules: `vsdbabysoc.v`, `rvmyth.v`, and `clk_gate.v`<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/0fa74ab9-4d29-4027-950b-7b6c729a26d2" />


* **Load Liberty Files:** Next, the corresponding `.lib` files for the PLL, DAC, and the `sky130_fd_sc_hd` standard cell library are loaded. [cite_start]These files provide the characteristics of the physical gates that will be used in the design  <img width="1920" height="1080" alt="2" src="https://github.com/user-attachments/assets/c2f53523-34ee-443d-b778-5b3f4b3299c2" />

* **Run Synthesis:** The `synth -top vsdbabysoc` command is executed to perform the core synthesis. <img width="1920" height="1080" alt="3" src="https://github.com/user-attachments/assets/b6d1b6df-cb6d-4416-9823-918a31032c0c" />


* **Map Flip-Flops:** The `dfflibmap` command maps the D flip-flops from the RTL to the specific D flip-flop standard cells available in the `sky130_fd_sc_hd` library. <img width="1920" height="1080" alt="4" src="https://github.com/user-attachments/assets/35935c99-e20a-441d-bb8e-14466a996617" />

  
* **Optimize and Clean Up:** Commands like `opt`, `abc`, `flatten`, and `clean` are used to optimize the netlist, remove unused components, and prepare the design for output. <img width="1920" height="1080" alt="5" src="https://github.com/user-attachments/assets/4a2aa4d3-b402-49f1-9be5-0903d568a757" />



* **Write Synthesized Netlist:** The final step is to write the gate-level netlist to a Verilog file named `vsdbabysoc.synth.v`. <img width="1920" height="1080" alt="6" src="https://github.com/user-attachments/assets/4c24c9c4-c5f7-49c6-bec4-54e870fe5e85" />


<br>


---

#### 2. Running Gate-Level Simulation (GLS)

With the synthesized netlist, we use Icarus Verilog to run a gate-level simulation. This simulation verifies the design's functionality using the actual gate delays.

**Steps:**

* **Compile the Testbench:** The `iverilog` command is used to compile the testbench along with the synthesized netlist. The `-DPOST_SYNTH_SIM` flag ensures the simulation uses the new gate-level design, and `-DUNIT_DELAY=#1` introduces a unit delay for all components to mimic real-world gate delays.
* **Execute Simulation:** The compiled output file is executed, generating a `post_synth_sim.vcd` file. This VCD file contains the waveform data for the simulation.
* **View Waveforms:** The `gtkwave` tool is used to open and analyze the VCD file, allowing for a visual inspection of the simulation results.

---

#### 3. Deliverables and Results

* **Synthesis Logs:** The synthesis logs are provided as part of the documentation, showing the successful synthesis flow and final cell count statistics.
* **GLS Waveform Screenshots:** Screenshots from GTKWave show the simulated waveforms of key signals, demonstrating the post-synthesis behavior. The waveforms for the DAC and other modules can be visually confirmed to be correct.
* **GLS Output Confirmation:** The results from the post-synthesis GLS match the output from the functional simulation performed in Week 2. This confirms that the synthesis process was successful and the design's intended behavior has been preserved at the gate level.

<img width="1920" height="1080" alt="7" src="https://github.com/user-attachments/assets/09724edc-ed2e-44da-9226-2a33cc03a71f" />

<img width="1920" height="1080" alt="8" src="https://github.com/user-attachments/assets/c490ec2d-025a-4f40-8578-1148f8eea281" />

<img width="1920" height="1080" alt="9" src="https://github.com/user-attachments/assets/a9cd3262-c2a0-4d07-902f-9f1fa1d3ee25" />


<br>
