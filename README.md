<p align="center">
  <img alt="In A Few Words" src="https://miro.medium.com/max/300/1*r_ZHEI90PzPnyaHZXI_org.png" width="120">
  <h1 align="center">In A Few Words</h1>
  <p align="center"><b>Multilingual text summarization with Deep Learning.</b></p>
  <p align="center">A lightweight Python wrapper around mT5 for summarizing text in multiple languages.</p>
</p>

<p align="center">
  <a href="https://github.com/Amloii/InAFewWords"><img alt="Stack" src="https://img.shields.io/badge/stack-Python%20%7C%20HuggingFace%20%7C%20mT5-25601B?style=flat-square&labelColor=ffffff&color=25601B"></a>
  <a href="https://github.com/Amloii/InAFewWords"><img alt="Created" src="https://img.shields.io/badge/created-April%202022-000000?style=flat-square&labelColor=ffffff&color=000000"></a>
  <a href="https://github.com/Amloii/InAFewWords"><img alt="Status" src="https://img.shields.io/badge/status-discontinued-ef4444?style=flat-square&labelColor=ffffff&color=ef4444"></a>
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/badge/license-MIT-blue?style=flat-square&labelColor=ffffff&color=blue"></a>
</p>

<p align="center">
  <a href="#-about">About</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-project-structure">Structure</a>
</p>

<br>

> **Created April 2022 as a pet project for multilingual NLP experimentation.**  
> This project has been **discontinued**. Modern LLMs (GPT, Gemini, Claude, etc.) deliver dramatically better summarization quality, handle far longer contexts, and support more languages out of the box. The code remains available as a reference for the mT5 approach.

---

## 🧐 About

Text summarization is essential for processing long documents, articles, and books. In 2022, most open-source summarization models were English-only, limiting their usefulness in multilingual contexts.

In A Few Words wraps [mT5_multilingual_XLSum](https://huggingface.co/csebuetnlp/mT5_multilingual_XLSum) — a multilingual variant of T5 trained on the XL-Sum dataset — into a simple, reusable Python class and function. It supports summarization across multiple languages without requiring language-specific fine-tuning.

The model processes up to 512 tokens of input text and generates concise summaries using beam search, making it suitable for short-to-medium length content.

---

## 🚀 Quick Start

```bash
git clone https://github.com/Amloii/InAFewWords.git
cd InAFewWords
pip install -r requirements.txt
```

---

## 🎈 Usage

### As a Python function

```python
from function.summarize_function import summarize, sum_model

text = "Long article or document text in Spanish, English, French, or other supported languages..."
summary = summarize(sum_model, text)
print(summary)
```

### Using the model class directly

```python
from src.SummarizationModel import SummarizationModel

model = SummarizationModel()
summary = model.summarize("Your text here in any supported language.")
```

The underlying model is `csebuetnlp/mT5_multilingual_XLSum`, a multilingual T5 fine-tuned on the XL-Sum dataset. Input is truncated to 512 tokens; output is generated with beam search (4 beams, max 84 tokens, no repeat n-grams).

---

## 📁 Project Structure

```
├── src/
│   └── SummarizationModel.py   # mT5 model wrapper class
├── function/
│   └── summarize_function.py   # Ready-to-use function import
├── requirements.txt
└── README.md
```

---

## 📝 License

MIT — see [LICENSE](LICENSE).

---

## 👤 Author

**Daniel Gómez Domínguez** — AI Systems Architect & Director of AI.

Built as a pet project exploring multilingual NLP and HuggingFace transformer pipelines, prior to the widespread availability of LLM-based summarization.

[GitHub](https://github.com/Amloii) · [LinkedIn](https://linkedin.com/in/danigdominguez) · [Portfolio](https://amloii.github.io)

<br>

---

<p align="center">
  <sub>In A Few Words · 2022 — Discontinued, but a good snapshot of pre-LLM multilingual NLP.</sub>
</p>
