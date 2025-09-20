# Tool Installation and Screenshots
The prequesite is to have a Ubuntu 20.04 above OS , I did my setup using Ubuntu 22.04 with VM Ware. <br>
This part is about showing that all the software for the project is installed and working on my VM.

<details>
<summary> 1. Yosys </summary>
Yosys is a cool tool for synthesizing Verilog code.

Commands: <br>
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make (If make is not installed please install it)
$ sudo apt-get install build-essential clang bison flex \
 libreadline-dev gawk tcl-dev libffi-dev git \
 graphviz xdot pkg-config python3 libboost-system-dev \
 libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
$ sudo make install 


To check it:
I just typed yosys and the prompt came up. So it's working.<br>

Screenshot : <img width="1920" height="1080" alt="VirtualBox_Kshitij-VSD_20_09_2025_23_08_39" src="https://github.com/user-attachments/assets/87d136a4-e910-4852-b1ea-76da7001fc57" />

</details>

<details>
<summary> 2. Icarus Verilog (Iverilog) </summary>

This one is a compiler for Verilog. It turns the code into something the computer can run.<br>

Commands :
sudo apt-get update
sudo apt-get install iverilog 


TO check it:
I just typed iverilog and it showed me the help menu. It didn't say "command not found," so that's what we want . 


Screenshot:
<img width="1920" height="1080" alt="iverilog" src="https://github.com/user-attachments/assets/d4f09312-90b0-4d61-b61c-eed568035f14" />


</details>

<details>
<summary> 3. GTKWave </summary>

GTKWave is for looking at the waveforms from the simulations.<br>

Commands :
sudo apt-get update
sudo apt install gtkwave

To check it:
I typed gtkwave and a window showed up. That's how I knew it worked.


Screenshot:
<img width="1920" height="1080" alt="gtkwave" src="https://github.com/user-attachments/assets/2f96313c-c549-43b1-add6-a30c46a7c023" />


</details>

<details>
<summary> 4. Ngspice </summary>

This tool is for simulating circuits. I had to download it and then compile it myself.
<br>
 1st download the tarball from https://sourceforge.net/projects/ngspice/files/ to a local directory and then unpack it using 
Commands :

$ tar -zxvf ngspice-37.tar.gz
$ cd ngspice-37
$ mkdir release
$ cd release
$ ../configure --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install 


# After downloading the tarball:
tar -xzvf ngspice.tar.gz
./configure --with-x --enable-cider --disable-debug
make
sudo make install

How to it:
Typing ngspice started up the console for the tool.


Screenshot:
<img width="1920" height="1080" alt="ngspice2" src="https://github.com/user-attachments/assets/746514ac-701c-43d5-8d1b-8f984a98a91f" />


</details>

<details>
<summary> 5. Magic </summary>

Magic is a tool for making chip layouts.<br>

Commands:<br>
$ sudo apt-get install m4
$ sudo apt-get install tcsh
$ sudo apt-get install csh
$ sudo apt-get install libx11-dev
$ sudo apt-get install tcl-dev tk-dev
$ sudo apt-get install libcairo2-dev
$ sudo apt-get install mesa-common-dev libglu1-mesa-dev
$ sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
make install 


How to check it:
I just typed magic and a program window came up. It was working.

Screenshot:
<img width="1920" height="1080" alt="magic2" src="https://github.com/user-attachments/assets/75fb1657-09c6-44c6-8cd4-389680c4a3d6" />


</details>

<details>
<summary> 6. OpenLANE </summary>
OpenLANE is the whole system to make an ASIC from start to finish. It was a lot of steps, but it worked.

Commands :<br>

sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git 
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o
/usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg]
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee
/etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world 
sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot

### After reboot, run:
docker run hello-world

Screenshot : 
<img width="1920" height="1080" alt="Openlane2" src="https://github.com/user-attachments/assets/4df2e86b-a5fb-41cf-9d5e-9be8d2ef359b" />

### To check installation 

Check dependencies
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
python3 -m venv -h 

Screenshot:
<img width="1920" height="1080" alt="version_check" src="https://github.com/user-attachments/assets/faf44dd7-2923-4c68-9d7e-2425e59885e8" />


### Below steps installs PDKs and Tools
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test 

Screenshot:
<img width="1920" height="1080" alt="final test passed" src="https://github.com/user-attachments/assets/ba43001a-a884-47e9-92e2-97887996d134" />


</details>
