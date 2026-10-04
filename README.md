<div align="center">

# Syed Muhammad Huzaifa Chishty

### BS Artificial Intelligence · Computer Vision · Retrieval Research · Agent Evaluation

[![Email](https://img.shields.io/badge/Email-syedhuzaifachishty%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:syedhuzaifachishty@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-SMHC--hub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SMHC-hub)
[![Kaggle](https://img.shields.io/badge/Kaggle-SASH--VPV%20Dataset-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/sashinoventures/sash-vpv-subcutaneous-vascular-palm-vein-data)

<br/>

<a href="https://github.com/SMHC-hub">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1200&color=22D3EE&center=true&vCenter=true&width=620&lines=Computer+Vision+%26+Biometrics;Urdu-English+Retrieval+Research;Agent+Behavioral+Evaluation;Applying+for+MS%2FPhD+Programs" alt="Typing Animation: Research Areas and MS/PhD Applicant" />
</a>

</div>

---

## 🧭 About Me

I recently graduated with a BS in Artificial Intelligence from the National University of Technology (NUTECH), Islamabad (2021–2025), and I am applying to MS/PhD programs abroad. My research investigates how modern AI systems fail and how to measure those failures reliably across computer vision, information retrieval, and autonomous agents. Rather than focusing only on closed-set benchmark accuracy, I design protocols to measure out-of-distribution drift, cross-dataset degradation, and evaluator hallucination.

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
| **Vision** | Open-set and equal error rate (EER) evaluation for 11-CNN palm-vein fusion across cross-sensor cohorts. |
| **Retrieval** | Quantifying tokenization and embedding collapse under Roman Urdu orthographic variability on BEIR corpora. |
| **Agents / Evaluation** | Calibrated LLM judges with code-enforced quote verification to eliminate evaluator false positives in CI. |
| **Datasets** | Preparing annotation and protocol updates for the SASH-VPV subcutaneous palm-vein corpus on Kaggle. |

---

## 🚀 Featured Engineering Projects

### 1. [urdu-english-retrieval-benchmark](https://github.com/SMHC-hub/urdu-english-retrieval-benchmark)

Empirical study measuring how four dense embedding models handle Urdu-English code-switched queries (native script and Roman Urdu) against English BEIR corpora.

- **Highlights:**
  - Evaluated `e5-base-v2`, `bge-base-en-v1.5`, `multilingual-e5-base`, and `bge-m3` on SciFact and NFCorpus datasets.
  - Queries generated with LLaMA 3.3-70B via Groq and spot-checked across 50 manual samples.
  - Observed up to a 20.6% nDCG@10 drop for `bge-base-en-v1.5` on NFCorpus (measured on the paired 136-query code-switched subset).
  - Identified that `bge-m3` substantially degrades on Roman Urdu due to out-of-vocabulary Latin transliteration patterns.
  - Fully reproducible through numbered Jupyter notebooks (01 to 08).
- **Stack:** `Python` `BEIR` `sentence-transformers` `PyTorch` `Groq` `Jupyter`

---

### 2. [glaucoma-detection-fyp](https://github.com/SMHC-hub/glaucoma-detection-fyp)

Computer-aided glaucoma screening pipeline from fundus images combining multi-channel decomposition, attention mechanisms, and visual explanations.

- **Highlights:**
  - EfficientNet-B3 backbone with Convolutional Block Attention Modules (CBAM) applied to 6-channel composite inputs.
  - Trained with Cup-to-Disc Ratio (CDR) loss guidance, test-time augmentation, and Grad-CAM interpretability.
  - Achieved AUC 0.9273 on the SMDG-19 benchmark with 89.1% sensitivity at 77.35% specificity (threshold 0.35).
  - Validated external generalization on ACRIMA (705 images from independent hardware) yielding AUC 0.7887 without fine-tuning.
  - Documented full version history (V1 to V2.1), including an honest failure analysis of V2 architecture over-parameterization.
- **Stack:** `PyTorch` `timm` `Albumentations` `Grad-CAM` `OpenCV`

```
+-------------------------------------------------------+
| 6-Channel Fundus Input (RGB, CLAHE Disc, Cup, Vessel) |
+---------------------------+---------------------------+
                            |
                            v
+-------------------------------------------------------+
|  EfficientNet-B3 Backbone + CBAM (Channel & Spatial)  |
+---------------------------+---------------------------+
                            |
             +--------------+--------------+
             |                             |
             v                             v
+-------------------------+   +-------------------------+
| Classification Logits   |   | Cup-to-Disc Ratio (CDR) |
| (SMDG-19 AUC: 0.9273)   |   | Loss Guidance           |
+-------------------------+   +-------------------------+
             |
             v
+-------------------------------------------------------+
| External Validation on ACRIMA (AUC: 0.7887, No Tuning)|
+-------------------------------------------------------+
```

---

### 3. [AgentPulse](https://github.com/SMHC-hub/AgentPulse)

Continuous integration quality gate and runtime behavioral drift monitoring platform for conversational AI agents.

- **Highlights:**
  - Automated pre-deployment behavioral test suites executed against simulated personas with configurable fail-under thresholds.
  - Post-deployment drift monitoring using two-proportion z-tests (p < 0.01, Δ ≥ 5%) and Welch's t-tests.
  - Calibrated LLM judge enforcing verbatim transcript quote verification, cutting evaluator false positives.
  - Measured judge agreement of κ = 0.82 against 200 human-annotated conversation samples.
  - Packaged as a standalone Python SDK with a FastAPI backend and interactive Next.js dashboard.
- **Stack:** `Python` `FastAPI` `Next.js` `PostgreSQL` `Redis` `Docker` `Groq`

```
+-------------------------------------------------------+
| Ingest: Python SDK Traces -> PII Scrubber -> Queue   |
+---------------------------+---------------------------+
                            |
                            v
+-------------------------------------------------------+
| Judge: LLM Evaluator + Verbatim Quote Verification    |
| (Human-Judge Agreement: kappa = 0.82 on n=200)        |
+---------------------------+---------------------------+
                            |
                            v
+-------------------------------------------------------+
| Drift: Two-Proportion z-Test (p < 0.01, Delta >= 5%)  |
+---------------------------+---------------------------+
                            |
                            v
+-------------------------------------------------------+
| Alert: Slack Dispatcher & 1-Click CI Test Synthesizer |
+-------------------------------------------------------+
```

---

### 4. [SASH-VPV-Portal](https://github.com/SMHC-hub/SASH-VPV-Portal)

Contactless near-infrared (NIR) palm-vein recognition system and biometric payment portal.

[![Kaggle Dataset](https://img.shields.io/badge/Kaggle-SASH--VPV%20Subcutaneous%20Data-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/sashinoventures/sash-vpv-subcutaneous-vascular-palm-vein-data)

- **Highlights:**
  - Python ctypes wrapper for the NIR hardware capture SDK with real-time video streaming.
  - High-throughput FastAPI backend managing enrollment, template matching, and authentication audit logs.
  - Role-based React web application supporting admin, employee, shop-owner, and self-service kiosk workflows.
  - Companion mobile wallet implementation in progress using Flutter.
  - Curated and published the SASH-VPV dataset on Kaggle (2,667 images across 122 subjects).
- **Stack:** `Python` `PyTorch` `FastAPI` `React` `Flutter` `OpenCV`

---

### 5. [palm-vein-multimodel](https://github.com/SMHC-hub/palm-vein-multimodel)

Multi-model score-level fusion study evaluating 11 CNN architectures for contactless palm-vein verification.

- **Highlights:**
  - Benchmark on FYODB (150 classes, 6,000 NIR images) with CLAHE preprocessing and test-time augmentation.
  - Evaluated score-level fusion across ResNet, EfficientNet, DenseNet, MobileNet, and VGG variants.
  - Cross-dataset verification check conducted on the external PLUSVein corpus.
  - Identifies that while closed-set recognition saturates near 100%, open-set verification and EER remain the true test of discriminative capability (in progress).
  - FYP team research project; role: Lead Architecture & Ensemble Fusion. Conducted under faculty supervision at NUTECH with student team collaborators.
- **Stack:** `PyTorch` `OpenCV` `scikit-learn` `NumPy`

---

## 🔬 Other AI/ML Projects

| Project | What | Technologies |
| :--- | :--- | :--- |
| [**People-AI**](https://github.com/SMHC-hub/People-AI) | Workforce attrition risk prediction with XGBoost and SHAP explainability (ROC-AUC 0.942 on synthetic data). | `Python` `FastAPI` `XGBoost` `SHAP` `React` |
| [**deepfake-detection**](https://github.com/SMHC-hub/deepfake-detection) | Multimodal forensic baseline combining residual CNN and frozen Wav2Vec2 audio features (ROC-AUC 0.66 with documented failure analysis). | `PyTorch` `Wav2Vec2` `OpenCV` `Librosa` |
| [**Gesture-Recognition**](https://github.com/SMHC-hub/Gesture-Recognition-Live-Using-Custom-Dataset) | Real-time 36-class alphanumeric sign and hand gesture classification using MediaPipe landmark extraction. | `Python` `TensorFlow` `MediaPipe` `OpenCV` |

---

## 🛠️ Technology Stack

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV" />
</p>

- **Deep Learning & Computer Vision:** `PyTorch` `torchvision` `timm` `Albumentations` `Grad-CAM` `OpenCV` `MediaPipe`
- **Retrieval & NLP:** `sentence-transformers` `BEIR` `HuggingFace Transformers` `Groq API` `Jupyter`
- **Systems & Infrastructure:** `FastAPI` `Python` `Docker` `PostgreSQL` `Redis` `React` `Next.js` `Flutter`
- **Evaluation & Tabular Modeling:** `scikit-learn` `XGBoost` `SHAP` `Two-Proportion z-Test` `Cohen's kappa`

---

## 📐 How I Evaluate

```
  [ Question ]
       |  Formulate failure mode or degradation hypothesis
       v
  [ Protocol ]
       |  Leak-free split; paired subsets; stratified folds
       v
  [ Baseline ]
       |  Simpler reference model; zero-shot or raw English
       v
  [ Model ]
       |  Target architecture, loss design, or ensemble
       v
  [ External Validation ]
       |  Cross-dataset tests (ACRIMA, PLUSVein, BEIR)
       v
  [ Limitations ]
       |  Document drops, failure modes, and bounds
       v
  [ Release ]
       |  Reproducible code, checkpoints, and datasets
```

1. **Negative Results & Honest Reporting:** If a model drops on external data, report it upfront. In `glaucoma-detection-fyp`, while the internal SMDG-19 score reached 0.9273, the external ACRIMA score dropped to 0.7887 without fine-tuning, and the failed V2 over-parameterization is documented.
2. **Cross-Domain Generalization:** Closed-set performance often hides real-world failure. Evaluating palm-vein models on PLUSVein and medical models on independent clinical cohorts is necessary to assess real utility.
3. **Evidence-Grounded Evaluators:** When using LLMs as judges, require verbatim quote verification against raw conversation text to prevent the judge from hallucinating false compliance failures.
4. **Isolated Paired Measurements:** Avoid diluting failure rates across unchanged queries. In `urdu-english-retrieval-benchmark`, degradation is reported on the exact paired 136 code-switched subset to capture the true 20.6% drop rather than obscuring it in corpus averages.

---

## 📑 Research and Datasets

- **SASH-VPV Subcutaneous Vascular Palm Vein Dataset:** 2,667 infrared images across 122 subjects captured with specialized NIR sensors for contactless biometric authentication benchmarks.  
  [![Kaggle Dataset](https://img.shields.io/badge/Kaggle-Dataset%20Page-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/sashinoventures/sash-vpv-subcutaneous-vascular-palm-vein-data)

<!-- Preprints placeholder: add entries once submitted/released -->

---

## 🎓 Education

**National University of Technology (NUTECH)** — Islamabad, Pakistan  
*Bachelor of Science in Artificial Intelligence* | 2021 – 2025

- **Core Study Areas:** `Computer Vision` `Deep Learning` `Natural Language Processing` `Machine Learning` `Data Structures & Algorithms` `Probability & Mathematical Statistics` `Linear Algebra`

---

## 🤝 Let's Connect

<div align="center">

[![Email](https://img.shields.io/badge/Email-syedhuzaifachishty%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:syedhuzaifachishty@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-SMHC--hub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SMHC-hub)
[![Kaggle](https://img.shields.io/badge/Kaggle-SASH--VPV-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/sashinoventures/sash-vpv-subcutaneous-vascular-palm-vein-data)

<br/>

Empirical evaluation, transparent baselines, and measurable system behavior.

</div>
