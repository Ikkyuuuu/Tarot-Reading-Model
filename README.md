# Tarot-Reading-Model

A fine-tuned **Phi-3 Mini** model for generating **3-card tarot readings** from a user question and the drawn cards.  
This project focuses on producing short, structured interpretations suitable for local inference.
<br><br>


## Base model

<img src="https://github.com/user-attachments/assets/f681f54a-c411-4e64-b46d-b1badadb0c21" style="width:100%" />

- Training base (LoRA fine-tune): **unsloth/Phi-3-mini-4k-instruct-bnb-4bit**  
  https://huggingface.co/unsloth/Phi-3-mini-4k-instruct-bnb-4bit
- Merge/export base (for GGUF conversion): **unsloth/Phi-3-mini-4k-instruct**  
  https://huggingface.co/unsloth/Phi-3-mini-4k-instruct
<br>

## Model format
This repo uses a **GGUF** export for local inference (e.g. `phi3_tarot.Q4_K_M.gguf`) compatible with **llama.cpp** / **llama-cpp-python**.
<br><br>

## Installation (Python)
```bash
pip install -U llama-cpp-python flask
```
<br>

## Data Source
Tarot dataset used for training : https://huggingface.co/datasets/Dendory/tarot/tree/main
<br>



