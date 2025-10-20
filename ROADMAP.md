# ROADMAP — Real-Time Monocular Depth Enhancement for AR Occlusion
**Team:** Alone  
**Member:** Artyom Say (ID: 220748)  
**Course:** Computer Vision – Fall 2025  
**Supervisors:** Dr. I. Atadjanov & Dr. B. Kiani  
**Repo:** [xts-art/Real-time-monocular-depth-enhancement-for-AR-occlusion](https://github.com/xts-art/Real-time-monocular-depth-enhancement-for-AR-occlusion)

---

## Scope
This project develops a **real-time monocular depth enhancement** system for **AR occlusion** in mixed reality headsets.  
It fine-tunes lightweight monocular depth models (MiDaS / Depth Anything) with **temporal smoothing** and **self-supervised adaptation**,  
aiming for temporally stable, spatially accurate, and efficient depth estimation suitable for **mobile or embedded AR GPUs**.

**Key Metrics:**  
- RMSE, AbsRel (accuracy)  
- SSIM (structural similarity)  
- Temporal Flicker Index (stability)  
- Latency (end-to-end <50 ms)  

---

## Milestones (Tashkent time)

### **W1 · Oct 27 – Nov 2**
Repository setup, baseline MiDaS/Depth-Anything integration, CI structure, initial dataset preparation.  
**Owner:** Artyom Say  
**Deliverable:** Repo initialized with working baseline.  
**Status:** Planned

---

### **W2 · Nov 3 – Nov 9**
Baseline fine-tuning on small dataset (KITTI/NYU/TUM).  
Compute baseline metrics (RMSE, AbsRel, SSIM).  
**Owner:** Artyom Say  
**Deliverable:** Baseline model trained and benchmarked.  
**Status:** Planned

---

### **W3 · Nov 10 – Nov 16**
Add temporal smoothing layer (optical-flow or recurrent filtering).  
Evaluate stability improvements (Temporal Flicker Index).  
**Owner:** Artyom Say  
**Deliverable:** Temporally stabilized model v1.  
**Status:** Planned

---

### **W4 · Nov 17 – Nov 23**
Implement self-supervised pseudo-stereo fine-tuning.  
Train on synthetic-to-real blended dataset (Blender / Unity).  
**Owner:** Artyom Say  
**Deliverable:** Self-adaptive model v2 with improved temporal consistency.  
**Status:** Planned

---

### **W5 · Nov 24 – Nov 30**
Quantize and export model to **ONNX Runtime** for mobile inference.  
Latency profiling on RTX 4080 (local) and Colab (T4).  
**Owner:** Artyom Say  
**Deliverable:** Real-time model (latency <50 ms).  
**Status:** Planned

---

### **W6 · Dec 1 – Dec 7**
Final evaluation and visualization.  
Compare temporal and spatial quality across test videos.  
Generate demo sequence for AR occlusion.  
**Owner:** Artyom Say  
**Deliverable:** Evaluation report + demo video draft.  
**Status:** Planned

---

### **W7 · Dec 8 – Dec 14**
Conduct ablation experiments:  
- With vs. without temporal smoothing  
- With vs. without self-supervised tuning  
Analyze trade-offs in latency and quality.  
**Owner:** Artyom Say  
**Deliverable:** Ablation summary table + plots.  
**Status:** Planned

---

### **W8 · Dec 15 – Dec 21**
Prepare final report (PDF), README polish, and GitHub release.  
Include side-by-side comparison visuals and code documentation.  
**Owner:** Artyom Say  
**Deliverable:** Final paper-ready report.  
**Status:** Planned

---

### **W9 · Dec 22 – Dec 27**
Final demo recording, repository cleanup, and presentation slides.  
Submit final version for grading (midterm + final).  
**Owner:** Artyom Say  
**Deliverable:** Demo video, slides, and GitHub repo submission.  
**Status:** Planned

---

## Success Criteria
- **≥10% RMSE improvement** vs baseline  
- **<50 ms** per-frame latency  
- **SSIM ≥ 0.90**  
- **Reduced temporal flicker (≥20% stability gain)**  
- Visually smoother occlusion boundaries in demo video  

---

## Risks and Mitigations

| Risk | Mitigation |
|------|-------------|
| Limited GPU resources | Use LoRA fine-tuning and reduced model variants |
| Temporal instability under motion | Optical flow correction or EMA smoothing |
| Domain mismatch between synthetic and real data | Synthetic-to-real adaptation, pseudo-stereo tuning |
| Latency exceeding real-time threshold | Quantization and ONNX optimization |
| Insufficient visual improvement | Combine perceptual loss and temporal loss terms |

---

## Weekly Check-ins
- Update this file weekly with 3–5 key progress notes.  
- Link commits or issues to specific milestones.  
- Include screenshots or metric tables where relevant.  

---

## Deliverables
- Full reproducible code (training, inference, ONNX export).  
- Enhanced monocular depth model for AR occlusion.  
- Evaluation report with metrics and visual results.  
- Demo video showing improved occlusion quality.  
- (Stretch goals) Unity integration for real-time headset visualization.

---

## Links
- **Proposal Document (PDF):** `CV25_Proposal_Alone.pdf`  
- **Maintained ROADMAP.md:** In project repo  
- **Weekly progress updates:** GitHub Issues + Commits  
- **Demo repo:** [xts-art/Real-time-monocular-depth-enhancement-for-AR-occlusion](https://github.com/xts-art/Real-time-monocular-depth-enhancement-for-AR-occlusion)
