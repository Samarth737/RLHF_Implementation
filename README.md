## About the Project
# RLHF Implementation with Open-Source LLMs

This project demonstrates a full **Reinforcement Learning from Human Feedback (RLHF)** pipeline using open-source language models.
The pipeline includes:

* **Supervised Fine-Tuning (SFT)**
* **Reward Model Training**
* **Policy Optimization using PPO**

The implementation uses the Hugging Face ecosystem (`transformers`, `trl`, `datasets`, etc.) and is designed to run both **locally** and in **Google Colab**.

---

# Environment Setup

The notebooks are designed to automatically configure the environment.

## Option 1 : Run in Google Colab (Recommended)

1. Open any notebook in Google Colab.
2. Run the **first cell** in the notebook.

The setup cell will automatically:

* detect the Colab environment
* clone the repository (if not already present)
* install required dependencies
* set the correct working directory

This setup runs **only once per Colab runtime session**.

---

## Option 2 : Local Setup

Clone the repository:

```bash
git clone https://github.com/Samarth737/rlhf-project.git
cd RLHF_Implementation
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Project Structure

```
RLHF_Implementation/
│
├── notebooks/
│   ├── sft_training.ipynb
│   ├── reward_model_training.ipynb
│   └── ppo_training.ipynb
│
├── models/
│   ├── sft_model/
│   ├── reward_model/
│   └── ppo_model/
│
├── plots/
│   └── training_curves
│
├── requirements.txt
└── README.md
```

---

# RLHF Pipeline Overview

The training pipeline follows the standard RLHF process:

1. **Supervised Fine-Tuning (SFT)**
   The base model is trained on human demonstrations to learn the desired response format.

2. **Reward Model Training**
   A reward model is trained using preference pairs (chosen vs rejected responses).

3. **Policy Optimization (PPO)**
   The policy model is optimized using **Proximal Policy Optimization (PPO)** with the reward model providing feedback.

---

# Dependencies

Main libraries used:

* `torch`
* `transformers`
* `trl`
* `accelerate`
* `datasets`
* `peft`
* `sentencepiece`

Full dependency list is available in:

```
requirements.txt
```

---

# Running the Pipeline

Typical workflow:

1. Run **Supervised Fine-Tuning**
2. Train the **Reward Model**
3. Run **PPO Training**
4. Evaluate the final model

Each stage is implemented in separate notebooks.

---

# Notes for Colab Users

The notebooks include an environment setup cell that:

* clones the repository automatically
* installs dependencies only once per runtime
* ensures the correct working directory

This makes the notebooks **self-contained and reproducible**.

---


## Author
Samarth Neerkaje Saralaya