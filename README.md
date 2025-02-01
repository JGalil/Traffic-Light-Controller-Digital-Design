# Traffic-Light-Controller-Digital-Design

#  Traffic Light Controller

##  Overview  
This project implements a **Traffic Light Controller** using **SystemVerilog**. The system controls a **multi-state traffic signal**, simulates traffic light behavior with **state transitions**, and ensures **safety and efficiency** in intersection management.

 **Part 1** – Initial traffic light state machine implementation.  
 **Part 2** – Improved logic with additional constraints and edge cases.  

##  Features  
- **Finite State Machine (FSM) Design** – Implements a traffic signal system with multiple states.  
- **State Transitions** – Controls light switching between `Green`, `Yellow`, and `Red`.  
- **Pedestrian Signals** – Incorporates crosswalk light control for pedestrians.  
- **Clocked Synchronous Operation** – Uses `posedge clk` for state updates.  
- **Glitch-Free Output** – Ensures stable transitions using `always_comb` logic.  

---

##  File Structure  
### **Part 1**  
| File | Description |  
|------|------------|  
| `light_package.sv` | Defines light states and related constants. |  
| `traffic_light_controller1.sv` | Implements the initial traffic light state machine. |  
| `lab3_part1_results.txt` | Output results from waveform simulations. |  

### **Part 2**  
| File | Description |  
|------|------------|  
| `traffic_light_controller_part2_starter.sv` | Updated traffic light controller logic with fixes. |  
| `Lab3Part2Results.txt` | Output results from Part 2 simulations. |  

### **Additional Files**  
| File | Description |  
|------|------------|  
| `Lab3.pdf` | Lab report detailing the implementation and challenges. |  

---

##  Simulation & Testing  
### **Requirements**  
- **SystemVerilog Compiler** (e.g., ModelSim, QuestaSim, Xilinx Vivado)  
- **Testbench Environment** for verifying behavior  

### **Running the Simulation**  
1️⃣ **Compile the SystemVerilog files**  
```sh
vlog light_package.sv traffic_light_controller1.sv traffic_light_controller_part2_starter.sv
```  
2️⃣ **Run the simulation**  
```sh
vsim -c -do "run -all" traffic_light_controller1
```  
3️⃣ **Check the waveform output** or **verify text outputs** (`lab3_part1_results.txt` and `Lab3Part2Results.txt`).  

---

## 📌 Issues Encountered  
### **Part 1**  
- **Infinite loop issue** due to incorrect state logic.  
- Fixed by **simplifying the state transitions** and removing unnecessary complexity.  

### **Part 2**  
- **Mismatch in initial output** due to missing reset condition.  
- Resolved by adding **`posedge reset`** in `always_comb` block.  

---

## 👨‍💻 Contributors  
- **Joachim Galil**  
- **Sean King**   
