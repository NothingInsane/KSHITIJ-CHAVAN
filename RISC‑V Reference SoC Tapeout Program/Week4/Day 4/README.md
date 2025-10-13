# Day 4 : Study of Noise Margin of CMOS Inverter

## Today's Goals : 

## 1. Understand the concept of noise margin as a measure of a circuit's robustness.
## 2. Perform a SPICE simulation to find the key voltage points on the Voltage Transfer Curve (VTC).
## 3. Calculate the High Noise Marggin and Low Noise Margin .

### Part 1
<details>
  <summary> Step 1 : Running the Simulation </summary>
  Open the terminal <br>
  There run the command : ngspice day4_inv_noisemargin_wp1_wn036.spice <br>
   This will run the ngspice 
  <img width="1920" height="1080" alt="ng_noise_margin" src="https://github.com/user-attachments/assets/1d401860-cf19-4c5c-8788-3805daa267ff" />

</details>
<details>
  <summary> Step 2 : Plot the graph </summary>
  We have to run the plot command to visualize the output voltage as the function of input voltage . <br>
  In ngspice terminal ; run the command : plot out vs in 
 <img width="1920" height="1080" alt="noise_margin graph" src="https://github.com/user-attachments/assets/c5a34d2b-7bed-4d45-a8bb-50eecbeed29d" />

</details>

### Part 2 

<details>
   <summary> Step 3 : Analysis of the curve </summary>
  Here the curve shows us 4 major parameters : Input low voltage , Output High Voltage , Input High voltage , Output high voltage . <br>
  Click on the curve where the slope get -1 on both sides . 
 <img width="1920" height="1080" alt="noise margin plotting" src="https://github.com/user-attachments/assets/a6233938-2d4c-4f1f-810d-01b04d76a9e1" />

Here the coordinates are respective parameters from the curve . <br>
X0 = 0.777 V , Y0 = 1.696 V <br>
X0 = 0.987 V , Y0 = 0.096 V <br>

this shows that we got enough data to calculate the noise margins .<br.
High Noise margin : 1.696V -0.987V <br>
   = 0.709V <br>

Low noise margin : 0.777V - 0.096V <br>
       = 0.681V 
                                                                                                                            
</details>
