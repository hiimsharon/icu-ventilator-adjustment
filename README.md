<div align="center">

# ICU Mechanical Ventilator Adjustment

### A Three-Phase Clinical Decision Framework Based on Multivariate Time-Series Analysis

<br>

This project learns and predicts the clinical decision workflow used
for ICU mechanical ventilator adjustment. Multivariate ventilator
time-series data are processed through three sequential decision tasks:
adjustment requirement determination, mode adjustment direction
classification, and parameter adjustment prediction.

<br>

[Research Framework](#research-framework) ·
[Data Preparation](#data-preparation) ·
[Model Development](#model-development) ·
[Decision Framework](#three-phase-decision-framework) ·
[Master Thesis](#master-thesis)

</div>

---

## Research Highlights

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Clinical Decision Workflow</h3>
      Learns and predicts the sequential clinical workflow used for
      ICU mechanical ventilator adjustment.
    </td>
    <td width="33%" valign="top">
      <h3>Multivariate Time-Series</h3>
      Analyzes temporally ordered ventilator settings and
      patient-response variables across successive observations.
    </td>
    <td width="33%" valign="top">
      <h3>Three-Phase Decision Framework</h3>
      Integrates adjustment requirement determination, mode adjustment
      direction classification, and parameter adjustment prediction.
    </td>
  </tr>
</table>

---

## Research Framework

The overall research workflow consists of five connected components:
data collection and preprocessing, phase-specific sample construction,
model development and training, the three-phase ventilator adjustment
decision framework, and model evaluation.

ICU mechanical ventilator records are first reviewed, processed, and
organized as multivariate time-series data. Adjustment events, mode
transitions, temporal sequences, and task-specific samples are then
constructed according to the objective of each research phase.

LSTM and GRU models are developed for the three decision tasks.
Hyperparameter configurations are optimized using the
Tree-structured Parzen Estimator, followed by model selection and
phase-specific evaluation.

The resulting framework learns and predicts the clinical decision
workflow used for ventilator adjustment:

1. determining whether the ventilator setting requires adjustment;
2. classifying the direction of ventilator mode adjustment; and
3. predicting the adjustment magnitude of pressure control and
   respiratory rate.

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
    Overall research workflow integrating data preparation,
    time-series construction, model development, the three-phase
    decision framework, and model evaluation.
  </sub>
</p>

---

## Data Preparation

The data preparation procedure is designed according to the objective
of each decision phase while maintaining a consistent multivariate
time-series modeling strategy.

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Data Processing</h3>
      Clinical data quality review, abnormal-value handling, temporal
      organization, and ventilator mode representation.
    </td>
    <td width="33%" valign="top">
      <h3>Sample Construction</h3>
      Adjustment-event definition, mode-transition identification,
      independent sample segmentation, and phase-specific selection.
    </td>
    <td width="33%" valign="top">
      <h3>Sequence Generation</h3>
      Sliding-window construction, multivariate temporal sequences,
      task-specific labels, and regression targets.
    </td>
  </tr>
</table>

Clinical source data, patient-level records, and restricted
institutional materials are not distributed through this repository.

---

## Model Development

<table>
  <tr>
    <td width="25%" valign="top">
      <h3>Time-Series Input</h3>
      Multivariate sequential inputs are constructed separately for
      each ventilator adjustment decision task.
    </td>
    <td width="25%" valign="top">
      <h3>LSTM and GRU</h3>
      Recurrent neural network architectures are developed and compared
      for classification and regression objectives.
    </td>
    <td width="25%" valign="top">
      <h3>Hyperparameter Optimization</h3>
      Bayesian optimization using the Tree-structured Parzen Estimator
      is applied to identify suitable model configurations.
    </td>
    <td width="25%" valign="top">
      <h3>Model Selection</h3>
      Models are selected and evaluated using repeated independent data
      splits and task-specific performance measures.
    </td>
  </tr>
</table>

---

## Three-Phase Decision Framework

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Phase 1</h3>
      <strong>Adjustment Requirement Determination</strong>
      <br><br>
      Uses multivariate ventilator time-series data to determine whether
      the current ventilator setting should be maintained or adjusted.
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-1</h3>
      <strong>Mode Adjustment Direction</strong>
      <br><br>
      Classifies the adjustment direction as maintaining the current
      mode, decreasing ventilator support, or increasing ventilator
      support.
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-2</h3>
      <strong>Parameter Adjustment Prediction</strong>
      <br><br>
      Predicts the adjustment magnitude of pressure control and
      respiratory rate after the mode adjustment direction is
      determined.
    </td>
  </tr>
</table>

---

## Phase Repositories

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Phase 1</h3>
      <strong>Adjustment Requirement Determination</strong>
      <br><br>
      Uses multivariate ventilator time-series data to determine whether
      the current ventilator setting should be maintained or adjusted.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-1">
        View Phase 1 Repository →
      </a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-1</h3>
      <strong>Mode Adjustment Direction</strong>
      <br><br>
      Classifies the clinical adjustment direction as maintaining the
      current mode, decreasing ventilator support, or increasing
      ventilator support.
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
      respiratory rate after the mode adjustment direction has been
      determined.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-2-2">
        View Phase 2-2 Repository →
      </a>
    </td>
  </tr>
</table>

---

## Master Thesis

**Applying Deep Learning Methods to Mechanical Ventilator Adjustment
in the Intensive Care Unit**

Master's thesis, July 2026.

The official thesis record and public link will be updated here after
they become available through the National Digital Library of Theses
and Dissertations in Taiwan.

---

## Research Portfolio Notice

Clinical source data, patient-level records, restricted institutional
materials, and confidential research data are not distributed through
this repository.

This repository is publicly accessible for research presentation,
professional portfolio review, and academic reference. Public access
does not grant an open-source license or general permission to reuse
the contents.

This research may be identified, discussed, or cited by clearly
acknowledging:

- the author: **Sha Huang**;
- the research title: **ICU Mechanical Ventilator Adjustment**;
- the year: **2026**; and
- the original repository link.

Acknowledgment or citation does not grant permission to reproduce,
republish, redistribute, modify, translate, redraw, adapt, or
incorporate protected materials into another research project,
publication, thesis, dissertation, academic project, presentation,
software system, commercial product, machine-learning dataset, or
derivative work.

Any reuse beyond a lawful and properly attributed limited citation
requires prior written permission from the copyright holder.

See:

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
