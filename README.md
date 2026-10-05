<div align="center">

# Syed Muhammad Huzaifa Chishty

### BS Artificial Intelligence · Computer Vision · Retrieval Research · Agent Evaluation

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:syedhuzaifachishty@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SMHC-hub)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/sashinoventures/sash-vpv-subcutaneous-vascular-palm-vein-data)

<br/>

<a href="https://github.com/SMHC-hub">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1200&color=22D3EE&center=true&vCenter=true&width=620&lines=Computer+Vision+%26+Biometrics;Urdu-English+Retrieval+Research;Agent+Behavioral+Evaluation;" alt="Typing Animation: Research Areas " />
</a>

</div>

---

## 🧭 About Me

I recently graduated with a BS in Artificial Intelligence from the National University of Technology (NUTECH), Islamabad (2022–2026), and I am applying to MS/PhD programs abroad. My research investigates how AI systems fail and how to measure those failures reliably across vision, retrieval, and autonomous agents. Rather than relying solely on standard benchmarks, I design empirical evaluation protocols to quantify out-of-distribution drift and cross-dataset degradation.

- 🔬 **Retrieval Evaluation:** Measuring dense embedding degradation on bilingual code-switched queries.
- 👁️ **Medical & Forensic Vision:** Attention-based pathology screening and multimodal synthetic media detection.
- 🖐️ **Biometric Authentication:** Infrared vascular feature extraction and multi-model score-level fusion.
- 🤖 **Agent Reliability:** Continuous integration test gates and statistical drift detection for conversational agents.
- 📊 **Dataset Curation:** Publishing real-world near-infrared biometrics with cross-sensor verification benchmarks.
- 🎓 **Graduate Focus:** Seeking doctoral and masters research groups in empirical AI evaluation and vision systems.

---

## 🎯 Current Focus

| Area | What I'm building |
| :--- | :--- |
| **Vision** | Open-set and EER evaluation for 11-CNN palm-vein fusion across cross-sensor cohorts. |
| **Retrieval** | Quantifying tokenization and embedding collapse under Roman Urdu transliterations on BEIR corpora. |
| **Agents / Evaluation** | Calibrated LLM judges with code-enforced quote verification to eliminate evaluator false positives in CI. |
| **Datasets** | Maintaining the SASH-VPV subcutaneous palm-vein benchmark dataset on Kaggle. |

---

## 🚀 Featured Engineering Projects

### 1. [urdu-english-retrieval-benchmark](https://github.com/SMHC-hub/urdu-english-retrieval-benchmark)

Empirical study measuring how dense retrieval models degrade on Urdu-English code-switched queries against English BEIR corpora.

- **Highlights:**
  - Evaluated 4 dense embedding models (`e5-base-v2`, `bge-base-en-v1.5`, `multilingual-e5-base`, `bge-m3`) across SciFact and NFCorpus.
  - Observed up to a 20.6% nDCG@10 drop on paired code-switched queries; identified `bge-m3` degradation on Roman Urdu transliterations.
- **Stack:** `Python` `BEIR` `sentence-transformers` `PyTorch` `Groq` `Jupyter`

---

### 2. [glaucoma-detection-fyp](https://github.com/SMHC-hub/glaucoma-detection-fyp)

Glaucoma screening pipeline from fundus images combining multi-channel decomposition, attention mechanisms, and visual explanations.

- **Highlights:**
  - EfficientNet-B3 + CBAM on 6-channel composite inputs with CDR-aware loss; achieved AUC 0.9273 on SMDG-19 (89.1% sens., 77.35% spec.).
  - External validation on ACRIMA (705 images) yielded AUC 0.7887 without fine-tuning; documented failed V2 over-parameterization.
- **Stack:** `PyTorch` `timm` `Albumentations` `Grad-CAM` `OpenCV`

```
Fundus (6-Ch) ──> EfficientNet-B3 + CBAM ──> Logits (0.9273 AUC) ──> ACRIMA External (0.7887)
```

---

### 3. [AgentPulse](https://github.com/SMHC-hub/AgentPulse)

Pre-deployment CI behavioral gate and runtime statistical drift monitoring for conversational AI agents.

- **Highlights:**
  - Pre-deployment persona tests with fail-under thresholds and live drift detection using two-proportion z-tests (p < 0.01, Δ ≥ 5%).
  - Calibrated LLM judge with verbatim transcript quote verification, achieving κ = 0.82 agreement with human annotators (n=200).
- **Stack:** `Python` `FastAPI` `Next.js` `PostgreSQL` `Redis` `Docker`

```
Ingest (Traces) ──> PII Scrub ──> LLM Judge (Quote Guard) ──> z-Test Drift ──> CI Gate / Alert
```

---

### 4. [SASH-VPV-Portal](https://github.com/SMHC-hub/SASH-VPV-Portal)

Contactless near-infrared (NIR) palm-vein recognition system and role-based biometric authentication portal.

- **Highlights:**
  - Ctypes wrapper for NIR hardware scanner with sub-second matching; multi-role React frontend (admin, employee, kiosk).
  - Curated and published the SASH-VPV dataset on Kaggle (2,667 images across 122 subjects; Flutter wallet in progress).
