<div align="center">

# ICU Mechanical Ventilator Adjustment

### A Three-Phase Clinical Decision Framework Based on Multivariate Time-Series Analysis

<br>

A robust deep-learning framework designed to model and predict intensive care unit (ICU) mechanical ventilator adjustment workflows through multivariate time-series analysis.

<br>

[Overview](#overview) · [Architecture](#research-framework) · [Methodology & Data](#methodology--data-governance) · [Phase Repositories](#phase-repositories) · [Thesis & Citation](#master-thesis--citation)

</div>

---

## Overview

<table align="center">
  <tr>
    <td align="center" width="33%">
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-1">
        <kbd>⚡ Phase 1: Requirement</kbd>
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-1">
        <kbd>🔄 Phase 2-1: Direction</kbd>
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-2">
        <kbd>📊 Phase 2-2: Recommendation</kbd>
      </a>
    </td>
  </tr>
</table>

This research establishes a sequential decision pipeline for mechanical ventilation management, leveraging high-frequency ICU telemetry and advanced sequence modeling.

---

## Research Scope & Specifications

<table>
  <tr>
    <td width="28%"><strong>Clinical Domain</strong></td>
    <td>Intensive Care Unit (ICU)</td>
  </tr>
  <tr>
    <td><strong>Research Topic</strong></td>
    <td>Mechanical Ventilator Parameter Adjustment</td>
  </tr>
  <tr>
    <td><strong>Data Structure</strong></td>
    <td>Multivariate Ventilator Time-Series</td>
  </tr>
  <tr>
    <td><strong>Sequence Models</strong></td>
    <td>Long Short-Term Memory (LSTM) & Gated Recurrent Unit (GRU)</td>
  </tr>
  <tr>
    <td><strong>Optimization</strong></td>
    <td>Bayesian Hyperparameter Optimization (Tree-structured Parzen Estimator)</td>
  </tr>
  <tr>
    <td><strong>Institutional Approval</strong></td>
    <td>KMUHIRB-E(I)-20240420</td>
  </tr>
</table>

---

## Research Framework

<p align="center">
  <a href="assets/figures/framework/research-framework.jpg">
    <img src="assets/figures/framework/research-framework.jpg" width="760" alt="Research Framework">
  </a>
</p>
<p align="center">
  <sub>Systematic pipeline covering temporal data preprocessing, sliding-window tensor generation, and three-phase decision modeling.</sub>
</p>

---

## Methodology & Data Governance

<details>
<summary><b>📂 Click to Expand: Cohort Profile, Data Integrity & Quality Statistics</b></summary>

<br>

The retrospective dataset comprises high-frequency telemetry and setting records from **355 patients** undergoing invasive mechanical ventilation, totaling **11,298,127 minutes** of observations.

| Category | Metric Description | Quantitative Value |
| :--- | :--- | :--- |
| **Cohort Scale** | Total Patient Cohort | 355 patients |
| | Raw Time-Series Observations | 11,298,127 records |
| **Data Integrity** | Available Data Ratio | 80.89% |
| | Unavailable / Masked Interval Ratio | 19.11% |
| **Event Distribution** | Adjustment Interval Ratio | 0.81% |
| | Non-Adjustment Interval Ratio | 99.19% |

</details>

<details>
<summary><b>🛡️ Click to Expand: IRB Approval & Strict Data Governance Policy</b></summary>

<br>

> **Institutional Review Board (IRB) Notice:**
> This study was approved by the Institutional Review Board of Kaohsiung Medical University Chung-Ho Memorial Hospital (Approval No.: **KMUHIRB-E(I)-20240420**).
> 
> * **Data Privacy & Confidentiality:** Clinical source records, patient-level identifiers, and institutional materials contain sensitive medical information protected under strict medical ethics.
> * **Non-Open Source Policy:** This repository is maintained exclusively for academic verification and is **not an open-source software project for general public use**.
> * **Access & Inquiry Protocol:** Public access does not grant reproduction, modification, or distribution rights. Any academic utilization or data access request **must be formally communicated and approved in advance**.
> * **Authorized Archives:** Processed sample archives are hosted securely via the [Project Releases Page](https://github.com/hiimsharon/icu-ventilator-adjustment/releases). Comprehensive guidelines are available in [DATA.md](DATA.md).

</details>

---

## Phase Repositories

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Phase 1</h3>
      <strong>Requirement Determination</strong>
      <br><br>
      Binary classification determining whether a ventilator adjustment is clinically required.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-1"><kbd>View Repository →</kbd></a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-1</h3>
      <strong>Direction Prediction</strong>
      <br><br>
      Multi-class prediction isolating the trajectory of parameter modifications.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-1"><kbd>View Repository →</kbd></a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-2</h3>
      <strong>Parameter Recommendation</strong>
      <br><br>
      Regression-based modeling providing optimal quantitative target settings.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-2"><kbd>View Repository →</kbd></a>
    </td>
  </tr>
</table>

---

## Master Thesis & Citation

<details>
<summary><b>📖 Click to View Official Thesis Record & Citation Details</b></summary>

<br>

**應用深度學習方法於加護病房呼吸器調參之研究**  
*Applying Deep Learning Techniques for Mechanical Ventilator Parameter Adjustment in the ICU*  
**Author:** 黃筱雯（2026）  
**Institution:** Kaohsiung Medical University  

**[View Official Thesis Record (hdl.handle.net)](https://hdl.handle.net/11296/7442av)**

### Academic Citation
> 黃筱雯（2026）。《應用深度學習方法於加護病房呼吸器調參之研究》。高雄醫學大學碩士論文。https://hdl.handle.net/11296/7442av

</details>

---

<div align="center">
<sub>

Copyright © 2026 Sha Huang. All Rights Reserved.  
Restricted to authorized academic research validation.

</sub>
</div>
