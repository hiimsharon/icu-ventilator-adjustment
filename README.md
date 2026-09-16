<div align="center">

# ICU Mechanical Ventilator Adjustment

### A Three-Phase Clinical Decision Framework Based on Multivariate Time-Series Analysis

<p align="center">
  <a href="#-research-specifications--scope"><img src="https://img.shields.io/badge/Status-Active_Research-blue?style=flat-square" alt="Status"></a>
  <a href="https://hdl.handle.net/11296/7442av"><img src="https://img.shields.io/badge/Thesis-KMU_2026-teal?style=flat-square" alt="Thesis"></a>
  <a href="DATA.md"><img src="https://img.shields.io/badge/IRB-Approved-critical?style=flat-square" alt="IRB"></a>
</p>

This project implements a multi-phase clinical decision framework designed to model and predict mechanical ventilator adjustment workflows in intensive care units using multivariate time-series data.

<br>

[Core Architecture](#-core-architecture) ·
[Specifications](#-research-specifications--scope) ·
[Methodology](#-methodology) ·
[Phase Repositories](#-phase-repositories) ·
[Thesis & Reference](#-master-thesis)

</div>

---

## Research Specifications & Scope

> **[ 點擊下方按鈕看看研究規格與範疇 ]**
> 詳細的臨床領域、序列模型與最佳化參數設定已收納於下方互動模組中。請點擊以檢視完整規格：

<details>
<summary><b> 展開：查看詳細研究範疇與系統規格 (Research Scope & Specifications)</b></summary>
<br>

> 本研究涵蓋高度複雜之加護病房臨床情境，非標準簡易資料處理專案：
>
> * **Clinical Domain:** Intensive Care Unit (ICU) — High-acuity physiological monitoring streams.
> * **Research Topic:** Mechanical Ventilator Parameter Adjustment & Sequential Decision Modeling.
> * **Data Architecture:** Multivariate Ventilator Time-Series (High-frequency telemetry & setting arrays).
> * **Core Sequence Models:** Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) architectures.
> * **Hyperparameter Optimization:** Bayesian Optimization via Tree-structured Parzen Estimator (TPE) for stability and generalization.
> * **Research Output:** A rigorous Three-Stage Clinical Decision Framework for intelligent ventilation control.

</details>

---

## Research Highlights

<details>
<summary><b> 展開：核心技術亮點 (Click to Expand Highlights)</b></summary>
<br>

* **Clinical Workflow Modeling:** Learns and predicts the sequential decision logic utilized by clinicians during mechanical ventilation management.
* **Multivariate Temporal Analysis:** Captures complex dynamic interactions among ventilator settings, patient physiological responses, and adjustment milestones.
* **Rigorous Optimization:** Employs Bayesian optimization frameworks to systematically search and stabilize network hyperparameter configurations.

</details>

---

## Research Framework

The research architecture integrates data preprocessing, phase-specific sample formulation, sequence modeling, and decision evaluation into a cohesive pipeline. 

Continuous ICU monitoring streams are structured into temporal intervals to predict three progressive clinical objectives: determining adjustment necessity, forecasting adjustment direction, and recommending precise parameter values.

<p align="center">
  <a href="assets/figures/framework/research-framework.jpg">
    <img
      src="assets/figures/framework/research-framework.jpg"
      width="760"
      alt="Overall research framework for ICU mechanical ventilator adjustment"
    >
  </a>
</p>

<p align="center">
  <sub>
    Systematic pipeline of temporal data processing, sequence generation,
    three-phase decision modeling, and validation.
  </sub>
</p>

---

## Methodology & Data Governance

### Cohort & Data Profile Summary
The retrospective dataset comprises high-frequency telemetry and setting records from **355 patients** undergoing invasive mechanical ventilation, totaling **11,298,127 minutes** of multivariate time-series observations.

<details>
<summary><b> 展開：檢視資料集統計分佈與完整數據指標 (Dataset Profile & Metrics)</b></summary>
<br>

* **Total Patient Cohort:** 355 patients
* **Raw Time-Series Observations:** 11,298,127 records
* **Available Data Ratio:** 80.89%
* **Unavailable / Masked Interval Ratio:** 19.11%
* **Adjustment Interval Ratio:** 0.81%
* **Non-Adjustment Interval Ratio:** 99.19%

</details>

<br>

<details>
<summary><b> 展開：IRB 審查與嚴格資料治理聲明 (IRB & Governance Notice)</b></summary>
<br>

> **Institutional Review Board (IRB) Notice:**
> This study was approved by the Institutional Review Board of Kaohsiung Medical University Chung-Ho Memorial Hospital (Approval No.: KMUHIRB-E(I)-20240420).
> 
> * **Data Privacy & Confidentiality:** Clinical source records, patient-level identifiers, and institutional materials contain sensitive medical information protected under clinical governance frameworks.
> * **Non-Open Source Policy:** This repository is maintained strictly for academic research verification. **It is not an open-source software project for general public reuse.**
> * **Access & Inquiry Protocol:** Public access to this repository does not grant reproduction, modification, or distribution rights. Any academic utilization, replication inquiry, or data access request **must be communicated to and approved by the author in advance**.
> * **Authorized Archives:** Processed, non-identifiable sample archives are securely hosted via the [Project Releases Page](https://github.com/hiimsharon/icu-ventilator-adjustment/releases). Comprehensive guidelines are documented in [DATA.md](DATA.md).

</details>

---

## Phase Repositories

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Phase 1</h3>
      <strong>Adjustment Requirement Determination</strong>
      <br><br>
      Binary classification determining whether ventilator adjustments
      are required at the current time step.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-1">
        View Phase 1 Repository →
      </a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-1</h3>
      <strong>Adjustment Direction Prediction</strong>
      <br><br>
      Multi-class prediction isolating the trajectory of parameter
      modifications following trigger confirmation.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-1">
        View Phase 2-1 Repository →
      </a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-2</h3>
      <strong>Parameter Adjustment Recommendation</strong>
      <br><br>
      Regression-based modeling providing optimal quantitative targets
      for ventilator control settings.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-2">
        View Phase 2-2 Repository →
      </a>
    </td>
  </tr>
</table>

---

## Master Thesis & Reference

**應用深度學習方法於加護病房呼吸器調參之研究**

Applying Deep Learning Techniques for Mechanical Ventilator Parameter Adjustment in the ICU

**Author:** 黃筱雯（2026）  
**Institution:** Kaohsiung Medical University

**[View Official Thesis Record →](https://hdl.handle.net/11296/7442av)**

<details>
<summary><b>📖 點此展開：學術引用格式與授權聲明 (Academic Citation & Terms)</b></summary>
<br>

If you reference this research framework or related materials, please cite the master's thesis:
> 黃筱雯（2026）。《應用深度學習方法於加護病房呼吸器調參之研究》。高雄醫學大學碩士論文。https://hdl.handle.net/11296/7442av

* Detailed governance policies: [Terms of Use](TERMS_OF_USE.md) | [Copyright Notice](COPYRIGHT.md) | [Research Notice](NOTICE.md)

</details>

---

<div align="center">
<sub>

Copyright © 2026 Sha Huang. All Rights Reserved.  
Restricted to authorized academic research validation.

</sub>
</div>
