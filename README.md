<div align="center">

# ICU Mechanical Ventilator Adjustment

### A Three-Phase Clinical Decision Framework Based on Multivariate Time-Series Analysis

<br>

This project implements a multi-phase clinical decision framework
designed to model and predict mechanical ventilator adjustment workflows
in intensive care units using multivariate time-series data.

<br>

[Research Scope](#research-scope) ·
[Research Highlights](#research-highlights) ·
[Research Framework](#research-framework) ·
[Methodology & Data](#methodology--data) ·
[Phase Repositories](#phase-repositories) ·
[Master Thesis](#master-thesis)

</div>

---

## Research Scope

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
    <td>Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU)</td>
  </tr>
  <tr>
    <td><strong>Model Optimization</strong></td>
    <td>Bayesian Hyperparameter Optimization via Tree-structured Parzen Estimator (TPE)</td>
  </tr>
  <tr>
    <td><strong>Research Output</strong></td>
    <td>Three-Stage Clinical Decision Framework</td>
  </tr>
</table>

---

## Research Highlights

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Clinical Workflow Modeling</h3>
      Learns and predicts the sequential decision logic utilized by
      clinicians during mechanical ventilation management.
    </td>
    <td width="33%" valign="top">
      <h3>Multivariate Temporal Analysis</h3>
      Captures complex dynamic interactions among ventilator settings,
      patient physiological responses, and adjustment milestones.
    </td>
    <td width="33%" valign="top">
      <h3>Rigorous Optimization</h3>
      Employs Bayesian optimization frameworks to systematically search
      and stabilize network hyperparameter configurations.
    </td>
  </tr>
</table>

---

## Research Framework

The research architecture integrates data preprocessing, phase-specific
sample formulation, sequence modeling, and decision evaluation into a
cohesive pipeline. 

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

## Methodology & Data

### Data Preparation & Cohort Statistics
The retrospective dataset comprises high-frequency telemetry and setting records from **355 patients** undergoing invasive mechanical ventilation, totaling **11,298,127 minutes** of multivariate time-series observations.

<br>

<!-- 互動按鈕效果：點擊即可展開詳細數據與 IRB 聲明 -->
<details>
  <summary><b>📊 點擊展開：Dataset Profile & IRB Compliance Statement</b></summary>
  <br>

  #### Dataset Profile and Quality Metrics
  <table>
    <tr>
      <td width="30%"><strong>Category</strong></td>
      <td width="40%"><strong>Metric Description</strong></td>
      <td><strong>Quantitative Value</strong></td>
    </tr>
    <tr>
      <td rowspan="2"><strong>Cohort Scale</strong></td>
      <td>Total Patient Cohort</td>
      <td>355 patients</td>
    </tr>
    <tr>
      <td>Raw Time-Series Observations</td>
      <td>11,298,127 records</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>Data Integrity</strong></td>
      <td>Available Data Ratio</td>
      <td>80.89%</td>
    </tr>
    <tr>
      <td>Unavailable / Masked Interval Ratio</td>
      <td>19.11%</td>
    </tr>
    <tr>
      <td rowspan="2"><strong>Event Distribution</strong></td>
      <td>Adjustment Interval Ratio</td>
      <td>0.81%</td>
    </tr>
    <tr>
      <td>Non-Adjustment Interval Ratio</td>
      <td>99.19%</td>
    </tr>
  </table>

  <br>

  #### Institutional Review Board (IRB) & Governance
  > **IRB Approval Notice:** 
  > This study was approved by the Institutional Review Board of Kaohsiung Medical University Chung-Ho Memorial Hospital (Approval No.: KMUHIRB-E(I)-20240420).
  > 
  > * **Data Privacy:** Patient-level records and institutional materials contain sensitive medical information protected under medical ethics.
  > * **Non-Open Source Policy:** Strictly for academic research verification. Not an open-source software project for general public reuse.
  > * **Access Protocol:** Public access does not grant reproduction rights. Any academic utilization or data access **must be communicated and approved in advance**.
  > * **Archives:** Processed sample archives are hosted via the [Project Releases Page](https://github.com/hiimsharon/icu-ventilator-adjustment/releases). See detailed guidelines in [DATA.md](DATA.md).

</details>

<br>

### Model Development & Evaluation
* **Sequence Modeling:** Implements deep recurrent networks (LSTM and GRU) optimized for clinical multivariate forecasting.
* **Hyperparameter Tuning:** Applies TPE-based Bayesian optimization to balance convergence speed and generalization error.
* **Evaluation Metrics:** Classification performance is assessed via accuracy, precision, recall, F1-score, and AUROC. Regression performance is evaluated using agreement and error metrics tailored to physiological targets.

---

## Phase Repositories

<table align="center">
  <tr>
    <td align="center" width="33%">
      <h3>Phase 1</h3>
      <p><b>Requirement Determination</b></p>
      <br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-1">
        <img src="https://img.shields.io/badge/View-Phase_1-blue?style=for-the-badge&logo=github" alt="Phase 1">
      </a>
    </td>
    <td align="center" width="33%">
      <h3>Phase 2-1</h3>
      <p><b>Direction Prediction</b></p>
      <br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-1">
        <img src="https://img.shields.io/badge/View-Phase_2.1-blue?style=for-the-badge&logo=github" alt="Phase 2-1">
      </a>
    </td>
    <td align="center" width="33%">
      <h3>Phase 2-2</h3>
      <p><b>Parameter Recommendation</b></p>
      <br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-2">
        <img src="https://img.shields.io/badge/View-Phase_2.2-blue?style=for-the-badge&logo=github" alt="Phase 2-2">
      </a>
    </td>
  </tr>
</table>

---

## Master Thesis

**應用深度學習方法於加護病房呼吸器調參之研究**  
*Applying Deep Learning Techniques for Mechanical Ventilator Parameter Adjustment in the ICU*  

* **Author:** 黃筱雯（2026）
* **Institution:** Kaohsiung Medical University
* **[View Official Thesis Record →](https://hdl.handle.net/11296/7442av)**

---

## Citation & Governance

If you reference this research framework, please cite the master's thesis:
> 黃筱雯（2026）。《應用深度學習方法於加護病房呼吸器調參之研究》。高雄醫學大學碩士論文。https://hdl.handle.net/11296/7442av

<sub>
Copyright © 2026 Sha Huang. All Rights Reserved. Restricted to authorized academic research validation. Detailed terms are available in <a href="TERMS_OF_USE.md">Terms of Use</a>.
</sub>
