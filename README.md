# SUB-FOLD  
**SERVIR Uncertainty-Based Forest Loss and Disturbance Alert System**

This repository serves as the central hub for documentation, system setup guidance, and references to associated components of the SUB-FOLD system. It does not contain active code, but instead provides context and instructions for working with the full ensemble system.

---

## Project Overview

SUB-FOLD is a modular system designed to monitor and validate forest loss using an ensemble of forest disturbance alerts from both optical and SAR-based sensors. It integrates:

- **Probabilistic forest change detection** using multiple satellite-based alert products.
- **Stratified random sampling** across levels of sensor agreement.
- **Interpreter validation** via high-resolution NICFI and Landsat time series imagery.
- **Post-processing and modeling**, including aggregation, confidence assessment, and machine learning integration.

The system supports scalable application in regions like Southeast Asia and can be adapted to other areas with appropriate sensor inputs and training data.

---

## Application Context

In Southeast Asia (Cambodia, Laos PDR, Vietnam), SUB-FOLD has been applied to:

- Generate **agreement-based strata** from five disturbance products:
  - **Optical**: GLAD Alerts, GLAD Annual Forest Map, LandTrendr  
  - **SAR**: SERVIR SAR Alerts (continuous), TropiSCO Alerts  
- Define strata ranging from **no alerts** to **cross-sensor agreement** to capture uncertainty and maximize disagreement.
- Validate outputs using **TimeSync Plus Online (TSPO)** and interpreter-labeled forest loss probabilities.

The ensemble model produces forest loss probability maps for the last 3, 6, and 12 months from a selected start date.

---

## Linked Repositories

| Component                         | Description                                              | Link        |
|----------------------------------|----------------------------------------------------------|-------------|
| **GEE Disturbance Algorithms** | Code for change detection and sample generation | [repo link](https://github.com/mckenziesime/SUB-FOLD-GEEScripts) |
| **TSPO Interface & Database** | Web interface and database for interpreter input | [repo link](https://github.com/eMapR/TSPO) |
| **Processing Validated TSPO Database** | Scripts to process interpreter responses | [repo link](https://github.com/mckenziesime/SUB-FOLD-DB-Processing) |

---

## System Workflow Summary

1. **Geospatial Model Development**
   - Combine forest disturbance alerts from optical and SAR products.
   - Assign per-product confidence levels (e.g., no change, low/high confidence).
   - Group into 6 final strata based on intra- and inter-sensor agreement.

2. **Random Sampling & Database Setup**
   - Perform stratified random sampling across agreement strata.
   - Structure and populate the validation database.

3. **Validation with TSPO**
   - Human interpreters use TSPO to label sample points.
   - Review combines high-resolution NICFI and Landsat time series for context.
   - Label each point with forest loss probability.

4. **Model Evaluation & Post-Processing**
   - Compare model predictions with interpreter input.
   - Assess model performance based on agreement and uncertainty.
   - Generate ensemble output maps showing forest loss probability.

---

## Notes

- This repository is for **documentation only**.
- To use the full SUB-FOLD system, please clone and explore the linked repositories above.
- If you find an issue or want to contribute, feel free to open a [GitHub issue](https://github.com/) or submit a pull request.

---

## Citation / Acknowledgment

If you use SUB-FOLD in your work, please cite SERVIR and acknowledge contributions from the development teams supporting the Southeast Asia forest monitoring efforts.

