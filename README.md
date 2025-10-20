# Real-Time Monocular Depth Enhancement for AR Occlusion

**Author:** Artyom Tsay (Team: Alone)  
**Course:** Computer Vision (Fall 2025)  
**Supervisors:** Dr. I. Atadjanov & Dr. B. Kiani  
**GitHub:** [xts-art/Real-time-monocular-depth-enhancement-for-AR-occlusion](https://github.com/xts-art/Real-time-monocular-depth-enhancement-for-AR-occlusion)

---

## Abstract

Augmented Reality (AR) and Mixed Reality (MR) applications depend on accurate **depth estimation** for realistic **occlusion** between virtual and real-world objects.  
However, monocular depth models in mobile MR headsets often suffer from **temporal instability** and **low accuracy**.  

This project proposes a **real-time monocular depth enhancement** approach that fine-tunes existing models (MiDaS, Depth-Anything) using lightweight, self-supervised adaptation and **temporal smoothing**.  
The goal is to achieve **smoother**, **more stable**, and **efficient** depth maps suitable for real-time AR occlusion rendering.

---

## Problem & Motivation

- Current monocular depth estimators on mobile AR/MR devices produce **noisy** and **flickering** depth maps.
- These artifacts reduce immersion by causing poor occlusion and “ghosting” effects.
- The project aims to **improve temporal and spatial consistency** of depth predictions while keeping inference real-time (<50 ms per frame).

---

## Related Work

- **MiDaS** and **Depth-Anything** introduced robust depth estimation via transformer backbones and dataset mixing.  
- **FastDepth** optimized CNNs for embedded inference.  
- **DPT-Video** and **optical-flow-guided refinement** improved temporal consistency.  
- This project builds upon these methods with a **temporal smoothing module** and **lightweight fine-tuning** for AR-specific occlusion.

---

## Data & Resources

**Datasets:**
- KITTI, NYU Depth V2, TUM RGB-D  
- Synthetic AR sequences (Blender / Unity)

**Frameworks & Tools:**
- PyTorch, OpenCV, ONNX Runtime

**Hardware:**
- Google Colab Pro (T4 GPU)  
- Local: RTX 3060 laptop GPU

---

## Method Overview

1. **Input:** RGB frame from AR headset passthrough  
2. **Depth Estimation:** Pre-trained MiDaS or Depth-Anything  
3. **Temporal Smoothing:** Recurrent or optical flow–based filtering  
4. **Self-Supervised Adaptation:** Fine-tuning using pseudo-stereo data  
5. **Output:** Enhanced depth map for AR occlusion rendering  

**Optimization:**  
Model quantized and exported to ONNX for low-latency inference.

---

## Evaluation Metrics

| Metric | Description |
|---------|--------------|
| RMSE | Root Mean Square Error |
| AbsRel | Absolute Relative Error |
| SSIM | Structural Similarity |
| Temporal Flicker Index | Stability across frames |

**Success Criteria:**
- ≥10% RMSE improvement over baseline  
- <50 ms per-frame latency  
- Visibly smoother occlusion boundaries  

---

## Risks & Mitigations

| Risk | Mitigation |
|------|-------------|
| Limited GPU capacity | Use LoRA or smaller model variants |
| Temporal instability | Optical flow correction / EMA smoothing |
| Dataset mismatch | Synthetic-to-real fine-tuning |

---

## Timeline

| Week | Task |
|------|------|
| W1 | Literature review, dataset setup |
| W2 | Baseline MiDaS fine-tuning |
| W3 | Add temporal smoothing |
| W4 | Implement self-supervised adaptation |
| W5 | ONNX optimization and deployment |
| W6 | Evaluation and final report/demo |

---

## Expected Outcomes

- Real-time depth enhancement model for AR occlusion  
- Demo video showcasing improved stability and realism  
- Final report + open-source code on GitHub  

**Stretch goal:** Unity integration for real-time headset visualization.

---

## Ethics & Compliance

- Uses publicly available datasets (MIT/CC BY).  
- No personal or biometric data collected.  
- Pretrained models credited and used per their licenses.  

---

## References

1. Ranftl et al., *Towards Robust Monocular Depth Estimation*, IEEE TPAMI 2022  
2. Ranftl et al., *Vision Transformers for Dense Prediction Tasks*, ICCV 2021  
3. Yang et al., *Depth Anything*, arXiv 2024  
4. Wofk et al., *FastDepth*, ICRA 2019  
5. Liu et al., *Video Depth Estimation with Optical Flow Guidance*, CVPRW 2020  
6. Apple, *ARKit Depth API*, 2023  
7. Google, *ARCore Depth API*, 2022  
