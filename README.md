## 🧠 RISC-V SoC Tapeout Journey — VSD Program

<div align="center">

![RISC-V](https://img.shields.io/badge/RISC--V-SoC-orange?style=for-the-badge&logo=riscv)
![VSD Program](https://img.shields.io/badge/VSD-Program-blue?style=for-the-badge)
![Open-Source EDA](https://img.shields.io/badge/EDA-OpenSource-brightgreen?style=for-the-badge)

</div>

Welcome all to my GitHub repo for the **RISC-V SoC Tapeout Program by VSD** — the **master-log** for the tapeout journey. Each week has its own **sub-repo** with detailed labs, scripts, and results.

---

<div align="center">
  
>“From ideas in Verilog to metal on silicon — this is my path through the tapeout flow from documenting every step of my hands-on RISC-V SoC tapeout journey using open-source EDA tools." 

</div>

---

## 🔍 Program Overview

**🎯 Objective:** Learn the complete SoC design flow and achieve a tapeout-ready design.  

**❓ Why:**

- 🔧 Gain hands-on experience with RTL, synthesis, physical design, and verification.

- 🇮🇳 Contribute to India’s semiconductor ecosystem.

📚 Create reproducible documentation for learning and collaboration.

**🖥️ Environment:** Ubuntu 22.04 + open-source EDA toolchain

---

## 🧰 Toolchain Setup (Week 0 Highlights)

> The open-source stack powering this SoC journey:

✅ Icarus Verilog — simulation & testbenches.

✅ GTKWave — waveform visualization.

✅ Yosys — RTL synthesis and optimization.

✅ Ngspice — circuit & mixed-signal simulation (where needed).

✅ Magic — layout editing, DRC, LVS.

✅ OpenLane — automated RTL → GDSII flow using Sky130 PDK.

✅ SkyWater SKY130 PDK — standard-cell & design rules (local or containerized install).

**Achievements in Week 0:**  

🟢 Installed tools and validated presence: yosys -V, iverilog -v, gtkwave --version, openlane --version (where applicable).

🧭 Configured environment variables and PATH entries for reproducibility (example .bashrc/.zshrc snippets included).

🐳 Docker / Container Notes: prepared container image and docker-compose snippets for reproducible flows (OpenLane + PDK in container). 

---

## 📊 Progress Level

<div align="center">

![Week 0](https://img.shields.io/badge/Week%200-✅%20Done-green?style=for-the-badge)
![Week 1](https://img.shields.io/badge/Week%201-✅%20Done-green?style=for-the-badge)
![Week 2](https://img.shields.io/badge/Week%202-✅%20Done-green?style=for-the-badge)
![Week 3](https://img.shields.io/badge/Week%203-✅%20Done-green?style=for-the-badge)
![Week 4](https://img.shields.io/badge/Week%204-✅%20Done-green?style=for-the-badge)
![Week 5](https://img.shields.io/badge/Week%205-✅%20Done-green?style=for-the-badge)
![Week 6](https://img.shields.io/badge/Week%206-✅%20Done-green?style=for-the-badge)
![Week 7](https://img.shields.io/badge/Week%207-✅%20Done-green?style=for-the-badge)
![Week 8](https://img.shields.io/badge/Week%208-✅%20Done-green?style=for-the-badge)

</div>

---

## 🗓️ Weekly Journey & Checkpoints

Each week is like a **milestone card**:

### 🟢 Week 0 — Environment Setup ✅

🛠️ Toolchain Setup & Validation — Installed and verified Yosys, Icarus Verilog, GTKWave, Ngspice, Magic, and OpenLane on Ubuntu 22.04 for RTL-to-GDSII flow.

🐳 Environment Configuration — Configured PATH variables, dependencies, and system environment ensuring reproducible and stable tool execution.

🧪 Initial Simulation & Synthesis — Ran sample RTL simulations (Icarus Verilog + GTKWave) and performed basic synthesis using Yosys to validate setup.

📂 Version Control & Repository Setup — Initialized and structured GitHub repositories for week-wise documentation and project tracking.

🧠 SoC Design Flow Understanding — Learned complete RISC-V SoC flow from C model (O0) → RTL (O2) → SoC integration (O3) → GDSII (O4).

🔄 Design Consistency Principle — Understood functional equivalence (O0 = O1 = O2 = O3 = O4) ensuring correctness across all abstraction levels.

🚀 Milestone Insight — Established a fully functional VLSI design environment and built strong foundation in end-to-end ASIC design flow.

### 🟢 Week 1 — RTL Design Basics & Gate-Level Synthesis ✅

✍️ RTL Design & Testbench Development — Wrote synthesizable Verilog RTL modules and created structured testbenches (stimulus, UUT, observer) for functional verification.

🧪 Simulation & Waveform Analysis — Performed RTL simulation using Icarus Verilog and analyzed signal behavior via GTKWave.

⚙️ Logic Synthesis (Yosys + Sky130) — Converted RTL into gate-level netlists using Yosys with Sky130 standard-cell libraries (.lib).

📚 Timing Library Understanding — Explored Liberty (.lib) files including timing arcs, setup/hold constraints, PVT corners, and power/area trade-offs.

🏗️ Hierarchical vs Flat Synthesis — Compared modular (hierarchical) and global (flat) synthesis flows for optimization vs readability.

🔁 Submodule & IP Reuse Strategy — Practiced submodule synthesis enabling scalable and reusable hardware design.

⚡ RTL & Logic Optimizations — Applied Boolean simplification, constant propagation, shift-based multiplications, and pruning of unused logic.

🧠 Sequential Logic & Flip-Flops — Studied flip-flop coding styles (sync/async reset, enable) and their impact on timing and stability.

🔍 Gate-Level Simulation (GLS) — Verified synthesized netlists using GLS flow to ensure RTL–netlist functional equivalence.

⚠️ Coding Discipline & Mismatch Debugging — Identified synthesis–simulation mismatches caused by improper sensitivity lists, blocking/non-blocking misuse, and non-synthesizable constructs.

🔀 Hardware Mapping of RTL Constructs — Analyzed how if-else, case, loops, and generate blocks translate into muxes, combinational logic, and sequential elements.

🚀 Milestone Insight — Established strong foundation in RTL design, timing-aware synthesis, and hardware mapping, realizing that Verilog directly defines physical hardware behavior.

### 🟢 Week 2 — SoC Fundamentals & Functional Modelling (VSDBabySoC) ✅

🧠 SoC Architecture Understanding — Studied System-on-Chip fundamentals, including CPU, memory, interconnects, peripherals, and power management trade-offs.

🍼 VSDBabySoC System Analysis — Analyzed PLL → RISC-V (RVMYTH) → DAC architecture, understanding complete data flow from clock generation to analog output.

⚡ Mixed-Signal Design Concepts — Explored digital–analog interaction, DAC behavior, and system-level signal flow in mixed-signal SoC design.

🔁 TL-Verilog to Verilog Conversion — Converted RVMYTH core from TL-Verilog to synthesizable Verilog using SandPiper-SaaS.

🧪 Functional Simulation Setup — Performed pre-synthesis simulation using Icarus Verilog for complete SoC design validation.

📊 Waveform Analysis (GTKWave) — Analyzed key signals (clk, reset, pll_locked, pc, RV_TO_DAC, OUT) to verify correct system behavior.

🔍 Testbench-Driven Verification — Used structured testbench to validate CPU execution, DAC interfacing, and system sequencing.

⏱️ Startup & Clock Sequencing — Verified PLL lock behavior and reset synchronization, ensuring proper system initialization.

📈 Signal-Level Validation — Observed DAC staircase output and confirmed correct mapping of digital CPU output to analog behavior.

🧩 Verification Methodology — Applied functional modelling principles to detect bugs early before synthesis and physical design stages.

🚀 Milestone Insight — Established strong understanding of SoC-level integration, mixed-signal behavior, and pre-synthesis functional verification, bridging RTL design with real system operation.

### 🟢 Week 3 — Post-Synthesis Validation & Static Timing Analysis (GLS + STA) ✅

🧩 Gate-Level Netlist Generation — Synthesized RTL into gate-level netlist using Yosys, mapping design to standard-cell libraries.

🧪 Post-Synthesis Simulation (GLS) — Verified synthesized netlist functionality using Icarus Verilog to ensure no logic mismatches after synthesis.

📊 Waveform Comparison (GTKWave) — Compared pre-synthesis and post-synthesis waveforms using GTKWave to validate identical system behavior.

🔍 RTL vs Netlist Equivalence — Confirmed that synthesis preserved functionality across all test vectors with no mismatches.

⚙️ Synthesis Optimization Awareness — Applied optimization steps (opt, abc, dfflibmap) and analyzed impact on gate-level structure and performance.

🧠 Static Timing Analysis Fundamentals — Learned core STA concepts including setup/hold checks, timing paths, clock domains, and delay modeling.

🧮 Slack Analysis (WNS/TNS) — Evaluated timing health using Worst Negative Slack (WNS) and Total Negative Slack (TNS) metrics.

⏰ Clock & Constraint Modeling — Defined clocks, generated clocks (PLL), uncertainties, and I/O delays using SDC constraints.

🔗 Timing Path Analysis — Explored different path types (reg→reg, input→reg, reg→output) and identified critical paths affecting performance.

🛠️ OpenSTA Timing Verification — Performed STA using OpenSTA to generate timing reports and validate timing closure.

🌡️ PVT Corner Analysis — Analyzed timing across multiple process-voltage-temperature corners to ensure robust design performance.

⚠️ Timing Violation Debugging — Identified causes of setup/hold violations and explored fixes like buffering, retiming, and cell sizing.

📉 Parasitic Awareness (SPEF) — Understood impact of interconnect delays and capacitance on timing through parasitic-aware analysis.

🚀 Milestone Insight — Achieved full post-synthesis validation by ensuring both functional correctness and timing closure, bridging the gap between RTL design and silicon-ready implementation.

---

## 🙏 Acknowledgments

🤝 VSD Team & Kunal Ghosh — mentoring & guidance.

🌐 Efabless & RISC-V International — enabling collaborative tapeouts.

🛠️ Open-source EDA community — tools, tutorials, and example flows.

👥 Peers & instructors — debugging help & design reviews.

---

👉 **Week-0 Repository Link:** https://github.com/CHITTESH-S/Week-0_RISC-V_SoC_TapeOut

👉 **Week-1 Repository Link:** https://github.com/CHITTESH-S/Week-1_RISC-V_SoC_TapeOut

👉 **Week-2 Repository Link:** https://github.com/CHITTESH-S/Week-2_RISC-V_SoC_TapeOut

👉 **Week-3 Repository Link:** https://github.com/CHITTESH-S/Week-3_RISC-V_SoC_TapeOut

👉 **Week-4 Repository Link:** https://github.com/CHITTESH-S/Week-4_RISC-V_SoC_TapeOut

👉 **Week-5 Repository Link:** https://github.com/CHITTESH-S/Week-5_RISC-V_SoC_TapeOut

👉 **Week-6 Repository Link:** https://github.com/CHITTESH-S/Week-6_RISC-V_SoC_TapeOut

👉 **Week-7 Repository Link:** https://github.com/CHITTESH-S/Week-7_RISC-V_SoC_TapeOut

👉 **Week-8 Repository Link:** https://github.com/CHITTESH-S/Week-8_RISC-V_SoC_TapeOut

> *“Designing a chip is a journey — every checkpoint counts, every reflection matters, and each milestone brings you closer to tapeout.”*

👨‍💻 **Contributor:** [Chittesh S](https://github.com/CHITTESH-S)
