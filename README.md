# SRNet-Steganalysis-PoC
Official implementation of SRNet for Steganalysis against S-UNIWARD algorithm


# SRNet: Deep Learning for Digital Forensics 

An implementation of the **SRNet (Steganalysis Residual Network)** architecture for detecting steganographic payloads in digital imagery. This project focuses on identifying **S-UNIWARD** and **WOW** algorithms using Deep Residual Learning.

# Key Features
- **High Accuracy:** Achieved **~90%** detection rate on BOSSBase v1.01 dataset (Payload 0.4 bpp).
- **Curriculum Learning:** Implemented a multi-stage training strategy (0.7 bpp -> 0.4 bpp) for stable convergence.
- **Explainable AI:** Integrated **Grad-CAM** to visualize and localize hidden payloads (Heatmap generation).
- **Hardware Optimization:** Customized for inference on consumer-grade GPUs (NVIDIA GTX 1650).

# Tech Stack
- **Core Framework:** PyTorch / TensorFlow
- **Algorithms:** SRNet, S-UNIWARD
- **Tools:** OpenCV, NumPy, Matplotlib, Gradio (for Web Demo)

# Methodology
1. **Preprocessing:** No-Pooling layers (L1-L7) to preserve noise residuals.
2. **Training:** Used Paired Training (Cover/Stego) with Data Augmentation.
3. **Evaluation:** Sensitivity analysis against adaptive steganography.

# Project Structure
- `SRNet_Model_Training.ipynb`: Main notebook for model training and evaluation.
- `Final_Report_SRNet_Research.pdf`: Full research documentation and experimental results.

---
### 🔗 Credits & Acknowledgements
- Based on the paper *"SRNet: Deep Residual Network for Steganalysis"*.
- Research conducted at **VNU-IS** (Vietnam National University).
