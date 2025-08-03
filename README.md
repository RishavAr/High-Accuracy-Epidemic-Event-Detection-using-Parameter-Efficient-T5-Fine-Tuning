# High-Accuracy-Epidemic-Event-Detection-using-Parameter-Efficient-T5-Fine-Tuning

# 🚀 Efficient Event Detection using Flan-T5, LoRA, and QLoRA on the SPEED Dataset

This repository benchmarks **full fine-tuning** and **parameter-efficient fine-tuning (PEFT)** techniques (LoRA, QLoRA) on the **SPEED dataset** developed by UCLA for detecting epidemic-related events from Twitter data.

---

## 🧠 STAR Breakdown

### ⭐ Situation
Social media provides timely information for epidemic surveillance, yet detecting meaningful events (e.g., infections, symptoms, deaths) is challenging due to noise and limited labeled data.

### 🎯 Task
Build an efficient event detection framework using state-of-the-art language models and assess trade-offs between full and parameter-efficient fine-tuning on the SPEED dataset.

### ⚙️ Action
- Fine-tuned **Flan-T5**, **T5**, **Flan-T5+LoRA**, and **Flan-T5+QLoRA** on the SPEED dataset using Hugging Face Transformers, PEFT, and Accelerate.
- Used **LoRA (32-bit)** and **QLoRA (4-bit)** to minimize trainable parameters and GPU usage while retaining accuracy.
- Recorded training durations and memory efficiency for real-world deployment benchmarking.

### 🏁 Result
| Model              | Accuracy | Time     | Precision Bits | Method         |
|-------------------|----------|----------|----------------|----------------|
| Flan-T5 (Base)     | **78%**  | 5h 42min | 32-bit         | Full Fine-Tune |
| Flan-T5 + LoRA     | 70%      | 3h 03min | 32-bit         | PEFT (LoRA)    |
| Flan-T5 + QLoRA    | 68%      | 5h 00min | 4-bit          | PEFT (QLoRA)   |
| T5 (Base)          | 67%      | ~6h      | 32-bit         | Full Fine-Tune |

---

## 📦 Dataset: SPEED (UCLA)
- 📄 Title: *Event Detection from Social Media for Epidemic Prediction*  
- 🧪 Description: 1,975 tweets with 2,217 human-annotated event mentions (COVID-19 focused)
- 🧬 Event Types: `infect`, `spread`, `symptom`, `prevent`, `control`, `cure`, `death`
- 🔗 [arXiv Paper (2024)](https://arxiv.org/abs/2404.01679)
- 🗃️ [Official Dataset Repo](https://github.com/PlusLabNLP/SPEED)

> Models trained on SPEED generalize well to unseen epidemics like Monkeypox, Zika, and Dengue.

---

