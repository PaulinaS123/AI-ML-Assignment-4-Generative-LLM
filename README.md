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

   ## Parameter Test Cases Summary

| Parameter | Value | Output Snippet | Observation |
|-----------|-------|----------------|------------|
| Temperature | 0.2 | "Once upon a time in a magical forest, the dragon was a living creature, and the dragon was a living creature…" | Very coherent, predictable, repetitive. |
| Temperature | 0.7 | "Once upon a time in a magical forest, the man was given the opportunity to save the forest…" | Creative and moderately coherent. Balanced randomness. |
| Temperature | 1.0 | "Once upon a time in a magical forest, the black stone that once was a part of the Great Stone Age…" | Highly creative, imaginative, slightly less coherent. |
| Max Tokens | 50 | "Once upon a time in a magical forest, a fox ran under the shining moonlight." | Short and concise. Story ends quickly. |
| Max Tokens | 150 | "Once upon a time in a magical forest, a fox ran under the shining moonlight, exploring hidden caves…" | Moderate length, more story development. |
| Max Tokens | 300 | "Once upon a time in a magical forest, a fox ran under the shining moonlight, exploring hidden caves, meeting mysterious creatures…" | Long and detailed. Full story with richer narrative. |
| Top-p | 0.5 | "Once upon a time in a magical forest, the owl watched carefully as the rabbit hopped along the path." | Low diversity, predictable. |
| Top-p | 0.9 | "Once upon a time in a magical forest, the owl watched carefully as the rabbit discovered sparkling mushrooms…" | Balanced diversity, creative and coherent. |
| Top-p | 1.0 | "Once upon a time in a magical forest, the owl watched carefully as the rabbit danced through glowing mushrooms…" | Highly diverse and creative, slightly less structured. |

