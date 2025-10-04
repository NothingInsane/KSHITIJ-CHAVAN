
<details>
  <summary> What is SoC ? </summary>
  A System-on-Chip(SoC) is a single , integrated circuit that combines all the components of an entire computer or electronic system onto a single silicon die. This includes a central processing unit (CPU), memory (RAM/ROM), input/output (I/O) ports, and other peripherals, all interconnected within one chip. By integrating these components, SoCs achieve significant advantages in size, power consumption, and performance compared to older designs where separate chips for each function were mounted on a printed circuit board (PCB).
</details>

<details>
  <summary> Components of a Typical SoC </summary>
Typical SoC is a self-contained system with several essential building blocks:

### CPU (Central Processing Unit): 
The brain of the SoC, which executes instructions and manages all system operations. In the BabySoC model, this role is fulfilled by the RVMYTH RISC-V CPU.


### Memory:
Provides storage for data and program instructions. SoCs use different types of memory, such as volatile RAM for temporary data and non-volatile ROM or Flash for storing firmware.


### Peripherals/I/O Blocks:
These are the interfaces that allow the SoC to interact with the external world. Examples include a Digital-to-Analog Converter (DAC), an Analog-to-Digital Converter (ADC), USB, and UART. BabySoC utilizes a 10-bit DAC for this purpose.

### Clock & Power Management:
SoCs require a stable clock to synchronize all the internal modules. A Phase-Locked Loop (PLL), as used in BabySoC, is a common component that generates and stabilizes the clock signal.

### Interconnect (Communication Bus): 
Acts as the internal "highway" that connects the CPU, memory, and peripherals, allowing them to communicate and transfer data.
</details>

<details>
  <summary> Why BabySoC is a Simplified Model for Learning </summary>
BabySoC is designed as a learning tool, providing a representative but minimal platform for students to grasp SoC design concepts without being overwhelmed.<br>
  
## It offers several educational advantages: 

### It strips down the complexity of commercial SoCs by focusing on a few core components—a CPU (RVMYTH), a PLL, and a DAC—to teach the fundamental interactions between digital and analog blocks.

### Focused Scope: Unlike a complex commercial chip with hundreds of modules, BabySoC’s limited scope allows students to concentrate on the key concepts of processor architecture, clock management, and interfacing.

### Open-Source Nature: The use of open-source technologies like Sky130 and RISC-V allows students to freely experiment, modify, and simulate the design, providing a hands-on learning experience that's often not possible with proprietary hardware.

### Educational Progression: It provides a holistic view of the SoC design process by integrating digital, analog, and mixed-signal components, covering all crucial domains for an aspiring chip designer. 
</details>

<details>
  <summary>
The Role of Functional Modeling
  </summary>

### Functional modeling is a critical, early-stage step in the SoC design workflow that occurs before Register-Transfer Level (RTL) and physical design. Its purpose is to create a high-level behavioral model of the chip using languages like C or SystemC.

### Behavioral Verification: At this stage, designers verify that the chip's logical behavior is correct and meets the high-level specifications. For example, a functional model of BabySoC would confirm whether the CPU's digital output is properly converted into the intended analog waveform by the DAC.

### Early Debugging: Finding and fixing design flaws at the functional level is significantly easier and cheaper than later in the process. Debugging at the RTL or physical design stages can be a time-consuming and expensive ordeal, sometimes requiring a complete redesign.

### Functional modeling serves as a crucial sanity check, ensuring the foundational logic of the system is sound before investing a massive amount of time and resources into the detailed RTL coding and the even more complex physical layout of the chip
  
</details>






