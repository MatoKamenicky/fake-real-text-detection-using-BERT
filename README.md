# Fake or Real: The Impostor Hunt (BERT)

This repository contains my work-in-progress solution for the [Kaggle "Fake or Real: The Impostor Hunt" competition](https://www.kaggle.com/competitions/fake-or-real-the-impostor-hunt).  
The goal is to detect fake texts from real ones in space-related documents, where both real and fake versions have been significantly modified using Large Language Models (LLMs).

## 📌 Competition Overview
- **Dataset**: Pairs of texts — one real and one fake — related to space research and projects.
- **Task**: Binary classification (Real vs Fake).
- **Challenge**: The fake and real texts are heavily modified by LLMs, making rule-based approaches unreliable.
- **Organizers**: ESA's European Space Operations Centre (ESOC) — part of the DataX initiative for AI security in space applications.

## 🧠 Current Approach
- Model: The model uses **DeBERTaV3-base** as the encoder with a custom multi-layer classification head
- Strategy:
  - Each text in a pair is treated individually for binary classification (Real vs Fake).
  - After classification, the pair is compared, and the text with the higher probability of being real is selected.

*(This approach is still under development — model architecture, preprocessing, and training strategy may change.)*