- **Stack:** `Python` `PyTorch` `FastAPI` `React` `Flutter` `OpenCV`

---

### 5. [palm-vein-multimodel](https://github.com/SMHC-hub/palm-vein-multimodel)

11-CNN score-level fusion study for contactless palm-vein verification on FYODB (150 classes, 6,000 images).

- **Highlights:**
  - Evaluated score-level fusion across 11 architectures with CLAHE and TTA; external cross-check on PLUSVein.
  - Closed-set accuracy saturates near 100%; open-set and EER evaluation in progress. Team project (Role: Lead Architecture & Fusion).
- **Stack:** `PyTorch` `OpenCV` `scikit-learn` `NumPy`

---

## 🔬 Other AI/ML Projects

| Project | What | Technologies |
| :--- | :--- | :--- |
| [**People-AI**](https://github.com/SMHC-hub/People-AI) | Workforce attrition prediction with XGBoost and SHAP explainability (ROC-AUC 0.942 on synthetic data). | `Vue 3` `Laravel 11` `FastAPI` `XGBoost` `SHAP` |
| [**deepfake-detection**](https://github.com/SMHC-hub/deepfake-detection) | Multimodal forensic baseline combining residual CNN and frozen Wav2Vec2 (ROC-AUC 0.66 with failure analysis). | `PyTorch` `Wav2Vec2` `OpenCV` `Librosa` |
| [**Gesture-Recognition**](https://github.com/SMHC-hub/Gesture-Recognition-Live-Using-Custom-Dataset) | Real-time 36-class alphanumeric sign classification using MediaPipe landmark extraction. | `Python` `TensorFlow` `MediaPipe` `OpenCV` |

---

## 🛠️ Technology Stack

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vue.js&logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white" alt="Laravel" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV" />
</p>

- **Deep Learning & Computer Vision:** `PyTorch` `torchvision` `timm` `Albumentations` `Grad-CAM` `OpenCV` `MediaPipe`
- **Retrieval & NLP:** `sentence-transformers` `BEIR` `HuggingFace Transformers` `Groq API` `Jupyter`
- **Systems & Infrastructure:** `Vue 3` `Laravel 11` `FastAPI` `Python` `Docker` `PostgreSQL` `Redis` `React` `Next.js` `Flutter`
- **Evaluation & Tabular Modeling:** `scikit-learn` `XGBoost` `SHAP` `Two-Proportion z-Test` `Cohen's kappa`

---

## 📐 How I Evaluate

```
Question ──> Data/Split Protocol ──> Baseline ──> Model ──> External Validation ──> Release
```

1. **Negative Results & Honest Reporting:** Report external domain drops upfront (e.g. ACRIMA AUC 0.7887 vs 0.9273 internal; documented failed V2 architecture).
2. **Cross-Domain Generalization:** Validate on independent datasets (ACRIMA, PLUSVein, BEIR) rather than relying solely on saturated closed-set benchmarks.
3. **Evidence-Grounded Evaluators:** Require verbatim transcript quotes in LLM evaluations to prevent false compliance alarms in CI gates.
4. **Paired Measurements:** Evaluate degradation on exact paired subsets (e.g. 136 code-switched queries) rather than masking drops in corpus averages.

---

## 📑 Research and Datasets

- **SASH-VPV Subcutaneous Vascular Palm Vein Dataset:** 2,667 infrared images across 122 subjects captured with specialized NIR sensors for contactless biometric authentication benchmarks.  
  [![Kaggle Dataset](https://img.shields.io/badge/Kaggle-Dataset%20Page-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/sashinoventures/sash-vpv-subcutaneous-vascular-palm-vein-data)

<!-- Preprints placeholder: add entries once submitted/released -->

---

## 🎓 Education

**National University of Technology (NUTECH)** — Islamabad, Pakistan  
*Bachelor of Science in Artificial Intelligence* | 2022 – 2026

- **Core Study Areas:** `Computer Vision` `Deep Learning` `Natural Language Processing` `Machine Learning` `Data Structures & Algorithms` `Probability & Mathematical Statistics` `Linear Algebra`

---

## 📊 GitHub Analytics & Activity

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=SMHC-hub&show_icons=true&bg_color=0b0f19&title_color=22d3ee&text_color=94a3b8&icon_color=38bdf8&border_color=1e293b&hide_border=false&count_private=true" alt="SMHC's GitHub Stats" height="165" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=SMHC-hub&layout=compact&bg_color=0b0f19&title_color=22d3ee&text_color=94a3b8&border_color=1e293b&hide_border=false" alt="Top Languages" height="165" />
</div>

<br/>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=SMHC-hub&background=0b0f19&border=1e293b&stroke=22d3ee&ring=38bdf8&fire=22d3ee&currStreakLabel=38bdf8&sideNums=94a3b8&sideLabels=94a3b8&dates=64748b" alt="GitHub Streak" />
</div>

---

<div align="center">
  <sub>Curated by <a href="https://github.com/SMHC-hub"><b>Syed Muhammad Huzaifa Chishty</b></a></sub>
  <br/>
  <sub><i>Empirical evaluation, transparent baselines, and measurable system behavior.</i></sub>
</div>
