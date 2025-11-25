# AI-ML-Assignment-4-Generative-LLM
Generative AI with Pre-trained LLMs

**Victoria Salomon**
**Model Used:** gpt2 (Hugging Face)  
**Task:** Text Generation

---

## Project Overview

This project demonstrates the use of a pre-trained Large Language Model (GPT-2) from Hugging Face for **text generation**. The goal was to experiment with key generation parameters to observe their effects on the output's coherence, creativity, and style.

---

## Environment Setup

- **Python Environment:** `hf` (conda)  
- **Libraries Used:** `transformers`, `torch`  
- **Jupyter Notebook:** All code is organized in `Generative_LLM_Assignment.ipynb`

---

## Core Implementation

1. **Model Loading:**  
   Loaded GPT-2 and its tokenizer from Hugging Face.

   ```python
   from transformers import AutoTokenizer, AutoModelForCausalLM

   tokenizer = AutoTokenizer.from_pretrained("gpt2")
   model = AutoModelForCausalLM.from_pretrained("gpt2")
