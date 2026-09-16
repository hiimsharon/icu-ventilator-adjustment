<div align="center">

# ICU Mechanical Ventilator Adjustment

### A Three-Phase Clinical Decision Framework Based on Multivariate Time-Series Analysis

<br>

This project learns and predicts the clinical decision workflow used
for ICU mechanical ventilator adjustment through multivariate
time-series analysis.

<br>

[Research Scope](#research-scope) ·
[Research Highlights](#research-highlights) ·
[Research Framework](#research-framework) ·
[Methodology](#methodology) ·
[Phase Repositories](#phase-repositories) ·
[Master Thesis](#master-thesis) ·
[Citation & References](#citation--references)

</div>

---

## Research Scope

<table>
  <tr>
    <td width="28%"><strong>Clinical Domain</strong></td>
    <td>Intensive Care Unit</td>
  </tr>
  <tr>
    <td><strong>Research Topic</strong></td>
    <td>Mechanical Ventilator Adjustment</td>
  </tr>
  <tr>
    <td><strong>Data Structure</strong></td>
    <td>Multivariate Ventilator Time-Series</td>
  </tr>
  <tr>
    <td><strong>Sequence Models</strong></td>
    <td>Long Short-Term Memory and Gated Recurrent Unit</td>
  </tr>
  <tr>
    <td><strong>Model Optimization</strong></td>
    <td>Bayesian Hyperparameter Optimization using the Tree-structured Parzen Estimator</td>
  </tr>
  <tr>
    <td><strong>Research Output</strong></td>
    <td>Three-stage ventilator adjustment decision framework</td>
  </tr>
</table>

---

## Research Highlights

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Clinical Decision Framework</h3>
      Learns and predicts the sequential clinical workflow used for
      ICU mechanical ventilator adjustment.
    </td>
    <td width="33%" valign="top">
      <h3>Multivariate Time-Series Analysis</h3>
      Models temporal relationships among ventilator settings,
      monitored responses, and successive adjustment decisions.
    </td>
    <td width="33%" valign="top">
      <h3>Bayesian Hyperparameter Optimization</h3>
      Applies the Tree-structured Parzen Estimator to optimize model
      configurations before final model selection.
    </td>
  </tr>
</table>

---

## Research Framework

The complete research workflow is organized into five connected
components: data collection and preprocessing, phase-specific sample
construction, model development and training, three-phase decision
modeling, and model evaluation.

ICU ventilator records are first reviewed and organized into
multivariate temporal sequences. Independent samples, adjustment
events, mode transitions, and prediction targets are subsequently
constructed according to the objective of each research phase.

The completed framework converts sequential ventilator information
into three linked decisions: adjustment requirement determination,
adjustment direction prediction, and parameter adjustment recommendation.

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
    Overall workflow of data preparation, time-series construction,
    model development, three-phase decision modeling, and evaluation.
  </sub>
</p>

---

## Methodology

### Data Preparation

The original research dataset comprises clinical records from 355 patients receiving invasive mechanical ventilation, totaling 11,298,127 time-series records with a sampling frequency of one record per minute for ventilator monitoring and setting information. 

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Data Processing</h3>
      Reviews data quality, handles predefined abnormal conditions,
      organizes temporal records, and represents ventilator modes.
    </td>
    <td width="33%" valign="top">
      <h3>Sample Construction</h3>
      Defines adjustment events and mode transitions, segments
      independent samples, and applies phase-specific selection rules.
    </td>
    <td width="33%" valign="top">
      <h3>Sequence Generation</h3>
      Constructs sliding-window time-series samples with task-specific
      classification labels or regression targets.
    </td>
  </tr>
</table>

#### Dataset Profile and Quality Statistics

<table>
  <tr>
    <td width="30%"><strong>Category</strong></td>
    <td width="40%"><strong>Statistical Item</strong></td>
    <td><strong>Value</strong></td>
  </tr>
  <tr>
    <td rowspan="2"><strong>Data Scale</strong></td>
    <td>Original Patient Count</td>
    <td>355 patients</td>
  </tr>
  <tr>
    <td>Original Time-Series Records</td>
    <td>11,298,127 records</td>
  </tr>
  <tr>
    <td rowspan="2"><strong>Data Quality</strong></td>
    <td>Available Data Ratio</td>
    <td>80.89%</td>
  </tr>
  <tr>
    <td>Unavailable Data Ratio</td>
    <td>19.11%</td>
  </tr>
  <tr>
    <td rowspan="2"><strong>Adjustment Event Distribution</strong></td>
    <td>Adjustment Ratio in Available Data</td>
    <td>0.81%</td>
  </tr>
  <tr>
    <td>Non-Adjustment Ratio in Available Data</td>
    <td>99.19%</td>
  </tr>
</table>

<br>

#### IRB Approval & Data Access Statement

> **Institutional Review Board (IRB) Notice:**
> The collection and utilization of this clinical dataset have been formally reviewed and approved by the Institutional Review Board (IRB). 
> 
> * **Confidentiality & Compliance:** Clinical source data, patient-level medical records, and restricted institutional materials contain sensitive health information and are strictly protected. 
> * **Access Restriction:** Public access to this repository does not grant permission to reproduce, distribute, or use the raw clinical data. Unauthorized use, redistribution, or commercial exploitation of these datasets is strictly prohibited.
> * **Authorized Archives:** For authorized personnel or academic replication, processed sample archives are securely maintained under institutional guidelines. You can check the authorized release assets via the [Project Releases Page](https://github.com/hiimsharon/icu-ventilator-adjustment/releases).

<br>

### Model Development

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Sequence Modeling</h3>
      Develops LSTM and GRU architectures for multivariate
      time-series classification and regression.
    </td>
    <td width="33%" valign="top">
      <h3>Hyperparameter Optimization</h3>
      Uses Bayesian optimization with the Tree-structured Parzen
      Estimator to search suitable model configurations.
    </td>
    <td width="33%" valign="top">
      <h3>Model Selection</h3>
      Compares candidate models using repeated independent data
      splits and decision-task-specific selection criteria.
    </td>
  </tr>
</table>

<br>

### Model Evaluation

Classification tasks are evaluated using accuracy, precision, recall,
F1-score, AUROC, and confusion-matrix analysis. Parameter adjustment
prediction is evaluated using correlation-based and
threshold-based agreement measures appropriate to the regression
objective.

Evaluation is performed separately for each decision phase so that
model performance remains aligned with the corresponding research
task.

---

## Phase Repositories

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Phase 1</h3>
      <strong>Adjustment Requirement Determination</strong>
      <br><br>
      Determines whether the current ventilator setting should be
      maintained or adjusted.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-1">
        View Phase 1 Repository →
      </a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-1</h3>
      <strong>Adjustment Direction Prediction</strong>
      <br><br>
      Predicts the direction of ventilator adjustment after the
      requirement for adjustment has been determined.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-1">
        View Phase 2-1 Repository →
      </a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-2</h3>
      <strong>Parameter Adjustment Recommendation</strong>
      <br><br>
      Recommends appropriate ventilator parameter adjustments
      based on the identified adjustment direction.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-2">
        View Phase 2-2 Repository →
      </a>
    </td>
  </tr>
</table>

---

## Master Thesis

**應用深度學習方法於加護病房呼吸器調參之研究**

Applying Deep Learning Techniques for Mechanical Ventilator Parameter Adjustment in the ICU

**Author:** 黃筱雯（2026）

Kaohsiung Medical University

**[View Thesis Record →](https://hdl.handle.net/11296/7442av)**



---

## Citation & References

### Citing This Research

If you reference this research in academic work, please cite the master's thesis:

> 黃筱雯（2026）。《應用深度學習方法於加護病房呼吸器調參之研究》。高雄醫學大學。https://hdl.handle.net/11296/7442av

<sub>
This citation is provided as a practical reference format. The bibliographic
details may be updated later to match the final official thesis record.
</sub>

<br>

### Reference List

The complete reference list used in this research is available in the master's thesis.

**[View Thesis Record and References →](https://hdl.handle.net/11296/7442av)**

<br>

### Access During the Embargo Period

If the thesis full text is not yet publicly available during the embargo period,
please refer to the official instructions provided by Kaohsiung Medical University Library.

**[Thesis Access Instructions →](https://olis.kmu.edu.tw/index.php/zh-TW/lib-faq/10-)**

<br>

<sub>
Citation or acknowledgment identifies the source of this research and does not
grant permission to reproduce, modify, adapt, redistribute, or reuse protected
research materials. For detailed conditions, see
<a href="TERMS_OF_USE.md">Terms of Use</a>.
</sub>


---

## Research Portfolio Notice

Clinical source data and patient-level records are not publicly
distributed. Public access to this repository does not grant an
open-source license or general reuse permission.

This research may be identified or discussed by clearly acknowledging
**Sha Huang**, the research title, the year **2026**, and the original
repository link. Acknowledgment does not grant permission to reproduce,
adapt, redistribute, or incorporate protected materials into another
work.

Detailed conditions are provided in:

- [Terms of Use](TERMS_OF_USE.md)
- [Copyright Notice](COPYRIGHT.md)
- [Research and Use Notice](NOTICE.md)

---

<div align="center">

<sub>

Copyright © 2026 Sha Huang. All Rights Reserved.

Academic, educational, non-commercial, or research use does not by
itself grant permission to reuse protected research materials.

</sub>

</div>
