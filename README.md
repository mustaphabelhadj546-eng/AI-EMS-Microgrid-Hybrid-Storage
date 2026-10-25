# Intelligent Energy Management System (EMS) for Hybrid Energy Storage Microgrids

## 📌 Overview
This repository contains an advanced **Energy Management System (EMS)** designed for modern microgrids integrating:
* **Photovoltaic (PV) Source** with MPPT control[cite: 4, 5].
* **Hybrid Energy Storage System (HESS)** combining **Li-ion Batteries** and **Supercapacitors (SC)**[cite: 4, 5].
* **Intelligent Optimization** via **Ant Colony Optimization (ACO)**[cite: 4, 6].

This project serves as an **extended development of my Master's Thesis (PFE)**, incorporating enhanced control strategies, improved dynamic load balancing, and extended system topologies.

---

## 🏗️ System Architecture & MATLAB/Simulink Implementation
The entire system is modeled, simulated, and validated using **MATLAB/Simulink**[cite: 7]. The architecture consists of the following key subsystems:

1. **Photovoltaic Source & DC/DC Converter:** Converts solar irradiance into electrical energy, optimized using Maximum Power Point Tracking (MPPT)[cite: 5].
2. **Li-ion Battery Module:** Provides long-term energy storage and stabilizes system voltage through a bidirectional DC/DC converter[cite: 5].
3. **Supercapacitor Module:** Absorbs high-frequency power fluctuations and manages fast transient load demands, protecting the battery from stress[cite: 5].
4. **Intelligent EMS (ACO-Based):** The central control unit that monitors real-time variables ($P_{PV}$, $P_{Load}$, $SOC_{batt}$, $SOC_{cap}$, $V_{bus}$) and dynamically distributes power flows using Ant Colony Optimization[cite: 6, 7].

---

## 📂 Repository Structure
* `/Simulink_Models/` -> Main MATLAB/Simulink simulation files (`.slx`) representing the PV, HESS, and microgrid network.
* `/Controllers/` -> MATLAB scripts and functions implementing the ACO-based EMS and MPPT algorithms.
* `/Results/` -> Simulation performance plots (DC bus stability, battery stress reduction, and efficiency comparisons).
* `README.md` -> Project documentation.

---

## 🚀 Key Objectives & Extensions (Post-PFE)
* **Battery Lifespan Extension:** Minimizing high-frequency cycling on Li-ion batteries by shifting transient power spikes to supercapacitors[cite: 6].
* **DC Bus Voltage Stability:** Maintaining a stable common DC bus voltage under variable solar irradiance and abrupt load changes[cite: 6].
* **Advanced Optimization:** Expanding the classical rule-based approach with heuristic ACO decision-making[cite: 4].

---

## 🛠️ Requirements
* **MATLAB / Simulink** (Recommended version: R2021b or newer)
* Simscape Electrical / Specialized Power Systems toolbox (for power electronics converters and battery/supercapacitor blocks).

---

## 📄 Reference
Based on the Master's Thesis: *"Intelligent Energy Management for a Hybrid Li-ion Battery and Supercapacitor System in Photovoltaic Applications"*[cite: 4].
