# Fine-Tuning LLMs

**When prompting is not enough — fine-tune models for your specific domain, style, and task requirements.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## When to Fine-Tune vs Prompt Engineer

| Situation | Solution |
|---|---|
| General tasks | Prompt engineering |
| Specific output format always needed | Fine-tuning |
| Domain-specific knowledge | RAG + prompting |
| Consistent tone/style | Fine-tuning |
| Faster inference needed | Fine-tuning (smaller model) |
| Proprietary data (cannot send to API) | Fine-tuning local model |

**Rule:** Try prompting + RAG first. Fine-tune only when you need consistency, speed, or data privacy.

## Fine-Tuning Methods

### LoRA (Low-Rank Adaptation) — Most Popular
Trains small adapter layers instead of full model weights.
Reduces trainable parameters by 99%+ with minimal quality loss.

### QLoRA — Fine-Tune on a Single GPU
4-bit quantization + LoRA = fine-tune 70B models on consumer hardware.

### DPO (Direct Preference Optimization)
Align model to human preferences without RLHF complexity.

## Dataset Format

Instruction tuning format:
- instruction: What to do
- input: The data/context
- output: The desired response

Quality > Quantity. 1,000 great examples beat 100,000 mediocre ones.

## Tools

- **Hugging Face Transformers + PEFT** — Full control
- **Unsloth** — 2x faster, less memory
- **Axolotl** — Config-driven, production-ready
- **OpenAI Fine-tuning API** — Easiest for GPT-4o mini

---

Part of the [Real-World AI Skills Ecosystem](https://github.com/saitejabandaru-in)
