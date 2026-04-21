# SC-DION: A Solver-Consistent Deep Inverse Operator Network for Self-Supervised Constitutive Inversion in Frozen Soils

This repository contains the codes and datasets associated with the manuscript:

**“SC-DION: A Solver-Consistent Deep Inverse Operator Network for Self-Supervised Constitutive Inversion in Frozen Soils”**

The proposed framework couples an inverse neural operator with a forward heat-transfer PDE solver to infer the **soil freezing characteristic curve (SFCC)** from temperature observations in a self-supervised manner.

---

## Environment

The codes were developed and tested using:

- **Python**
- **PyTorch**
- **NVIDIA GeForce RTX 4070 Super GPU**

GPU acceleration is recommended for model training and inversion.

---

## Repository Structure

### `Dataset/`
This folder contains:

- fitted parameters of the **SFCC** dataset
- temperature-field data used for model training and evaluation

The original SFCC measurement points are available at Zenodo:

- https://zenodo.org/records/5592825

---

### `Train_20/` to `Train_160/`
These folders contain the complete codes for model training and evaluation under different training dataset sizes:

- `Train_20/`: training with 20 temperature fields
- `Train_40/`: training with 40 temperature fields
- `Train_80/`: training with 80 temperature fields
- `Train_120/`: training with 120 temperature fields
- `Train_160/`: training with 160 temperature fields

Among them, **`Train_80/`** additionally includes the full codes for the three generalization settings discussed in the study.

---

### `Scaling law/`
This folder contains:

- inversion results under different training dataset sizes
- forward temperature prediction results under different training dataset sizes
- visualization codes for the **scaling-law analysis**

---

## Main Contents

This repository supports the following tasks:

- self-supervised inversion of **SFCCs**
- reconstruction of temperature fields using the inferred SFCCs
- generalization tests under multiple settings
- scaling-law analysis with respect to training dataset size

---

## Reproducibility Guide

The main executable files in this repository are the Jupyter notebooks (`.ipynb`) in each training folder.

For example:

- `Train_20/DM_Operator_form_2_train20.ipynb`
- corresponding notebooks in `Train_40/`, `Train_80/`, `Train_120/`, and `Train_160/`

These notebooks contain the main workflow for model training, inversion, and temperature-field prediction.

The other files in each training folder are supporting data or generated outputs, including:

- `.npy`: predicted temperature fields or sensor observations
- `.npz`: processed dataset used in the corresponding experiment
- `.pt`: saved PyTorch model
- `.xlsx`: recorded loss components or postprocessed results

---

## Notes

- The original SFCC data points were not generated in this repository. Please refer to the Zenodo archive above for the raw measurements.
- This repository mainly contains the processed inputs, training scripts, inversion scripts, forward simulation scripts, and visualization scripts used in this work.
- Folder names follow the training sample size used in the corresponding experiments.

---

## Citation

If you use this repository, please cite the associated manuscript:

**Gou, L., Likos, W. J., and Wang, Z.**  
*SC-DION: A Solver-Consistent Deep Inverse Operator Network for Self-Supervised Constitutive Inversion in Frozen Soils.*

---

## Contact

**Lingyun Gou**  
Email: lgou4@wisc.edu
