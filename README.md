# Explainable Fault Diagnosis using Vibration Signal Decomposition

📌 **Master’s Thesis & Summer Internship Project (IIT Kharagpur)**  
AI-driven fault diagnosis framework for machinery (rail bogies, industrial gears, induction motors)  
using vibration signals collected via accelerometers.  

---

## 🔬 Problem Statement
Machinery faults are challenging to detect early. Vibration signals carry hidden fault signatures,  
but require decomposition and explainability for robust detection.

---

## 🚀 Methodology
- Applied **Empirical Mode Decomposition (EMD)** to extract up to 5 Intrinsic Mode Functions (IMFs).  
- Constructed multiple signal sets: Raw, IMF1 only, IMF1–3, IMF2–5, etc.  
- Two pipelines:
  - **Deep Learning:** Converted signals into images → CNN models.
  - **Machine Learning:** FAST + SIFT + Visual Bag of Words + Statistical features → XGBoost, LightGBM.
- Used **SHAP interpretability** and **IMF corruption (ablation) studies** to validate IMF importance.

---

## 📊 Results
- Achieved **~96% accuracy**, with IMF-based signals outperforming raw signals by 3–5%.  
- Found **lower-order IMFs (IMF1–3)** are most discriminative, reducing complexity without accuracy loss.  
- **SHAP**: IMF1 > IMF2 > IMF3 globally, IMF2 slightly stronger in normal class.  
- **Ablation**: Removing IMF1 caused the largest performance drop → IMF1 is dominant.  

---

## 🛠️ Tech Stack
- Python, PyTorch, NumPy, SciPy, Scikit-learn  
- EMD, SHAP, CNN, XGBoost, LightGBM  
- FFT & Vibration Signal Analysis  

---

## Project Notebooks
The analysis and results are available as interactive Colab notebooks:
- [Metro Dataset](https://colab.research.google.com/drive/1F0SzVm8ZBbh3JE6w1E6z519LvEOb4DZj?usp=sharing)
- [EH Dataset](https://colab.research.google.com/drive/16pVy-byRyyF14LAa673d5quHoEp7LdCn?usp=sharing)
- [Induction Motor Dataset](https://colab.research.google.com/drive/1Zv7L4g4M5pTZ8KUgLVbgi5CSbQyHjNXV?usp=sharing)
- [Gear Dataset](https://colab.research.google.com/drive/1MOeJe1W1Wj_UiBmvBF1jSKHjuV4VjJD_?usp=sharing)
