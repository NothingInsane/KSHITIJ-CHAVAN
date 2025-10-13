# **Lets start with Day 1**

In Day 1 we are introduced with the **NMOS transistor** .

So we have to understand how an ;

    --> NMOS transistor works in resistive and saturation regions

&nbsp;   --> how NGSPICE can be used to simulate Id-Vds characteristics for different transistor sizes





Note : W/L is device size parameter  
Larger W -> More Current  
Larger L -> Less Current

## *LAB Setup Steps*

### Step 1 :

To setup up the lab we need to clone this repo (https://github.com/kunalg123/sky130CircuitDesignWorkshop.git) into the VM-ware .

note: use **cd** to enter into folder and **ls** to see its contents .

### Step 2 :

Go to the directory where we can run the ngspice simulations as done in screenshot

<img width="1920" height="1080" alt="1 setupday1" src="https://github.com/user-attachments/assets/54afad9b-b9c7-4f73-9616-01b6665e43e9" />



here we can see the "vim day1\_nfet...."

### Step 3 :

Run the **vim** code

<img width="1920" height="1080" alt="2 vimday1" src="https://github.com/user-attachments/assets/eaeba7d7-d511-47c5-b33f-93206d7a3ef7" />

here we can see the parameters like W , L , Vdd , Vin .

key observation - **W/L ratio** is 2.5

### Step 4 :

Open another terminal and run :
ngspice day1\_nfet....

<img width="1920" height="852" alt="3 ngspiceday1" src="https://github.com/user-attachments/assets/9a7ed21c-df24-44d8-b261-9d5b3811d649" />

here you can see the run analysis of ngspice

we want to focus on the the **Vdd#branch**

### Step 5 :

run : plot -vdd#branch

<img width="1920" height="1080" alt="4 graphday1" src="https://github.com/user-attachments/assets/0cb5afdb-6df3-449f-be9f-0238bbbe1d73" />

here the reason to plot vdd using minus sign is that we need to study the current delivered to the positive terminal .

*vdd#branch* shows the current provided or consumed

now right click the mouse and drag over the graph in region of 1.2V .
this zooms the graph . Then click the curve where it intersects the gridline of 1.2V .

This displays the coordinates of that point in the ngspice terminal .



<img width="713" height="86" alt="3 2 ngspiceday1" src="https://github.com/user-attachments/assets/888f7022-9bd6-42fe-958c-c0edc95bf345" />

