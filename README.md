# Week 0 VSD RISC-V Tapeout Program
This document describes the setup and verification of the required tools for the VSD RISC-V Tapeout program.

## Tools Installation

   All the instructions for installation of required tools can be found here:</ins>

### System Information

<img width="848" height="461" alt="Screenshot from 2025-09-20 23-16-21" src="https://github.com/user-attachments/assets/5259e069-cb5b-40f1-9a2f-002ea650f480" />

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

Iverilog comes bundled with the OSS-CAD Suite, but the problem is, it comes with the latest version 13 which isn't regarded as a stable version in Iverilog's documentation
Thus, we have to manually revert back to a stable version.
This is done by deleting all iverilog files that came bundled with OSS-CAD Suite (using the search function might be helpful)

### INSTALLATION:
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

GTKWave too comes bundled with OSS-CAD Suite, but this time with the version 3.4.0 which is stable.
But just to be on the safer side it is recommended to delete the GTKWave files inside the OSS-CAD Suite folder

### INSTALLATION:

```bash
sudo apt-get update
sudo apt install gtkwave
sudo apt-get install libcanberra-gtk-module
```
### TOOL CHECK:
```
 gtkwave -v
```

<img width="1209" height="543" alt="Screenshot from 2025-09-19 22-13-28" src="https://github.com/user-attachments/assets/eba7b2dd-7741-4cf4-838b-835c5d6d6e37" />

### TOOLS
|Tools|Version|
|-----|-------|
|yosys|9.0|
|iverilog|11.0|
|GTKWave|3.3.104|
