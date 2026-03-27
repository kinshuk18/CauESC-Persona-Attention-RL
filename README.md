# 🧠 CauESC with Persona-Attention and Reinforcement Learning for Emotional Support Dialogue

> Enhancing empathetic dialogue systems using **causal reasoning, persona conditioning, and reinforcement learning**

---

## 📌 Overview

Emotional support dialogue systems must understand **why users feel distressed** and respond in a **personalized and empathetic manner**.

This project extends the **CauESC framework** by integrating:

* 🧠 Commonsense reasoning (COMET)
* 👤 Persona-aware modeling (PAL)
* 🎯 Strategy-guided response generation
* ⚡ Reinforcement learning optimization

---

## 🚀 Key Contributions

* **Persona Attention Loop (PAL)**
  Enables bidirectional interaction between persona and dialogue context for personalized response generation.

* **Multi-Factor Decoder**
  Dual cross-attention over:

  * Dialogue context
  * Strategy embeddings
    fused via a gating mechanism.

* **Two-Stage Training Pipeline**

  * Stage 1: Maximum Likelihood Estimation (Pointer-Generator Network)
  * Stage 2: Reinforcement Learning (REINFORCE)

* **Commonsense Knowledge Integration**
  Leveraging COMET for causal and emotional reasoning.

---

## 🧠 Architecture

The system consists of:

* Cause-Aware Encoder
* Persona Attention Loop (PAL)
* Strategy Predictor
* Multi-Factor Decoder
* Pointer-Generator + RL Optimization

---

## 📊 Results

| Metric     | Stage 1 | Stage 2 (Final) |
| ---------- | ------- | --------------- |
| BLEU-4     | 2.66    | **3.92**        |
| ROUGE-L    | 15.76   | **16.91**       |
| METEOR     | 13.22   | **17.37**       |
| Perplexity | 11.95   | **11.41**       |

✔ Reinforcement learning improves response fluency and quality.

---

## 🧪 Ablation Study

| Variant           | Observation                        |
| ----------------- | ---------------------------------- |
| ❌ No PAL          | Reduced persona alignment          |
| ❌ Vanilla Decoder | Weak context-strategy fusion       |
| ❌ No RL           | Lower BLEU/ROUGE, higher diversity |

✔ Each component contributes significantly to performance.

---

## 📦 Dataset

Due to size constraints (**~90GB**), the dataset is not included in this repository.

### Datasets Used:

* **ESConv** (Emotional Support Conversation Dataset)

### Access:

* ESConv: https://aclanthology.org/2021.acl-long.269/

---

## 🔁 Reproducibility

To reproduce results:

1. Download ESConv dataset
2. Preprocess data (tokenization + cleaning)
3. Extract COMET commonsense features
4. Train Stage 1 (MLE - Pointer Generator)
5. Train Stage 2 (Reinforcement Learning)
6. Evaluate using BLEU, ROUGE, METEOR

---

## ⚙️ Experimental Setup

* **GPU:** NVIDIA RTX 6000 Ada
* **Training Time:** ~14 GPU hours
* **Frameworks:**

  * PyTorch
  * HuggingFace Transformers
  * NLGEval

---

## 📁 Repository Structure

```
.
├── report/        # ACM-style research paper
├── results/       # Model outputs, metrics, ablation studies
├── SoP/          # Statement of Purpose
```

---

## 📄 Project Report

👉 [Read Full Report](./Report/Report.pdf)

---

## 🔮 Future Work

* Multi-objective reinforcement learning
* Strategy-aware reward design
* Human evaluation for empathy
* Diversity-aware decoding

---

## ⚠️ Disclaimer

This project is a **research prototype** and not intended for real-world mental health deployment.

---

## 👨‍💻 Author

**Kinshuk Gupta**
B.Tech, Data Science & Artificial Intelligence
IIT Bhilai

---

⭐ If you found this interesting, consider starring the repository!
