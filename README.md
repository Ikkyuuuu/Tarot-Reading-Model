# Tarot-Reading-Model

A fine-tuned **Phi-3 Mini** model for generating **3-card tarot readings** from a user question and the drawn cards.  
This project focuses on producing short, structured interpretations suitable for local inference.
<br><br>

## 🔗 Download (Hugging Face)

Download the GGUF model(s) here:  **https://huggingface.co/Ikkyuuu/Tarot-Reading-Model**
<br><br>

## 🦥 Base model (Unsloth)

<img src="https://github.com/user-attachments/assets/f681f54a-c411-4e64-b46d-b1badadb0c21" style="width:100%" />

- Training base (LoRA fine-tune): **unsloth/Phi-3-mini-4k-instruct-bnb-4bit**  
  https://huggingface.co/unsloth/Phi-3-mini-4k-instruct-bnb-4bit
- Merge/export base (for GGUF conversion): **unsloth/Phi-3-mini-4k-instruct**  
  https://huggingface.co/unsloth/Phi-3-mini-4k-instruct
<br>

## 📦 Model format
This repo uses a **GGUF** export for local inference (e.g. `phi3_tarot.Q4_K_M.gguf`) compatible with **llama.cpp** / **llama-cpp-python**.
<br><br>

## 💾 Setup (Python)
```bash
pip install -U llama-cpp-python 
```
<br>

## 🚀 Quick Start (llama-cpp-python)
```bash
from llama_cpp import Llama

llm = Llama(
    model_path="phi3_tarot.Q4_K_M.gguf",
    n_ctx=4096,
)

prompt = """You are a tarot reader.
User question: Will I get a new job soon?
Cards: 1) The Fool (upright), 2) Three of Pentacles (upright), 3) The Moon (reversed)
Give a short 3-card reading with structure:
- Past
- Present
- Future
- Advice
"""

out = llm(prompt, max_tokens=250, temperature=0.7)
print(out["choices"][0]["text"].strip())
```
<br>

## 📚 Data Source
Tarot dataset used for training : https://huggingface.co/datasets/Dendory/tarot/tree/main
<br>



