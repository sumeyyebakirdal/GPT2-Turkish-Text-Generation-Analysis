# The Effect of Sampling Parameters on Human and Automatic Evaluation Metrics in Turkish Text Generation

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97-Hugging%20Face-orange)
![NLP](https://img.shields.io/badge/Focus-NLP-green)

This repository contains the implementation and experimental results of a study investigating the impact of different decoding strategies on **Turkish text generation** using the **GPT-2** architecture. The research focuses on the trade-off between text fluency, coherence, and creativity.

## 📖 Project Abstract
In Natural Language Processing, the quality of generated text is highly dependent on the sampling strategy used during the inference phase. This study evaluates the Turkish language performance of GPT-2 across three key parameters:
1. **Temperature ($T$):** Controlling the sharpness of the probability distribution.
2. **Top-k Sampling:** Limiting the vocabulary to the top $k$ most likely tokens.
3. **Top-p (Nucleus) Sampling:** Dynamically selecting a subset of tokens whose cumulative probability exceeds threshold $p$.

The study concludes that while higher randomness increases creativity, it often degrades grammatical coherence in Turkish due to its complex morphological structure.

---

## 🛠️ Experimental Methodology
The pipeline involves generating text from a set of Turkish prompts and evaluating them through two distinct lenses:

### 1. Automatic Evaluation
* **Perplexity (PPL):** Used as the primary metric to measure the model's uncertainty.
* **Observation:** Lower perplexity was observed in "Greedy Search" and low-temperature settings, but at the cost of repetitive and "boring" text.

### 2. Human Evaluation
A panel of human evaluators scored the generated samples based on:
* **Fluency:** Grammatical correctness and natural flow in Turkish.
* **Coherence:** Logical consistency across sentences.
* **Creativity:** The diversity and uniqueness of the generated content.



---

## 📊 Key Findings
As detailed in the research paper:
* **Optimal Top-p:** Values between **0.90 and 0.95** provided the best balance for Turkish generative tasks.
* **Temperature Impact:** $T < 1.0$ produced more focused and coherent text, while $T > 1.0$ led to significant semantic degradation.
* **Top-k Influence:** A $k$ value of **40 to 50** was found to be effective in filtering out low-probability "noise" tokens.

---

## 📂 Repository Structure
* `GPT2_Sampling_Metrics_Turkish.ipynb`: Full implementation of the generation and evaluation pipeline.
* `nlp.pdf`: The complete technical research paper (in Turkish).
  
---
