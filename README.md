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

---

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

---

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

---

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

### 🟢 Week 4 — CMOS Circuit Design & SPICE Simulation (Sky130 PDK) ✅

🧠 MOSFET Device Understanding — Explored NMOS and PMOS characteristics using Ngspice, analyzing current–voltage behavior across different biasing regions.

📊 Id–Vds Characteristics (NMOS) — Studied linear and saturation regions, identified knee point, and understood channel-length modulation effects.

🔍 Threshold Voltage Extraction (Vth) — Determined Vth using Id–Vgs analysis and linked it to device switching behavior.

🔁 CMOS Inverter Design — Built and simulated a CMOS inverter using Sky130 PDK device models.

📈 Voltage Transfer Characteristics (VTC) — Plotted Vout vs Vin to identify switching threshold (Vm) and analyze inverter gain.

⚖️ Transistor Sizing Insight — Understood how PMOS/NMOS W/L ratio affects switching point, symmetry, and performance.

⏱️ Transient Switching Analysis — Measured propagation delays (tPLH, tPHL) and rise/fall times using pulse inputs.

⚡ Delay vs Load Relationship — Analyzed how capacitive load and transistor strength influence switching speed.

🔊 Noise Margin Analysis — Calculated VOL, VOH, VIL, VIH and derived NML/NMH to evaluate circuit robustness.

🛡️ Robustness & Stability — Studied how inverter design ensures reliable logic levels in presence of noise.

🔋 Power Supply Variation Study — Observed impact of VDD scaling on switching threshold, delay, and noise margins.

🔄 Device Variation Analysis — Explored effects of W/L ratio changes on performance, delay, and power.

📉 Design Trade-offs — Understood trade-offs between speed, power, and noise immunity in CMOS circuits.

🧾 SPICE-Based Modelling — Gained hands-on experience writing netlists, running simulations, and extracting results.

📊 Data Visualization & Interpretation — Generated plots (Id–Vds, VTC, transient waveforms) and correlated them with device physics.

🚀 Milestone Insight — Developed a strong foundation in transistor-level design and analysis, understanding how device physics translates into circuit behavior—an essential step toward full-chip physical design and tapeout.

---

### 🟢 Week 5 — OpenROAD Flow, Floorplanning & Placement (Physical Design) ✅

🛠️ OpenROAD Environment Setup — Installed and configured OpenROAD flow, enabling full RTL-to-GDSII backend automation.

🔧 Build & Debugging Skills — Resolved compilation issues (CMake conflicts, missing dependencies) and successfully built the OpenROAD toolchain locally.

⚙️ Toolchain Integration — Understood integration of key tools: Yosys (synthesis), OpenSTA (timing), and Triton tools (physical implementation).

📐 Floorplanning Fundamentals — Learned how die area, core area, aspect ratio, and utilization are defined to create the physical layout foundation.

📍 Standard Cell Placement — Executed placement stage where synthesized cells are optimally arranged within the core to minimize wirelength and timing delays.

🔄 RTL-to-Layout Mapping — Visualized how logical netlists are transformed into geometric layouts using LEF/DEF and OpenDB formats.

📊 Flow Execution (ORFS) — Ran complete OpenROAD Flow Scripts (make) to automate synthesis → floorplan → placement stages.

🖼️ Layout Visualization (GUI) — Used OpenROAD GUI to inspect core boundaries, cell placement, and timing metrics visually.

📁 Design Data Understanding — Explored physical design file formats: DEF (layout), LEF (library), LIB (timing), ODB (database).

⏱️ Timing Awareness in Physical Stage — Observed slack and timing reports during placement, linking physical layout with timing performance.

🧩 Configuration Management — Modified design parameters (clock, constraints, RTL files) within flow configuration for successful runs.

🔍 Backend Flow Insight — Understood intermediate outputs (logs/, reports/, results/) and their role in debugging and analysis.

⚡ Automation Understanding — Learned how OpenROAD automates complex backend stages like floorplan and placement with minimal manual intervention.

🚀 Transition to Physical Design — Shifted from circuit-level and RTL design to full-chip physical realization and layout generation.

📈 Scalability Insight — Understood how the same flow scales from small designs (GCD) to full SoCs.

🚀 Milestone Insight — Achieved hands-on experience in physical design flow setup and execution, understanding how digital logic is physically arranged on silicon—marking a crucial step toward complete chip tapeout.

---

### 🟢 Week 6 — Full RTL-to-GDSII Physical Design Flow (OpenLANE + Sky130) ✅

🧠 Physical Design Workflow Mastery — Executed the complete RTL-to-GDSII flow using OpenLANE, gaining hands-on experience across synthesis, floorplanning, placement, CTS, routing, and sign-off stages.

🏭 Sky130 PDK Utilization — Worked extensively with Sky130 PDK, understanding real fabrication constraints, design rules, and layout requirements.

🔄 RTL to Layout Transformation — Observed how RTL descriptions are converted into fully placed and routed layouts, bridging the gap between logical design and physical silicon implementation.

📐 Floorplanning & Placement Analysis — Explored core utilization, aspect ratio, and cell placement strategies, analyzing good vs bad floorplans and their impact on performance and congestion.

