# SUB-FOLD
**SERVIR Uncertainty-Based Forest Loss and Disturbance Alert System**

This repository serves as a central hub for documentation, setup instructions, and links to related components of the SUB-FOLD system. It does not contain active code, but instead provides guidance for setting up and coordinating the system.

---

## 🔗 Linked Repositories

| Component | Description | Link |
|----------|-------------|------|
| **GEE Disturbance Algorithms** | Code for change detection and sample generation | [repo link](https://github.com/mckenziesime/SUB-FOLD-GEEScripts) |
| **TSPO Interface & Database** | Web interface and database for interpreter input | [repo link](https://github.com/eMapR/TSPO) |
| **Processing Validated TSPO Database** | Scripts to process interpreter responses | [repo link](https://github.com/mckenziesime/SUB-FOLD-DB-Processing) |

---

## 📂 Setup Instructions

To get started, see the `setup/` folder:

- [`local_setup.md`](https://github.com/eMapR/TSPO): for installing the TSPO interface and setting up the local database.
- [`gee_setup.md`](setup/gee_setup.md): for running analysis in Google Earth Engine.

---

## 🧭 Project Overview

The SUB-FOLD system enables uncertainty-based interpretation and integration of forest disturbance data from various sources. It combines:

- Probabilistic forest change detection
- Manual interpreter input using high-resolution imagery
- Post-processing for aggregation and validation
- Integration with machine learning models

---

## 📌 Notes

- This repo is documentation-only. Clone the linked repos to work on specific components.
- Feel free to submit issues or pull requests for improvements to documentation.
