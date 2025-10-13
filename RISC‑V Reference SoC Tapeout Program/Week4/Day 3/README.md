# Day 3 ; Study and Analysis of the Voltage Transfer Characteristics .
## Todays Goals : 
## 1.Plot the Voltage Transfer Characteristics (VTC) of a CMOS inverter .
## 2.Perform Transient Analysis to calculate the inverter's rise and fall delays .

### Part 1 - VTC Analysis
<details>
  <summary> Step 1 :Run the SPICE Simulation </summary>
  We have to run the NGSPIICE file of [day3_inv_vtc_Wp084_Wn036.spice] as it is configured  for a DC sweep to generate the VTC curve. 
  <img width="1920" height="1080" alt="ng_day3_vtc" src="https://github.com/user-attachments/assets/63ae4242-fdec-412b-a603-63754c7e0d00" />
 
  Here we can see that the DC voltage is being sweeped and also the terminal output shows that the simulation has successfully completed, and the relevant vectors, including in and out, are ready for plotting.
</details>

<details>
  <summary> Step 2 :Plot the VTC Curve </summary>
  Once the simulation is complete, use the plot command in terminal . This wil show the output voltage as a function of the input voltage . 
  command :  plot out vs in 
  <img width="1920" height="1080" alt="day3 vtc graph" src="https://github.com/user-attachments/assets/d31b4833-b3f6-4d94-9a54-0331e73ef8ec" />

</details>

<details>
  <summary> Step 3 :Finding the switching voltage  </summary>
  The switching threshold value is a point on the curve having same input and output voltage are equal. 
  <img width="1920" height="1080" alt="day3 vtc graph plotting" src="https://github.com/user-attachments/assets/03b407ec-4ab4-4a70-a010-39499ae72d89" />
  the threshold voltage is approximately 0.876 V . 
</details>

### Part 2 - Transient Analysis

<details>
  <summary> Step 1 :Run SPICE for Transient Analysis </summary>
  Here also we will run the spice file named as [day3_inv_tran_Wp084_Wn036.spice] for transient simulation . <br>
  Run the file <br>
  <img width="1920" height="1080" alt="ng_day3 tran" src="https://github.com/user-attachments/assets/10d5c461-5c8a-42f7-9643-9d9ec996f2b9" />
  
</details>

<details>
  <summary> Step 2: Plot the Waveform </summary>
  We will place the both input and output waveforms to analyze the time domain response . <br>
  the command is : ngspice -> plot out vs time in .<br>
  Above command will open this graph : 
  <img width="1920" height="1080" alt="day3 tran graph" src="https://github.com/user-attachments/assets/77c4615f-5c21-47f1-a964-dbd462fc7bc9" />

</details>
<details>
  <summary> Step 3: Calculations of the rise and fall delays </summary>
  We will calculate the rise and fall delays by measuring the time it takes for the signal to transition between its 50% voltage level (0.9V) on both the input and output curves. To do this, we'll zoom in on the plot and click on the curves at 0.9V.
<details>
      <summary>Step 3.1 : Rise delay calculation  </summary>
  Click on the curves for the rising edge and Y coordinate as 0.9V and terminal provides the time for both curves .
  <img width="1920" height="1080" alt="day 3 tran rise_delay plot" src="https://github.com/user-attachments/assets/314e8c75-ad75-43a6-ab00-9a5ebbc28d39" />

  </details>
      <details>
  <summary> Step 3.2 : Fall delay calculation </summary>
        Click on the curves for the falling edge and Y coordinate as 0.9 V and terminal will provide the time for the both curves . 
        <img width="1920" height="1080" alt="day 3 tran fall_delay plot" src="https://github.com/user-attachments/assets/c69fc1a8-c779-43e2-9146-bd9aeeab263f" />

</details>
</details>
