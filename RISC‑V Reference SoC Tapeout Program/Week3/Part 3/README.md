# Generate Timing Graphs with OpenSTA

## Focusing on applying the fundamentals of Static Timing Analysis (STA) by using the open-source tool OpenSTA. The objective is to perform practical timing analysis on a synthesized design, generate key timing reports and graphs, and interpret the results, such as identifying the critical path and understanding slack.

To be specific , we already simulated the graph of the RISC-V in Baby SoC format . The output was post_synth_sim.v <br>
Soo ,  here in this part we will do Static Timing Analysis we learned from STA - 1 from the course . Here the result we get at last are the text file showing the analysis of the hold and setup time of .scd file .


### Step-by-Step Execution Plan
* Load Design and Constraints

* Start by launching the OpenSTA tool.

* Load your synthesized netlist (.v file) from Part 1.

* Load the design constraints, which typically include clock definitions and timing exceptions, from a .tcl or .sdc file.

* Generate Timing Reports and Graphs

* Use OpenSTA commands to perform a full timing analysis on the loaded design.

* Generate a timing report that details the timing paths, including the critical path (the path with the worst timing).

* Create a graphical representation of the timing paths. This visual graph helps in understanding the signal flow and delays along the path.

* Capture timing report and its corresponding graph for your deliverables.

<img width="1920" height="1080" alt="sta_command" src="https://github.com/user-attachments/assets/5d653afd-cf07-4f46-b94b-f5eb80bf3324" />


### Analyze and Interpret Results

* Identify the critical path from the timing report.

* Note the slack of the critical path and other key paths.

* Interpret what the slack indicates.

### Hold Time Analysis :

<img width="1920" height="1080" alt="2" src="https://github.com/user-attachments/assets/1ea43bcb-8399-4550-bdc0-8a29f4c88211" />

### Setup Time Analysis :

<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/7d6b5345-d28d-4206-839a-0e9f5be5d06d" />