🔬 Custom Standard Cell Design — Designed and characterized a standard cell using Magic VLSI and Ngspice, linking device-level design with full-chip integration.

⏱️ Timing Analysis & Clock Tree Understanding — Performed pre-layout STA using OpenSTA, and studied clock tree synthesis (CTS) impact on skew, latency, and timing closure.

🛣️ Routing & Physical Connectivity — Completed global and detailed routing using TritonRoute, ensuring proper interconnections and signal integrity.

🧪 DRC & LVS Verification — Verified layout correctness through Design Rule Check (DRC) and Layout vs Schematic (LVS), ensuring fabrication-ready design quality.

📊 Design Trade-off Analysis — Understood the relationship between area, power, and timing, and how physical design decisions affect overall chip performance.

🖥️ VDI-Based Environment Setup — Successfully configured and utilized a pre-built virtual environment with all EDA tools, enabling smooth execution of complex physical design flows.

🔗 End-to-End Integration Insight — Connected all previous weeks (RTL, synthesis, STA, CMOS design) into a unified physical design workflow, achieving a holistic understanding of chip design.

🚀 Milestone Insight — Achieved a complete understanding of how a design moves from RTL to a verified, fabrication-ready layout, marking a major step toward real-world ASIC implementation.

---

### 🟢 Week 7 — VSDBabySoC RTL-to-GDSII Automation (OpenROAD Flow) ✅

🧠 End-to-End SoC Implementation — Executed complete RTL-to-GDSII flow for VSDBabySoC using OpenROAD and OpenROAD-flow-scripts.

📦 Design Integration — Integrated digital RISC-V core with analog macros (DAC, PLL) using Sky130 HD PDK.

🔨 Logic Synthesis (Yosys) — Converted RTL to optimized gate-level netlist and analyzed area, cell count, and initial timing.

📐 Floorplanning Strategy — Defined die/core area, optimized macro placement, and designed power distribution (VDD/VSS rings & straps).

🎯 Placement Optimization — Performed global + detailed placement ensuring legal cell placement and balanced utilization (~55–65%).

📊 Congestion & Density Analysis — Evaluated routing congestion (RUDY), pin density, and placement heatmaps to identify bottlenecks.

⚡ IR Drop Analysis — Investigated power integrity and identified voltage drop hotspots across the chip.

⏰ Clock Tree Synthesis (CTS) — Built balanced clock network with optimized skew (<1 ns) and controlled latency.

🛣️ Routing Completion — Achieved full signal routing using TritonRoute with 0 DRC violations.

🔬 Parasitic Extraction (SPEF) — Generated post-route SPEF capturing RC effects for accurate timing analysis.

📊 Design Metrics Evaluation — Verified ~30K standard cells, full connectivity, and timing closure.

🖼️ Layout Visualization — Inspected floorplan, placement, CTS, and routing using OpenROAD GUI.

🔄 Iterative Optimization Insight — Learned impact of floorplan, placement, and routing on timing, power, and congestion.

🚀 Milestone Achievement — Successfully transformed RTL into a fabrication-ready GDSII layout, gaining real-world ASIC design flow experience.

---

🟢 Week 8 — Post-Route STA & PVT Corner Analysis (VSDBabySoC) ✅

🧠 Post-Route Timing Analysis — Performed detailed STA using OpenSTA with back-annotated parasitics.

🔗 SPEF Back-Annotation — Incorporated extracted RC data to analyze real interconnect delays and timing impact.

📊 Timing Graph Exploration — Analyzed timing paths, slack distribution, and critical paths in the timing graph.

⏱️ Setup & Hold Verification — Evaluated setup/hold constraints ensuring no violations in post-route design.

📉 Slack Analysis — Studied WNS (Worst Negative Slack) and TNS (Total Negative Slack) across timing paths.

🌡️ PVT Corner Analysis — Verified timing across multiple Process, Voltage, Temperature (PVT) conditions.

⚙️ Corner-Based Behavior

- 🐢 Slow Corner: Worst-case delay (low VDD, high temperature)
- ⚡ Fast Corner: Best-case delay (high VDD, low temperature)
- 🎯 Typical Corner: Nominal operating condition

🔍 Critical Path Identification — Located longest delay paths affecting timing closure.

⚡ Parasitic Impact Understanding — Observed how resistance & capacitance increase delay and affect signal integrity.

🔄 Timing Variation Study — Compared timing shifts across corners to ensure robust design.

📊 Report Analysis — Interpreted STA reports, path delays, clock skew, and uncertainties.

🛡️ Design Robustness Validation — Ensured chip operates reliably under real-world variations.

📈 Signoff-Level Understanding — Learned importance of post-route STA in final tapeout validation.

🚀 Final Milestone Insight — Bridged physical design and timing signoff, achieving a complete understanding of silicon-level timing verification.

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

> *“Designing a chip is a journey — every checkpoint counts, every reflection matters, and each milestone brings you closer to tapeout.”*

👨‍💻 **Contributor:** [Chittesh S](https://github.com/CHITTESH-S)
