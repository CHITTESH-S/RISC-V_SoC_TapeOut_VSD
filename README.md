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

🔧 Gain hands-on experience with RTL, synthesis, physical design, and verification.

🇮🇳 Contribute to India’s semiconductor ecosystem.

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

## 🗓️ Weekly Journey & Checkpoints

Each week is like a **milestone card**:

### 🟢 Week 0 — Environment Setup ✅

🟢 Installed tools and validated presence: yosys -V, iverilog -v, gtkwave --version, openlane --version (where applicable).

🧭 Configured environment variables and PATH entries for reproducibility (example .bashrc/.zshrc snippets included).

🐳 Docker / Container Notes: prepared container image and docker-compose snippets for reproducible flows (OpenLane + PDK in container).

🔁 Backup & snapshot: PDK and critical tool artifacts backed up and hashed for future verification.

### 🟢 Week 1 — RTL Design Basics & Gate-Level Synthesis ✅

✍️ Verilog RTL to Simulation — Wrote modular RTL, created testbenches, simulated with Icarus Verilog, and visualized outputs in GTKWave.

⏱️ Timing & Synthesis — Explored Sky130 .lib timing libraries, performed hierarchical vs flat synthesis, and reused submodules for efficiency.

⚡ Optimizations — Applied Boolean simplification, shift-based multiplications, and pruning of unused logic; compared pre vs post optimization netlist stats in Yosys.

🔗 Gate-Level Verification — Ran GLS on synthesized netlists, understood blocking vs non-blocking assignments, and identified synthesis–simulation mismatches.

🧱 RTL-to-Hardware Mapping — Studied how if-else, case, and loops translate into gates, muxes, and flops; reinforced synthesis-friendly coding practices.

🚀 Milestone Insight — Learned that Verilog = Hardware, synthesis tools are powerful but not magical, and disciplined RTL design is the first big step toward tapeout.

### 🔵 Week 2 —  ⚡ *(Upcoming)*

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

## 🔮 Roadmap & Next Steps

🔁 Week-2: deep dive into synthesis optimization, STA, and gate-level validation.

🏗️ Physical Design: floorplanning, placement & routing, DRC/LVS iterations (OpenLane + Magic).

🧾 Tapeout prep: final sign-off checks, GDSII generation, and submission packaging.

📤 Documentation: weekly logs, reproducible scripts, and final “tapeout cookbook”.

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
