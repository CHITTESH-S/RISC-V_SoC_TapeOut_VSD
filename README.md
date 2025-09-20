## 🧠 RISC-V SoC Tapeout Journey — VSD Program

> From RTL to GDSII, documenting every step of my hands-on RISC-V SoC tapeout journey using open-source EDA tools.  
> This repository serves as the **master-log**, while each week’s detailed work has its own dedicated sub-repo.

---

## 🔍 Program Overview

**🎯Objective:** Learn the complete SoC design flow and achieve a tapeout-ready design.  

**Why:**  
- Gain hands-on experience with RTL, synthesis, physical design, and verification.  
- Contribute to India’s semiconductor ecosystem.  
- Document all stages for reproducibility and learning.  

**Environment:** Ubuntu 22.04 + Open-source EDA toolchain.

---

## 🧰 Toolchain Setup (Week 0 Highlights)

> The open-source stack powering this SoC journey:

- 🟢 **Yosys** — RTL synthesis  
- 🟢 **Icarus Verilog** — Simulation & testbenches  
- 🟢 **GTKWave** — Waveform visualization  
- 🟢 **Ngspice** — Circuit & mixed-signal simulation  
- 🟢 **Magic** — Layout, DRC, LVS  
- 🟢 **OpenLane** — RTL → GDSII full flow  

**Achievements in Week 0:**  
- Installed all tools and configured environment variables.  
- Verified sample RTL, simulation, and synthesis runs.  
- Learned the importance of version consistency and paths.  

---

## 🗓️ Weekly Journey & Checkpoints

Each week is like a **milestone card**:

### 🟢 Week 0 — Environment Setup ✅
- Installed all tools and dependencies  
- Sample RTL simulation → waveform checks  
- Basic OpenLane RTL → GDSII flow validation  

### 🟡 Week 1 — RTL Design Basics ✍️ *(Current)*
- Writing modular Verilog designs  
- Creating testbenches and simulating functionality  
- Preparing modules for synthesis  

### 🔵 Week 2 — Gate-Level Synthesis ⚡ *(Upcoming)*
- Convert RTL → gate-level netlist with Yosys  
- Run gate-level simulation  
- Compare RTL vs synthesized behavior 

---

## 🔮 Roadmap & Next Steps

- Complete **Week 1 RTL modules** and testbench verification.  
- Move to **Week 2 synthesis & gate-level simulation**.  
- Start documenting **physical design steps** and timing constraints.  
- Maintain weekly reflections and update the master log.  

---

## 🙏 Acknowledgments

- **VSD Team & Kunal Ghosh** — mentoring & guidance  
- **Efabless & RISC-V International** — enabling collaborative tapeouts  
- **Open-source EDA community** — providing tools & tutorials  
- **Peers & instructors** — helping debug & conceptualize  

---

👨‍💻 **Contributor:** [Chittesh S](https://github.com/CHITTESH-S)

> *“Designing a chip is a journey — every checkpoint counts, every reflection matters, and each milestone brings you closer to tapeout.”*
