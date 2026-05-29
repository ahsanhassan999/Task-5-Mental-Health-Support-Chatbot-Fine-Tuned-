# Task 5: Mental Health Support Chatbot (Fine-Tuning & Gemini Runtime)

This repository contains the implementation for **Task 5: Mental Health Support Chatbot** as part of the AI/ML Engineering Internship at DevelopersHub Corporation.

## Objective
The goal is to design an empathetic conversational chatbot supporting users dealing with stress, anxiety, or emotional wellness.

## Approach & Dual-Structure
Due to local computing hardware constraints on training and running deep LLMs locally, we implement a **hybrid dual-structure**:
1. **Fine-Tuning Template (GPU-Ready)**: Executable cells that demonstrate loading Facebook's `EmpatheticDialogues` dataset and fine-tuning a `DistilGPT2` model using the Hugging Face `Trainer` API (ready for Google Colab/Kaggle GPUs).
2. **Empathetic Gemini Runtime (CPU-Ready)**: A runtime implementation using Google Gemini's **Gemini 2.5 Flash Lite** model and custom system instructions defining an empathetic Active-Listening persona.
3. **Failsafe Offline Fallback**: In the absence of an API key or during network timeouts, the chatbot automatically switches to locally simulated responses.

## Setup & Execution
Install the lightweight Google Generative AI package:
```bash
pip install google-generativeai
```

### API Configuration
Input your Google Gemini API key when prompted by `getpass` inside the notebook, or leave it blank to run in offline simulation mode.

## Structure
- `task_5_mental_health.ipynb`: The Jupyter Notebook containing the fine-tuning workflow template, the Gemini-based empathetic companion logic, and mock offline test cases.
