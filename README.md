# AIML Project

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge&logo=github-actions)](https://github.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.1-blue?style=for-the-badge)](https://github.com)
[![Code Coverage](https://img.shields.io/badge/coverage-88%25-success?style=for-the-badge)](https://github.com)

## Table of Contents

- [Overview](#overview)
    - [Key Features](#key-features)
- [CNN Results](#cnn-results)
- [Getting Started](#getting-started)
- [Team Members](#team-members)
- [License](#license--acknowledgments)

---

## Overview
This project focuses on building and optimizing Deep Convolutional Neural Networks (CNN) for binary image classification of Dogs vs. Cats using TensorFlow and Keras.

### Key Features
- **Exploratory Data Analysis (EDA)**: Dataset balance and file corruption checks.
- **Optimized Data Pipeline**: Stratified splitting with `tf.data` prefetching and caching.
- **Model Evolution**: Baseline CNN (V1) yielding 76.08% $\rightarrow$ Optimized CNN (V2) yielding **87.98% accuracy**.
- **Error Analysis**: Detailed false-positive & false-negative visual breakdown.

---

## CNN Results

<br>
<center>
<table border="1">
    <tr><th colspan="2"><b>Baseline CNN Results (Model V1)</b></th></tr>
    <tr><td>&emsp;Input size:      </td><td> &emsp; 224 × 224 × 3 &emsp; </td></tr>
    <tr><td>&emsp;Training images:  </td><td> &emsp; 17,500 </td></tr>
    <tr><td>&emsp;Validation images: &emsp;&emsp;  </td><td> &emsp; 2,500  </td></tr>
    <tr><td>&emsp;Test images:  </td><td> &emsp; 5,000  </td></tr>
    <tr><td>&emsp;Batch size:  </td><td> &emsp; 16  </td></tr>
    <tr><td>&emsp;Total parameters:   </td><td> &emsp; 109,889  </td></tr>
    <tr><td>&emsp;Best validation accuracy:   </td><td> &emsp; 75.44%   </td></tr>
    <tr><td>&emsp;Test accuracy:   </td><td> &emsp; 76.08% </td></tr>
</table>
</center>

<br>
<br>

<center>
<table border="1">
    <tr><th colspan="2"><b>Improved CNN Results (Model V2)</b></th></tr>
    <tr><td>&emsp;Input size:      </td><td> &emsp; 224 × 224 × 3 &emsp; </td></tr>
    <tr><td>&emsp;Regularization:  </td><td> &emsp; Batch Normalization + Dropout (0.25, 0.50) &emsp; </td></tr>
    <tr><td>&emsp;Best validation accuracy:   </td><td> &emsp; 86.12%   </td></tr>
    <tr><td>&emsp;Test accuracy:   </td><td> &emsp; <b>87.98%</b> (+11.90% improvement) </td></tr>
    <tr><td>&emsp;Test loss:   </td><td> &emsp; 0.2914 </td></tr>
</table>
</center>

<br>
<br>

<center>
<table>
<tr>
<td>
<table border="1">
    <tr><th colspan="2"><b>Cat Classification Metrics:</b></th></tr>
    <tr><td>&emsp;Precision:       </td><td> &emsp; 0.94 &emsp; </td></tr>
    <tr><td>&emsp;Recall:   </td><td> &emsp; 0.82 </td></tr>
    <tr><td>&emsp;F1-score:  &emsp;&emsp;  </td><td> &emsp; 0.87 </td></tr>
</table>
</td>
<td>
<table border="1">
    <tr><th colspan="2"><b>Dog Classification Metrics:</b></th></tr>
    <tr><td>&emsp;Precision:       </td><td> &emsp; 0.84 &emsp; </td></tr>
    <tr><td>&emsp;Recall:   </td><td> &emsp; 0.94 </td></tr>
    <tr><td>&emsp;F1-score:  &emsp;&emsp;  </td><td> &emsp; 0.89 </td></tr>
</table>
</td>
</tr>
</table>
</center>

<br>
<br>

<center>
<table border="1">
    <tr><th colspan="3"><b>Confusion Matrix</b></th></tr>
    <tr><td></td><td><b>Predicted Dogs</b></td><td><b>Predicted Cats</b></td></tr>
    <tr><td><b>Actual Dogs</b></td><td>2040</td><td>460</td></tr>
    <tr><td><b>Actual Cats</b></td><td>141</td><td>2359</td></tr>
</table>
</center>

<br>
<br>

---

## Getting Started

### 1. Installation
```bash
# Clone the repository
git clone https://github.com/IT25102993/AIML-Project.git
cd Dogs_vs_Cats_CNN

# Install required dependencies
python install_requirements.py
```

### 2. Run Training & Evaluation
```bash
# Train Model V2
python src/train_cnn_v2.py

# Evaluate Model V2 on test set
python src/evaluate_cnn_v2.py

# Run Error Analysis
python src/error_analysis_v2.py
```

### 3. Real-Time Inference
```bash
python src/predict.py
```

---

## Team Members

- **IT25102040** - Nimesh K. G. N. 
- **IT25102993** - Sakalasooriya S. A. T. S.
- **IT25200818** - Ranathunga K. A. L. D.
- **IT25102186** - Weerasena K. W. D.
- **IT25300026** - Thilakarathna K. K. R. V.
- **IT25101186** - Sulakshana N. V. B. U.

---

## License & Acknowledgments

Distributed under the MIT License. See `LICENSE` for more information.

<p align="center">
  Designed & Developed by <b>2026-Y2-S1-MLB-B1G2-03</b> Team Members for the <br>
  <b>Artificial Intelligence & Machine Learning Project - SLIIT</b>
</p>
