# 32Bit-ALU_Synthesis

## Aim:

Synthesize 32 Bit ALU design using Constraints and analyse area and Power reports.

## Tool Required:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim)

Synthesis: Genus

### Step 1: Getting Started

Synthesis requires three files as follows,

◦ Liberty Files (.lib)

◦ Verilog/VHDL Files (.v or .vhdl or .vhd)

### Step 2 : Performing Synthesis

The Liberty files are present in the library path,

• The Available technology nodes are 180nm ,90nm and 45nm.

• In the terminal, initialise the tools with the following commands if a new terminal is being
used.

◦ csh

◦ source /cadence/install/cshrc

• The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

• Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist.
            read_libs /cadence/install/FOUNDRY-01/digital/90nm/dig/lib/slow.lib
            read_hdl alu_32bit.v
            elaborate
            syn_generic
            report_area
            syn_map
            report_area
            syn_opt
            report_area 
            report_area > alu_32bit_area.txt
            report_power > alu_32bit_power.txt
            report_area > alu_32bit_cell.txt
            report_gates > alu_32bit_gates.txt
            write_hdl > alu_32bit_netlist.v
            gui_show

#### Synthesis RTL Schematic :
![WhatsApp Image 2024-11-22 at 12 37 48_e0e37b72](https://github.com/user-attachments/assets/1df8f23d-537f-42d0-a202-99471331da31)

#### Area report:
![WhatsApp Image 2024-11-22 at 12 37 48_525b458e](https://github.com/user-attachments/assets/fa9e5484-94c9-49cd-af80-b71a204771da)

#### Power Report:
![WhatsApp Image 2024-11-22 at 12 37 48_a9628af9](https://github.com/user-attachments/assets/3cbeac9d-729e-4672-8367-20e02763cac7)

#### Result: 

The generic netlist of 32 bit ALU  has been created, and area, power reports have been tabulated and generated using Genus.
