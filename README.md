# CareerFit AI — Resume Intelligence Engine

An end-to-end **AI system** that analyzes a resume against a job description using
semantic search (RAG), large language models, and a fine-tuned classifier — built
to demonstrate core AI-engineering concepts from first principles.

> **Why this project exists:** to learn and showcase the full modern AI stack —
> vector embeddings, Retrieval-Augmented Generation (RAG), retrieval evaluation,
> LLM prompting, and fine-tuning — with real evaluation metrics at every step.

---

## What it does

Given a **resume** and a **job description**, CareerFit AI returns:
- An **ATS match score** (0–100)
- **Matched** and **missing** skills
- **Weak bullet points** rewritten to be stronger
- Tailored **interview questions** (technical, behavioral, resume deep-dive)
- The most **similar real job postings** found via semantic search (RAG)

---

## AI concepts demonstrated

| Module | Concept | Key technique | Evaluation |
|--------|---------|---------------|------------|
| 1 | **Vector embeddings** | `sentence-transformers`, cosine similarity | similarity sanity checks + t-SNE visualization |
| 2 | **RAG** | chunking → embedding → FAISS retrieval → prompt augmentation | — |
| 3 | **Retrieval evaluation** | building a test set of queries | recall@k, MRR |
| 4 | **LLM analysis** | prompt engineering, structured JSON output | output validity checks |
| 5 | **Fine-tuning** | LoRA / PEFT on DistilBERT (bullet-strength classifier) | accuracy, F1, confusion matrix (before vs. after) |
| 6 | **Deployment** | Streamlit demo app | — |

---

## Tech stack

**Python** · sentence-transformers · FAISS · HuggingFace Transformers · PEFT (LoRA) ·
Anthropic Claude · scikit-learn · Streamlit

---

## Project structure

```
careerfit-ai/
├── data/            # job-postings corpus, sample resumes
├── notebooks/       # one notebook per AI concept (the learning trail)
├── src/careerfit/   # reusable Python modules
├── app/             # Streamlit demo app
└── tests/           # sanity checks
```

## Status

🚧 In active development — building module by module. See `notebooks/` for progress.
