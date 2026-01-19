# 🛡️ SRNet-Steganalysis-PoC: Digital Forensics with Deep Learning

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.1.2-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Research_Prototype-yellow)

> **Official implementation of SRNet architecture for detecting S-UNIWARD steganography.** > *Research conducted at VNU-IS (Vietnam National University - International School).*

## 📖 Overview
This project implements the **SRNet (Steganalysis Residual Network)** architecture to detect hidden steganographic payloads in digital imagery. Unlike traditional CNNs, SRNet is designed to suppress image content and amplify faint **noise residuals**, making it highly effective against adaptive algorithms like **S-UNIWARD** and **WOW**.

## 🚀 Key Features
* **🏆 State-of-the-Art Accuracy:** Achieved **99.95% detection rate** on the BOSSBase v1.01 dataset at 0.4 bpp payload.
* **🧠 Curriculum Learning:** Implemented a robust training strategy (starting from 0.7 bpp $\to$ 0.4 bpp) to prevent convergence failure.
* **🔍 Explainable AI (XAI):** Integrated **Grad-CAM** to generate heatmaps, visualizing and localizing hidden payloads in high-texture regions.
* **⚡ Optimization:** Customized for efficient inference on consumer-grade GPUs (tested on NVIDIA GTX 1650 & Tesla T4).

## 🛠️ Tech Stack
* **Core Framework:** PyTorch
* **Algorithms:** SRNet (Deep Residual Learning), S-UNIWARD (Spatial Domain).
* **Tools:** OpenCV, NumPy, SciPy, Gradio (for Web Demo).

## 📊 Experimental Results
| Payload (bpp) | Accuracy | AUC Score | Status |
| :--- | :--- | :--- | :--- |
| **0.4** | **99.95%** | **1.0000** | Expert |
| 0.2 | 87.10% | 0.9119 | Robust |
| 0.1 | 62.40% | 0.6602 | Physical Limit |

*Note: Results based on BOSSBase v1.01 (Grayscale, 256x256).*

## ⚠️ Limitations & Future Work
1.  **S-UNIWARD Simulation:** The data generator uses a *fast spatial high-pass filter approximation* instead of the original C++ implementation to optimize training speed.
2.  **JPEG Robustness:** Current model is optimized for RAW/PGM formats. Performance on compressed JPEG images is a subject for future research.

## 🔗 Credits & Acknowledgements
This project is built for educational and research purposes. We gratefully acknowledge the following works:

**1. Original Paper & Architecture:**
* *Boroumand, M., Chen, M., & Fridrich, J. (2018).* "Deep Residual Network for Steganalysis of Digital Images." IEEE Transactions on Information Forensics and Security.
* *Holub, V., Fridrich, J., & Denemark, T. (2014).* "Universal distortion function for steganography."

**2. Code References:**
* This implementation is inspired by the original SRNet concepts.
* **Special thanks to:** "https://github.com/TracyCuiq/S-UNIWARD-python.git",  "https://github.com/milesial/Pytorch-UNet.git" for the base structure of the data loader/model. *(Ví dụ: Thanks to `bboroumand` for the Matlab implementation reference)*.

---
**Author:** Arthur Pham-dragon  
**Contact:** 080at080@gmail.com
