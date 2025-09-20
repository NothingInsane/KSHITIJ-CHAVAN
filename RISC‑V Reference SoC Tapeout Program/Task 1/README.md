# Overview
In this I watched the theory video {1-Getting started with Digital VLSI SOC Design and Planning} along with the setting up of Ubuntu and its tools installation. 
## Task 1 - Lecture Theory 
The lecture conducted by the sir was regarding the VLSI methodology with reference to the VSD- Squadron . The core idea was to verify the design at every stage , from high-level software models to the final hardware implementation . THe process can be broken down into the following key steps :

### Fundamental Ideology : 
<details>
  <summary> 1. Golden Model Creation and Verification </summary>
<br>
A. Output 0 Verification :The C model is compiled using GCC ( GNU Compiler Collection ) . This creates a basic executable output with minimal optimization , we will name it O0 <br>
B. This O0 is our baseline reference for the system's behavoir .<br>
</details>

<details>
  <summary> 2. SPEC Verification </summary>
The same C model is run through a SPEC tool to generate a Output 1 . Maily used to simulate performance and check for any deviations fron the Golden Model .
</details>

<details>
  <summary> 3. Consistency Check</summary>
A critical verification step is to compare the O0 with the O1 . <br>
If O0 == O1 , the C model is considered consistent and correct . This confirms that the software logic is ok and we can proceed towards hardware design phase . <br>
Now as the outputs are matched , we have established a reliable GOlden Model that will be used for all consequent hardware verification 
</details>

### Hardware Implementation and RTL Verification 

Once the Golden Modle is validated , we wil do designing of hardware using a HDL .<br>

<details>
  <summary> 1. RTL Design </summary>
A. The HDL will be Verilog RTL model . This is like a softcopy of the hardware design .<br>
B. This Verilog code is written to be a direct representation of the C Golden Model .
</details>

<details>
  <summary> 2. RTL to C - Verification </summary>

  A. The behavoir of the Verilog code is simulated and its results are compared against the outputs of the original C model . <br>
  B. If the results match , it confirms that the hardware design at the RTL level correctly implements the required logic . This is a crucial check before moving on to physical synthesis
</details>

### SoC Architecture & Synthesis 

This is where we study to convert high level design into a physical format . The Verilog RTL is divided and synthesized into a physical implementation . 
<details>
  <summary> 1. Processors : </summary>
  A. The processor cores are synthesized into a Gate Level netlist , this is the first level of physical implementation , transforming RTL logic into an interconnected network of standard digital gates . <br>
  B. In lecture it is refered as "synth P1" .
</details>

<details>
  <summary> 2. Peripherals :</summary>

  Peripherals are categorized into two types : 
  1. Macros :These are pre-designed , hardened blocks that are synthesized at the RTL level ( synth RTL )<br>
  2. Analog IP's : These ar etypically provided as pre-designed functional blocks with a functional RTL description for integration . 
</details>

### Final System Verification : 
The final step in this process is a comprehensive check of the entire integrateed system . <br>

<details>
  <summary> 1. GPIO </summary>
  The lecture used the GPIOs as a concrete example of final check .
</details>
<details>
  <summary> 2. Final Condition </summary>
  The output from the GPIOs must exactly match the original outputs from the GOlden Model ( O0 and O1 ).<br>  THis final verification step ensuress that the entire chain , from the initial code to the final Gate level and peripherals implementation is correct 
</details>

## Check Task 2 for documentation regarding tools installation .


