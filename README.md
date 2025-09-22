# Week 0 VSD RISC-V Tapeout Program
This document describes the setup and verification of the required tools for the VSD RISC-V Tapeout program.

## Tools Installation

   All the instructions for installation of required tools can be found here:</ins>

### System Information

<img width="848" height="461" alt="Screenshot from 2025-09-20 23-16-21" src="https://github.com/user-attachments/assets/5259e069-cb5b-40f1-9a2f-002ea650f480" />

### TOOLS INSTALLATION


#### <ins>Yosys Installation</ins>

Download the `oss-cad-suite-linux-x64-20250916.tgz` file from releases page of [OSS-CAD-Suite](https://github.com/YosysHQ/oss-cad-suite-build) repository

```bash
cd ~/Downloads 
# The place the tgz file is downloaded
tar -xvzf oss-cad-suite-linux-x64-20250916.tgz -C ~/
gedit ~/.bashrc
```
```bash
export PATH="$HOME/oss-cad-suite/bin:$PATH" 
# At the end of the file that opened
```
then,
```bash
source ~/.bashrc
```

### TOOL CHECK:
```bash
yosys
license
```
<img width="748" height="595" alt="Screenshot from 2025-09-22 17-40-35" src="https://github.com/user-attachments/assets/563806ae-e09d-48de-abe2-4ffdd658e1e7" />


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
|yosys|0.9|
|iverilog|11.0|
|GTKWave|3.3.104|

## About
Week 0 of the RISV-V Reference SoC Tapeout Program.

For further guidance, refer to [VLSI System Design Labs.](https://www.vlsisystemdesign.com/soc-labs/)
