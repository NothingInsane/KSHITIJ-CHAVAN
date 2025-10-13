# Day 5 : Study of robustness of inverter in Process and Supply Variation

## Today's goals :

## Analysis of how device variation (changing transistor sizes) affects the CMOS inverter's VTC .
## Analyze how supply voltage variation affects the inverter's VTC .


### Part 1: Inverter's Robustness for Supply voltage variation :

<details>
  <summary>  Step 1 : SPICE Simulation </summary>
  We will run the ngspice file to seep dc voltage . <br>
  <img width="1920" height="1080" alt="Ngspice Day5supply_voltage" src="https://github.com/user-attachments/assets/c95e3432-fe7d-44af-b409-de6ade43f6d3" />


</details>

<details>
  <summary> Step 2 : Get the coordinates to observe the gain . </summary>
  In given grraph ,  click the curve of 1.8V to get Gain 
  <img width="1920" height="1080" alt="ngspice day5supply-voltage" src="https://github.com/user-attachments/assets/d6c3c33c-34c2-477e-9026-39b49f90d215" />

</details>

### Part 2 : Inverter Robustness to Device Variation ;

<details>
  <summary> Step 1 : Run the Simulation </summary> 
  run simulation by ngspice command : ngpice day5_inv_devicevariation_wp7_wn042.spice <br>
  <img width="1920" height="1080" alt="ngspice day5device-variation" src="https://github.com/user-attachments/assets/f006831c-391f-440a-8f7a-491f3abd3650" />

</details>

<details>
  <summary> Step 2 : Plot the graph </summary>
  run ; "plot out vs in" in the SPICE terminal to plot the graph .<br>
  <img width="1920" height="1080" alt="graph day5device-variation" src="https://github.com/user-attachments/assets/55156363-3ca3-4be6-bc59-605d88b8bcb4" />

  Then find the threshold voltage <br>
  <img width="1920" height="1080" alt="plotting day5device-variation" src="https://github.com/user-attachments/assets/471c10a2-38ec-4720-9eaf-99ead3ffe5bc" />

 the switching threshold value is approximately = 0.98V
</details>
