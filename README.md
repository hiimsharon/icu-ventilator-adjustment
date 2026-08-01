<div align="center">

# ICU Mechanical Ventilator Adjustment

### A Three-Phase Clinical Decision Framework Based on Multivariate Time-Series Analysis

<br>

This project learns and predicts the clinical decision workflow used
for ICU mechanical ventilator adjustment. Multivariate ventilator
time-series data are processed through three sequential decision
tasks: adjustment requirement determination, mode adjustment
direction classification, and parameter adjustment prediction.

<br>

[Phase 1](https://github.com/hiimsharon/icu-ventilator-phase-1) ·
[Phase 2-1](https://github.com/hiimsharon/icu-ventilator-phase-2-1) ·
[Phase 2-2](https://github.com/hiimsharon/icu-ventilator-phase-2-2) ·
[Citation](CITATION.md) ·
[Terms of Use](TERMS_OF_USE.md)

</div>

---

## Research Highlights

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Three-Phase Clinical Decision</h3>
      Models the sequential ICU ventilator adjustment workflow,
      progressing from adjustment requirement determination to mode
      adjustment direction and parameter-level prediction.
    </td>
    <td width="33%" valign="top">
      <h3>Multivariate Time-Series Analysis</h3>
      Learns temporal relationships among ventilator settings,
      ventilator monitoring variables, and patient-response
      information.
    </td>
    <td width="33%" valign="top">
      <h3>Hyperparameter Optimization</h3>
      Applies Bayesian hyperparameter optimization using the
      Tree-structured Parzen Estimator to identify appropriate
      training configurations for each decision phase.
    </td>
  </tr>
</table>

---

## Research Framework

The research framework begins with the collection and preprocessing
of ICU mechanical ventilator data. Ventilator modes, parameter
settings, and patient-response variables are organized into
multivariate time-series samples according to the requirements of
each research phase.

Long Short-Term Memory and Gated Recurrent Unit models are developed
for the three sequential decision tasks. Bayesian hyperparameter
optimization is used to determine the training configuration of each
model, followed by repeated data splitting and phase-specific model
evaluation.

The complete workflow includes:

1. **Data preparation and preprocessing** — clinical data screening,
   ventilator mode organization, feature processing, and temporal
   segmentation;
2. **Time-series sample construction** — stage-specific event
   definition and sliding-window sample generation;
3. **Model development and optimization** — LSTM and GRU modeling
   with Bayesian hyperparameter optimization;
4. **Three-phase decision modeling** — adjustment requirement
   determination, mode adjustment direction classification, and
   parameter adjustment prediction; and
5. **Evaluation and application demonstration** — stage-specific
   performance evaluation and presentation of the complete decision
   workflow through a research prototype.

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
    Overall research workflow integrating data preprocessing,
    multivariate time-series construction, recurrent neural network
    modeling, Bayesian hyperparameter optimization, and the
    three-phase ventilator adjustment decision framework.
  </sub>
</p>

---

## Phase Repositories

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Phase 1</h3>
      <strong>Adjustment Requirement Determination</strong>
      <br><br>
      Uses multivariate ventilator time-series data to determine
      whether the current ventilator setting should be maintained
      or adjusted.
      <br><br>
      <a href="https://github.com/hiimsharon/icu-ventilator-phase-1">
        View Phase 1 Repository →
      </a>
    </td>
    <td width="33%" valign="top">
      <h3>Phase 2-1</h3>
      <strong>Mode Adjustment Direction</strong>
      <br><br>
      Classifies the clinical adjustment direction as maintaining
      the current mode, decreasing ventilator support, or increasing
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

**黃筱雯（2026）。《應用深度學習方法於加護病房呼吸器調參之研究》。**

*Applying deep learning technique to parameter adjusting of mechanical ventilator ICU*

Master's thesis, Kaohsiung Medical University, July 2026.

The official National Digital Library of Theses and Dissertations in Taiwan record will be linked here after publication.

---

## Citation

When discussing or referencing the research presented in this
repository, please cite the associated master's thesis:

> 黃筱雯（2026）。《應用深度學習方法於加護病房呼吸器調參之研究》
> （碩士論文）。高雄醫學大學。

The complete citation instructions are provided in
[CITATION.md](CITATION.md).

Citation identifies and acknowledges the source of the research.
It does not grant permission to reproduce, redraw, modify,
redistribute, implement, or incorporate protected materials into
another research project or publication.

---

## Research Portfolio Notice

Clinical source data are not included in this repository.

This repository is provided for professional portfolio presentation,
research communication, and academic reference. It is not an
open-source project, and no general permission for reuse is granted.

Academic, educational, non-commercial, institutional, or research
purposes do not automatically grant permission to reproduce, adapt,
redistribute, implement, or incorporate protected materials into
another work.

Prior written permission is required before using original figures,
workflow diagrams, interface designs, documentation, source code,
model materials, or other protected research content in a paper,
thesis, dissertation, academic project, presentation, software
system, product, or derivative work.

See:

- [Citation Instructions](CITATION.md)
- [Terms of Use](TERMS_OF_USE.md)
- [Copyright Notice](COPYRIGHT.md)
- [Research and Use Notice](NOTICE.md)

---

<div align="center">

<sub>

Copyright © 2026 Sha Huang. All Rights Reserved.

Public access, citation, forking, cloning, or downloading does not
grant permission to reproduce, adapt, redistribute, implement, or
reuse protected research materials.

</sub>

</div>
