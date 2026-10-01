<div align="center">

# Yash Chavan

### AI/ML Engineering

Building and evaluating machine learning systems, from model adaptation to agent workflows and evidence-grounded search.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Yash_Chavan-0A66C2?style=flat-square)](https://www.linkedin.com/in/yash-chavan-9500a3228/)
[![Hugging Face](https://img.shields.io/badge/Hugging_Face-cyash1204-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/cyash1204)
[![Email](https://img.shields.io/badge/Email-Let%27s_connect-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:yashchavan1214@gmail.com)

</div>

---

## About me

I'm pursuing a **BS in Data Science & Applications at IIT Madras**, with a focus on **AI/ML engineering. I take projects from data and baselines to model experiments, backend workflows, and usable apps, with attention to evaluation and explicit failure handling.

My current work spans **small-model adaptation with AdaptLM**, **stateful agent workflows with ResolveFlow**, and **retrieval-augmented generation with DocuLens**. Each project includes reproducible experiments and evidence that makes engineering decisions easy to inspect.

## Selected projects

### AdaptLM · Small-model adaptation for support triage

An experimental lab for adapting a small language model to structured support triage, with typed issues, extracted entities, and source-linked summary claims.

- Fine-tuned **Qwen2.5-1.5B-Instruct** with **PEFT/TRL LoRA** on Apple silicon over 880 training examples.
- Evaluated a TF-IDF classifier and zero-shot, few-shot, and adapted generation using frozen splits, strict JSON contracts, and exact source-span checks, with documented schema and source-offset failures.
- Deployed real base/adapter inference on **Hugging Face ZeroGPU**, backed by bounded FastAPI serving and inspectable experiment reports.

**Stack:** Python · PyTorch · Transformers · PEFT · TRL · scikit-learn · FastAPI

[Source code](https://github.com/cyash24f3/AdaptLM) · [Live demo](https://huggingface.co/spaces/cyash1204/AdaptLM) · [Evaluation & findings](https://github.com/cyash24f3/AdaptLM/blob/main/docs/results.md)

### ResolveFlow · Stateful support operations agent

A fictional support sandbox that investigates requests, collects missing details, and routes refunds, replacements, and cancellations through supervisor approval.

- Built **LangGraph workflows** with persistent PostgreSQL checkpoints, typed tools, and a durable job worker.
- Enforced deterministic policy checks, scoped role access, and approval of the **exact proposed action** before changing the sandbox ledger.
- Verified recovery across worker restarts and a cloud redeploy, with rejection checks and protection against duplicate effects. The hosted demo uses fixture decisions; live model tool calling is an optional mode.

**Stack:** Python · LangGraph · FastAPI · Pydantic · PostgreSQL · SQLAlchemy · Alembic

[Source code](https://github.com/cyash24f3/resolveflow) · [Live demo](https://resolveflow-wojr.onrender.com/) · [Architecture & transactions](https://github.com/cyash24f3/resolveflow/blob/main/docs/ARCHITECTURE.md)

### DocuLens · Evidence-grounded knowledge copilot

A retrieval-augmented knowledge assistant for support documentation, with PDF, Markdown, and text ingestion, search, and answers linked to exact source versions.

- Compared **BM25, MiniLM dense retrieval, RRF hybrid search, and cross-encoder reranking** with reproducible retrieval experiments and documented evaluation limits.
- Built versioned ingestion with background jobs and atomic activation, so a failed document replacement keeps the previous version searchable.
- Shipped a **Render demo with quantized ONNX retrieval and Groq generation**, plus local Ollama generation and persistent PostgreSQL/pgvector deployment through Docker Compose.

**Stack:** Python · FastAPI · Sentence Transformers · ONNX Runtime · PostgreSQL/pgvector · Docker

[Source code](https://github.com/cyash24f3/doculens-v2) · [Live demo](https://yash-doculens-v2.onrender.com/) · [Retrieval results](https://github.com/cyash24f3/doculens-v2/blob/main/docs/evidence/retrieval-test/report.md)

## Engineering stack

| Area | Tools I use |
|:---|:---|
| Languages | Python, SQL, JavaScript, HTML/CSS |
| Model adaptation | PyTorch, Hugging Face Transformers, PEFT/LoRA, TRL, scikit-learn |
| Retrieval & generation | Sentence Transformers, BM25, RRF, cross-encoders, ONNX Runtime, Ollama, Groq |
| Agents & APIs | LangGraph, FastAPI, Pydantic, REST/OpenAPI |
| Data & persistence | PostgreSQL, pgvector, SQLite, SQLAlchemy, Alembic |
| Deployment | Docker, Docker Compose, Render, Neon, Hugging Face Spaces |
| Quality & tooling | pytest, Playwright, Ruff, mypy, GitHub Actions, Git, uv |

## How I build

**Define the contract → build a baseline → evaluate failures → ship a bounded service.**

I keep model quality, workflow correctness, and deployment verification as separate measurements. My repositories include setup instructions, architecture notes, experiment records, and observed limitations so the work can be reproduced and reviewed.

## Education

**Indian Institute of Technology Madras**<br>
BS in Data Science & Applications · Pursuing<br>
**CGPA 8.95** · 2024–October 2027

**BITS Pilani**<br>
BE Chemical Engineering · 2023–2025<br>
Dropped out.

---

<div align="center">

**[LinkedIn](https://www.linkedin.com/in/yash-chavan-9500a3228/)** · **[Hugging Face](https://huggingface.co/cyash1204)** · **[Email](mailto:yashchavan1214@gmail.com)**

</div>
