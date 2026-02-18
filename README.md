# Roam-Robotic_Welding_SD

## Overview

This repository contains the public-facing website and non-confidential materials for the **ROAM / Rapid Prototyping Lab (RPL) — Robotic Welding Senior Design Project (Fall 2025 – Spring 2026)** at **Colorado State University**.

The goal of this project is to develop a functional robotic welding system integrating a **UFactory xArm 850** with welding hardware and sensing. The system will be capable of performing automated weld paths with repeatability, safety, and process parameter logging.

## Repository Structure
* 📁 ROAM-Robotic_Welding_Senior_Design
  * /docs/ → GitHub Pages source (Jekyll + Minimal Mistakes)
  * README.md → Project overview and repository policy
  * LICENSE → License file

> ⚠️ *Do not store proprietary vendor files or sensitive information in this repo.*

## Intellectual Property & Confidentiality

This repository contains materials generated as part of the Colorado State University
Senior Design Project sponsored by **Roam Electric**.

All intellectual property developed for this project is assigned to Roam Electric per the
IP agreement signed by team members.

Some elements of the project may be confidential under NDA. Do not upload or disclose
ROAM Confidential Information (designs, data, research, or business details) without
written permission from ROAM.

## Public and Private Repositories

This public repository contains website content and non-confidential project materials.

- **Public repository**: https://github.com/Bgujer/ROAM-Robotic_Welding_Senior_Design
- **Private companion repository (authorized collaborators only)**: https://github.com/Bgujer/Roam-Robotic_Welding_SD

Confidential project files (including development CAD, code, analysis, and internal documentation) are maintained in the private repository.

## Hardware Used

| **Component** | **Model** | 

| Robotic Arm | **UFactory xArm 850** |\
| Welder | **Miller MillerMatic Pro** |\
| End Effector | Custom mount & torch adapter |\
| Safety Hardware | Welding light curtains, emergency stops |

## Software Stack

| **Category** | **Tool / Framework** |

| IDE / Control | UFactory Studio, Python, ROS |\
| Path Planning | Point-to-point w/ python-guided paths (future development needed for post-processing)|\
| Version Control | Git + GitHub Projects |


## 👥 Contributors

| **Name** | **Role** | **Responsibilities** |

| Ben Gujer | Controls Focus | Welder Integration, Safety |\
| Dexter Shafer-White | Controls Focus | xArm control scripts, path planning logic |\
| Gage Steinke | Mechanical Focus | Welder interface, torch mounting system |\
| Greg Hider | Mechanical Focus | Welder interface, supporting mounting systems |\
| Tamsin Izard | Project Manager | Timeline, documentation, meeting coordination |\
| John Mizia (RPL) | Faculty Advisor | Technical oversight, weekly reviews |\
| Bryan Willson (Energy Institute) | Sponsor | Technical oversight, weekly reviews |\
| Wesley Holmes (ROAM) | Masters Thesis | Touchpoint for ROAM, biweekly reviews |
