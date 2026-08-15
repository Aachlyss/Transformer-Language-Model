# Transformer-Language-Model

This is a personal project where I build a Small Transformer Language Model, completely from scratch using PyTorch.

**This is not a competitor to ChatGPT, Claude or any moderm LLM!**
**It is simply an educational project created because I really wanted to get a better understanding of the math, data and architecture that transformers work with.**

****

## Why build this?

If you are looking to kind of demystify the concepts behind LLMs and not only use them to build applications via the API of providers, I would recommend to and would be greateful if you have a look at this `Python Notebook`, which I have in this repository. Here are the key concepts, which I aim to learn about whilst doing this project:

* Process and tokenize text streams using sub-word tokenizers (`tiktoken`).
* Build PyTorch DataLoaders to efficiently feed data into a GPU.
* Write custom embeddings (Token and Positional).
* Construct Self-Attention mechanisms and Transformer blocks from scratch.
* Train, optimize, and fine-tune a model on consumer hardware.

****

## Tech Stack & Hardware

* **Framework:** PyTorch (with CUDA)
* **Hardware:** NVIDIA RTX 4060 Ti (16GB VRAM)
* **Tokenizer:** OpenAI's `gpt2` tokenizer via `tiktoken`
* **Data Handling:** Hugging Face `datasets`

****

## Datasets

I read about the different stages and concepts when training a transformer in the book "[AI Engineering](https://www.oreilly.com/library/view/ai-engineering/9781098166298/)" by the writer and computer scientist [Chip Huyen](https://huyenchip.com/). There it is mentioned the approach of first `pre-training` your model on a wide range of information, to achieve general understanding and after that `fine-tuning` the model based on the specific task you want your transformer to do -- in my case that would be conversations. Here are the two datasets I will be using:

1. **Pre-training:** Using a slice of the [TinyStories](https://huggingface.co/datasets/roneneldan/TinyStories) dataset to teach the model basic grammar, structure, and language flow (5 000).
2. **Fine-tuning (Planned):** Transitioning to a dialogue/instruction dataset to experiment with conversational formatting (`<|user|>` and `<|assistant|>` markers).

****
