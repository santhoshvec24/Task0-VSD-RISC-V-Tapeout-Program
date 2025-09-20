# RISC-V Reference SoC Tapeout Program VSD
## Tools Installation

   All the instructions for installation of required tools can be found here:</ins>

### System Requirements



### TOOLS INSTALLATION


#### <ins>Yosys Installation</ins>
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
git submodule update --init --recursive
make
sudo apt install yosys
```
### TOOL CHECK:
```
yosys
```

<img width="774" height="469" alt="Screenshot from 2025-09-19 22-05-57" src="https://github.com/user-attachments/assets/291c313a-02f2-4f0d-9648-bcc72a85e078" />

#### <ins>Iverilog</ins>
```bash
sudo apt-get update
sudo apt-get install iverilog
```
### TOOL CHECK:
```
iverilog -v
```
<img width="775" height="559" alt="Screenshot from 2025-09-19 22-08-11" src="https://github.com/user-attachments/assets/4d113347-d701-4fcc-bc56-4e9fb0a5cf26" />

#### <ins>gtkwave</ins>
```bash
$ sudo apt-get update
$ sudo apt install gtkwave
```
### TOOL CHECK:
```
 gtkwave -v
```

<img width="1209" height="543" alt="Screenshot from 2025-09-19 22-13-28" src="https://github.com/user-attachments/assets/eba7b2dd-7741-4cf4-838b-835c5d6d6e37" />

