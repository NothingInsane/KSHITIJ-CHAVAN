# Tool Installation and Snapshots
This part is about showing that all the software for the project is installed and working on my VM.

<details>
<summary> 1. Yosys </summary>
Yosys is a cool tool for synthesizing Verilog code.

Commands: <br>
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt-get install build-essential clang bison flex libreadline-dev gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3 libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install

To check it:
I just typed yosys and the prompt came up. So it's working.
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
</details>

<details>
<summary> 4. Ngspice </summary>

This tool is for simulating circuits. I had to download it and then compile it myself.
<br>

Commands :

Bash

sudo apt install build-essential autoconf automake libtool

# After downloading the tarball:
tar -xzvf ngspice.tar.gz
./configure --with-x --enable-cider --disable-debug
make
sudo make install

How to it:
Typing ngspice started up the console for the tool.


Screenshot:
</details>

<details>
<summary> 5. Magic </summary>

Magic is a tool for making chip layouts.<br>

Commands:
sudo apt-get install m4 tcsh csh libx11-dev tcl-dev tk-dev libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install


How to check it:
I just typed magic and a program window came up. It was working.

Screenshot:
</details>

<details>
<summary> 6. OpenLANE </summary>
OpenLANE is the whole system to make an ASIC from start to finish. It was a lot of steps, but it worked.

Commands :
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world
sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot


# After reboot, run:
docker run hello-world
git clone --depth 1 https://github.com/The-OpenROAD-Project/OpenLane.git
cd OpenLane/
make
make test


How to check it:
Run the make test command , and when it finished, it says Basic test passed.. That means everything is good.

Screenshot:
</details>
