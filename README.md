# Unsupervised Anomaly Detection in Brain MRI via Disentangled Anatomy Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Medical Image Analysis](https://img.shields.io/badge/Journal-Medical%20Image%20Analysis-blue)](https://doi.org/10.1016/j.media.2025.103922)
[![arXiv](https://img.shields.io/badge/arXiv-2512.21924-b31b1b.svg)](https://arxiv.org/abs/2512.21924)

This repository is the official implementation of the paper: **Unsupervised Anomaly Detection in Brain MRI via Disentangled Anatomy Learning (DAL)**.

## 📝 Abstract
Detection of various lesions in brain MRI is clinically critical, but challenging due to the diversity of lesions and variability in imaging conditions. Current unsupervised learning methods detect anomalies mainly through reconstructing abnormal images into pseudo-healthy images (PHIs) by normal samples learning and then analyzing differences between images. However, these unsupervised models face two significant limitations: restricted generalizability to multi-modality and multi-center MRIs due to their reliance on the specific imaging information in normal training data, and constrained performance due to abnormal residuals propagated from input images to reconstructed PHIs. To address these limitations, two novel modules are proposed, forming a new PHI reconstruction framework. Firstly, the disentangled representation module is proposed to improve generalizability by decoupling brain MRI into imaging information and essential imaging-invariant anatomical images, ensuring that the reconstruction focuses on the anatomy. Specifically, brain anatomical priors and a differentiable one-hot encoding operator are introduced to constrain the disentanglement results and enhance the disentanglement stability. Secondly, the edge-to-image restoration module is designed to reconstruct high-quality PHIs by restoring the anatomical representation from the high-frequency edge information of anatomical images, and then recoupling the disentangled imaging information. This module not only suppresses abnormal residuals in PHI by reducing abnormal pixels input through edge-only input, but also effectively reconstructs normal regions using the preserved structural details in the edges. Evaluated on nine public datasets (4,443 patients’ MRIs from multiple centers), our method outperforms 17 state-of-the-art methods, achieving absolute improvements of +18.32 % in average precision and +13.64 % in Dice similarity coefficient.

## 📅 Coming Soon
The full code will be released soon. We are currently organizing the code to make it user-friendly.

## 🖼️ Method Overview
The overall framework of the proposed **DAL** method is shown below:

![Method Overview](Framework.png)

## 📖 Citation
If you find this work useful for your research, please cite our paper:

```bibtex
@article{Yang2026DAL,
  title   = {Unsupervised anomaly detection in brain MRI via disentangled anatomy learning},
  journal = {Medical Image Analysis},
  volume  = {109},
  pages   = {103922},
  year    = {2026},
  issn    = {1361-8415},
  doi     = {10.1016/j.media.2025.103922},
  url     = {[https://doi.org/10.1016/j.media.2025.103922](https://doi.org/10.1016/j.media.2025.103922)},
  author  = {Tao Yang and Xiuying Wang and Hao Liu and Guanzhong Gong and Lian-Ming Wu and Yu-Ping Wang and Lisheng Wang}
}
