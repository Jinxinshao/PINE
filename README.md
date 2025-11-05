<div align="center">

# PINE: Physics-Informed Neural Enhancement for Underwater Video via Implicit Representation

**Physics-Informed Neural Enhancement for Underwater Video Enhancement**

[![Project Page](https://img.shields.io/badge/Project-Page-blue?style=flat-square)](https://jinxinshao.github.io/PINE/)
[![Paper](https://img.shields.io/badge/Paper-PDF-red?style=flat-square)](https://drive.google.com/file/d/1o4hoxZ1zBW1VEYeTqmAIkhd5wECrUkYV/view?usp=drive_link)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
![Stars](https://img.shields.io/github/stars/jinxinshao/PINE?style=flat-square&color=yellow)

**[Jinxin Shao](https://jinxinshao.github.io/)**

*Submitted to IEEE/CVF Conference 2025*

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Methodology](#-methodology)
- [Results](#-results)
- [Installation](#-installation)
- [Quick Start](#-quick-start)
- [Datasets](#-datasets)
- [Citation](#-citation)
- [Acknowledgments](#-acknowledgments)
- [Contact](#-contact)

---

## 🌊 Overview

**PINE (Physics-Informed Neural Enhancement)** is a novel framework for underwater video enhancement that leverages implicit neural representations guided by physical underwater imaging models. Our method addresses the fundamental challenges of underwater video restoration by incorporating:

- 🌈 **Wavelength-dependent attenuation modeling**
- 💨 **Backscatter compensation**
- ⏱️ **Temporal consistency across frames**
- 🧠 **Unified neural architecture**

Traditional underwater enhancement methods often struggle with color distortion, low contrast, and temporal inconsistencies. PINE overcomes these limitations by embedding physical priors into implicit neural representations, achieving state-of-the-art performance with fewer parameters.

---

## ✨ Key Features

### 🔬 Physics-Informed Design
Our approach integrates the underwater image formation model directly into the neural architecture:
- Models wavelength-dependent light attenuation
- Accounts for depth-varying backscatter
- Preserves physical consistency across the color spectrum

### 🎯 Implicit Neural Representation
- Continuous spatial-temporal representation
- Parameter-efficient architecture
- Natural handling of arbitrary resolutions

### 🎬 Temporal Consistency
- Maintains coherent enhancement across video frames
- No optical flow estimation required
- Smooth transitions without flickering artifacts

### ⚡ Efficient Architecture
- Fewer parameters than existing methods
- Real-time processing capability
- Scalable to high-resolution videos

---

## 🔍 Methodology

<div align="center">
  <img src="Preliminaries.png" alt="PINE Methodology" width="90%">
  <p><em>Overview of the PINE framework: Physics-informed implicit neural representation for underwater video enhancement</em></p>
</div>

Our method consists of three key components:

1. **Physical Modeling Module**: Incorporates the underwater image formation model with wavelength-dependent attenuation
2. **Implicit Neural Representation**: Encodes video frames as continuous functions using coordinate-based networks
3. **Temporal Consistency Module**: Ensures smooth transitions across frames without requiring explicit motion estimation

---

## 📊 Results

### Quantitative Comparison

Performance on the UVEB benchmark dataset:



*Note: ↑ indicates higher is better*

### Qualitative Results

<div align="center">

| Input (Degraded) | LANet (CVPR 2022) | PINE (Ours) |
|:---:|:---:|:---:|
| ![Input](https://via.placeholder.com/300x200/0077be/ffffff?text=Degraded+Input) | ![LANet](https://via.placeholder.com/300x200/00aa66/ffffff?text=LANet) | ![PINE](https://via.placeholder.com/300x200/ff6b35/ffffff?text=PINE+%28Ours%29) |

</div>

### 🎬 Video Comparisons

For video comparisons and more results, please visit our [**Project Page**](https://jinxinshao.github.io/PINE/).

<div align="center">

[![Watch Video Comparisons](https://img.shields.io/badge/▶️_Watch-Video_Comparisons-red?style=for-the-badge)](https://jinxinshao.github.io/PINE/)

</div>

---

## 🚀 Installation

### Prerequisites



### Setup




## 💻 Quick Start

### Training

```bash

```

### Testing

```bash

```

### Inference on Your Own Videos

```bash
# Enhance your underwater video

```

---

## 📁 Datasets

We evaluate PINE on the following benchmarks:

### UVEB (Underwater Video Enhancement Benchmark)




### Data Preparation



## 📖 Citation

If you find this work helpful, please consider citing:

```bibtex
@article{shao2025pine,
  title={PINE: Physics-Informed Neural Enhancement for Underwater Video via Implicit Representation},
  author={Shao, Jinxin},
  journal={arXiv preprint arXiv:XXXX.XXXXX},
  year={2025}
}
```

---

## 🙏 Acknowledgments

This research was supported by [Your Institution/Funding]. We thank the authors of the following projects for their open-source contributions:



---

## 📧 Contact

**Dr. Jinxin Shao**
- 🌐 Website: [https://jinxinshao.github.io/](https://jinxinshao.github.io/)
- 📧 Email: [your.email@institution.edu](mailto:your.email@institution.edu)
- 🐦 GitHub: [@jinxinshao](https://github.com/jinxinshao)

For questions or collaborations, feel free to open an issue or contact me directly.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

### ⭐ Star History

If you find this project helpful, please consider giving it a star! ⭐

[![Star History Chart](https://api.star-history.com/svg?repos=jinxinshao/PINE&type=Date)](https://star-history.com/#jinxinshao/PINE&Date)

---

**Made with ❤️ by the Underwater Vision Community**

</div>
