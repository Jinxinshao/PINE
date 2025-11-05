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

| Method | PSNR ↑ | SSIM ↑ | UIQM ↑ | Parameters | Year |
|:-------|:------:|:------:|:------:|:----------:|:----:|
| WaterNet | 22.43 | 0.856 | 2.87 | 28.6M | ECCV 2019 |
| UGAN | 23.15 | 0.871 | 2.92 | 54.4M | CVPR 2020 |
| FUnIE-GAN | 23.67 | 0.882 | 3.01 | 31.2M | RA-L 2020 |
| LANet | 24.89 | 0.903 | 3.15 | 43.8M | CVPR 2022 |
| PUGAN | 25.12 | 0.908 | 3.18 | 48.3M | TIP 2023 |
| **PINE (Ours)** | **26.34** | **0.927** | **3.34** | **18.7M** | 2025 |

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

- Python >= 3.8
- PyTorch >= 1.10.0
- CUDA >= 11.1 (for GPU acceleration)

### Setup

```bash
# Clone the repository
git clone https://github.com/jinxinshao/PINE.git
cd PINE

# Create a virtual environment
conda create -n pine python=3.8
conda activate pine

# Install dependencies
pip install -r requirements.txt

# Install PyTorch (adjust based on your CUDA version)
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

---

## 💻 Quick Start

### Training

```bash
# Train on UVEB dataset
python train.py --config configs/train_uveb.yaml \
                --data_path /path/to/UVEB \
                --batch_size 4 \
                --epochs 100

# Resume training from checkpoint
python train.py --config configs/train_uveb.yaml \
                --resume checkpoints/latest.pth
```

### Testing

```bash
# Test on a single video
python test.py --checkpoint checkpoints/pine_best.pth \
               --input_video path/to/input.mp4 \
               --output_video path/to/output.mp4

# Test on UVEB test set
python test.py --checkpoint checkpoints/pine_best.pth \
               --test_dir /path/to/UVEB/test \
               --output_dir results/uveb
```

### Inference on Your Own Videos

```bash
# Enhance your underwater video
python inference.py --model checkpoints/pine_best.pth \
                    --input your_video.mp4 \
                    --output enhanced_video.mp4 \
                    --resolution 1920x1080
```

---

## 📁 Datasets

We evaluate PINE on the following benchmarks:

### UVEB (Underwater Video Enhancement Benchmark)
- **Description**: Large-scale underwater video dataset with paired degraded/clean sequences
- **Download**: [UVEB Dataset](https://li-chongyi.github.io/proj_benchmark.html)
- **Statistics**: 890 video clips, 50K+ frames

### UIEB (Underwater Image Enhancement Benchmark)
- **Description**: Widely-used underwater image enhancement dataset
- **Download**: [UIEB Dataset](https://li-chongyi.github.io/proj_benchmark.html)
- **Statistics**: 950 real-world underwater images

### Real-World Test Set
- **Description**: Our collected underwater videos from various marine environments
- **Coming Soon**: Will be released upon paper acceptance

### Data Preparation

```bash
# Organize your data in the following structure:
PINE/
├── data/
│   ├── UVEB/
│   │   ├── train/
│   │   │   ├── input/
│   │   │   └── gt/
│   │   └── test/
│   │       ├── input/
│   │       └── gt/
│   └── UIEB/
│       ├── input/
│       └── gt/
```

---

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

- [LANet](https://github.com/Li-Chongyi/LANet_underwater) for underwater enhancement baselines
- [UVEB Dataset](https://li-chongyi.github.io/proj_benchmark.html) for the benchmark dataset
- [PyTorch](https://pytorch.org/) for the deep learning framework

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
