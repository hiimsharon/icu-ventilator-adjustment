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
[Master Thesis](#master-thesis)

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
    <td>Three sequential ventilator adjustment decisions</td>
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
mode adjustment direction classification, and parameter adjustment
prediction.

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

Clinical source data, patient-level records, and restricted
institutional materials are not distributed through this repository.

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
      <strong>Mode Adjustment Direction</strong>
      <br><br>
      Classifies whether ventilator support should be maintained,
      decreased, or increased.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-1">
        View Phase 2-1 Repository →
      </a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-2</h3>
      <strong>Parameter Adjustment Prediction</strong>
      <br><br>
      Predicts the adjustment magnitude of pressure control and
      respiratory rate.
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
*Applying Deep Learning Technique to Parameter Adjusting of Mechanical Ventilator ICU*

**黃筱雯（2026）**。The official thesis record and permanent public
access link will be added after publication.
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
