# Mini Transformer Language Model (From Scratch)

## Overview

This project is a fully custom-built transformer-based language model developed from first principles. The goal was not to achieve state-of-the-art performance, but to deeply understand how modern language models function internally by implementing every major component manually.

Unlike typical projects that rely on pretrained architectures or high-level libraries, this model was built with minimal abstraction to expose the underlying mechanics of training and inference.

---

## Key Features

- ~10 Million Parameter Transformer Model  
  The architecture is intentionally kept compact to enable local training while still demonstrating meaningful learning behavior.

- Custom Tokenizer  
  A tokenizer designed and implemented from scratch to control the text preprocessing pipeline and vocabulary handling.

- Self-Attention Mechanism  
  Multi-head self-attention implemented manually, including query, key, value projections and attention score computation.

- Causal Masking  
  Proper masking ensures the model learns autoregressive behavior, predicting the next token without access to future tokens.

- Full Training Loop  
  The training pipeline, including batching, loss computation, backpropagation, and optimization, is implemented without relying on high-level trainer APIs.

- From-Scratch Training  
  No pretrained weights or external checkpoints were used. The model learns entirely from the provided dataset.

---

## Training Insights

The training process reveals distinct learning phases:

1. Initial Phase  
   The model produces completely random and incoherent text, reflecting uninitialized probability distributions.

2. Structural Learning Phase  
   Outputs become grammatically consistent but lack semantic meaning, indicating the model is capturing syntax patterns.

3. Coherence Phase  
   The model generates text that appears meaningful at a glance, though deeper inspection shows limited understanding.

This progression highlights a key property of language models: they learn statistical structure before any semblance of meaning.

---

## Technical Stack

- Python
- PyTorch (low-level usage, minimal abstraction)
- Custom data preprocessing pipeline
- GPU training (local laptop GPU)

---

## Why This Project Matters

Most implementations abstract away the complexity of transformer models, making it difficult to understand their true behavior. This project focuses on:

- Understanding attention at a mathematical and implementation level  
- Observing how models learn patterns over time  
- Identifying failure modes and limitations of probabilistic text generation  

The emphasis is on learning depth rather than producing polished outputs.

---

## Limitations

- Small model size compared to modern LLMs  
- Limited dataset and compute resources  
- Outputs may lack deep semantic consistency  

These constraints are intentional to keep the system interpretable and trainable on local hardware.

---

## Future Work

- Scaling model parameters and dataset size  
- Improving tokenizer efficiency  
- Experimenting with training stability techniques  
- Adding evaluation benchmarks  

---

## Conclusion

This project is an exploration of how language models actually work beneath the surface. It prioritizes understanding over convenience and exposes the realities behind modern AI systems.

It is not the most powerful model—but it is one where every component is understood, controlled, and built from the ground up.
