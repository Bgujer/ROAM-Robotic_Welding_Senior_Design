# Roam-Robotic_Welding_SD

## Overview

This repository contains documentation, source code, CAD models, simulation data, and test results for the **ROAM / Rapid Prototyping Lab (RPL) — Robotic Welding Senior Design Project (Fall 2025 – Spring 2026)** at **Colorado State University**.

The goal of this project is to develop a functional robotic welding system integrating a **UFactory xArm 850** with welding hardware and sensing. The system will be capable of performing automated weld paths with repeatability, safety, and process parameter logging.

---

## Repository Structure
* 📁 Roam-Robotic_Welding_SD
  * /cad/ → Final and working CAD assemblies & components
  * /code/ → Controller scripts, ROS nodes, automation logic
  * /documentation/ → Meeting notes, test reports, safety docs
  * /analysis/ → Simulation results & weld-path planning
  * README.md → You're reading it!

> ⚠️ *Do not store proprietary vendor files or sensitive information in this repo.*

---

## Hardware Used

| Component | Model | 

| Robotic Arm | **UFactory xArm 850** |\
| Welder | TBD (MIG) |\
| End Effector | Custom mount & torch adapter |\
| Safety Hardware | Welding light curtains, emergency stops |

---

## Software Stack

| Category | Tool / Framework |\
| IDE / Control | UFactory Studio, Python, ROS |\
| Path Planning | tbd (Post-Processor)|
| Version Control | Git + GitHub Projects |

## Getting Started

### Clone the repo

```git clone https://github.com/bgujer/Roam-Robotic_Welding_SD.git cd Roam-Robotic_Welding_SD ```

## 👥 Contributors

| Name | Role | Responsibilities |\

| Ben Gujer | Controls Focus | Welder Integration, Safety |\
| Dexter Shafer-White | Controls Focus | xArm control scripts, path planning logic |\
| Gage Steinke | Mechanical Focus | Welder interface, torch mounting system |\
| Greg Hider | Mechanical Focus | Welder interface, supporting mounting systems |\
| Tamsin Izard | Project Manager | Timeline, documentation, meeting coordination |\
| John Mizia (RPL) | Faculty Advisor | Technical oversight, weekly reviews |\
| Bryan Willson (Energy Institute) | Sponsor | Technical oversight, weekly reviews |\
| Wesley Holmes (ROAM) | Masters Thesis | Touchpoint for ROAM, biweekly reviews |\
