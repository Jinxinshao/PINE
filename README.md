
# PINE: Physics-Informed Neural Enhancement for Underwater Video via Implicit Representation (submitted)

<div align="center">

**Dr. Jinxin SHAO**

*October 29, 2025*

[![Project Page](https://img.shields.io/badge/Project-Page-blue)](https://jinxinshao.github.io/PINE/)
[![Paper](https://img.shields.io/badge/Paper-PDF-red)](https://drive.google.com/file/d/1o4hoxZ1zBW1VEYeTqmAIkhd5wECrUkYV/view?usp=drive_link)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

</div>

---

## 📋 Overview

This repository contains the official implementation of **PINE (Physics-Informed Neural Enhancement)**, a novel framework for underwater video enhancement that leverages implicit neural representations guided by physical underwater imaging models. Our method addresses the fundamental challenges of underwater video restoration by incorporating wavelength-dependent attenuation, backscatter modeling, and temporal consistency into a unified neural architecture.

![Methodology Overview]({{ site.baseurl }}/Preliminaries.png)

### Key Contributions

Our work makes three significant contributions to underwater video enhancement. First, we introduce a physics-informed implicit neural representation that naturally models the wavelength-dependent light attenuation in underwater environments, which previous learning-based methods often overlook. Second, we propose a novel temporal consistency mechanism that maintains coherent enhancement across video frames without requiring optical flow estimation or complex warping operations. Third, we demonstrate that our physically-grounded approach achieves superior performance on benchmark datasets while using fewer parameters than existing state-of-the-art methods.

---

## 🎬 Qualitative Video Comparisons

This section presents qualitative comparisons among our method (PINE), the input degraded video (Blur), and the ground-truth baseline approach (LANet) from the UVEB dataset. The videos demonstrate our method's ability to recover color information, reduce backscatter, and maintain temporal stability across frames.

<table align="center" style="width:100%; border-collapse: collapse;">
  <thead>
    <tr style="text-align: center;">
      <th style="padding: 10px;">Blur (Input)</th>
      <th style="padding: 10px;">LANet (CVPR 2022)</th>
      <th style="padding: 10px;">PINE (Ours 2025)</th>
    </tr>
  </thead>
  <tbody>
    <tr style="text-align: center;">
      <td style="padding: 10px;">
        <video autoplay loop muted playsinline preload="auto" width="100%" style="max-width: 400px;">
          <source src="https://jinxinshao.github.io/PINE/videos/cv_1000_blur.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </td>
      <td style="padding: 10px;">
        <video autoplay loop muted playsinline preload="auto" width="100%" style="max-width: 400px;">
          <source src="https://jinxinshao.github.io/PINE/videos/cv_1000_LANet.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </td>
      <td style="padding: 10px;">
        <video autoplay loop muted playsinline preload="auto" width="100%" style="max-width: 400px;">
          <source src="https://jinxinshao.github.io/PINE/videos/cv_1000_enhanced.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </td>
    </tr>
  </tbody>
</table>

**Note:** The videos demonstrate our method's effectiveness in handling real-world underwater degradation. Notice how PINE recovers more natural color tones and sharper details compared to the baseline while maintaining smooth temporal transitions.

---



<div align="center">

**⭐ If you find this project helpful, please consider giving it a star! ⭐**

</div>
