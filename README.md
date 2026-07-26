<div align="center">

# Yash Chavan

### AI Engineering · LLM Evaluation · Model Serving

Final-year IIT Madras BS Data Science student building small-language-model systems from data design and fine-tuning through evaluation, portability, APIs, containers, and release evidence.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Yash_Chavan-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yash-chavan-9500a3228/)
[![Hugging Face](https://img.shields.io/badge/Hugging_Face-cyash1204-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/cyash1204)
[![Portfolio](https://img.shields.io/badge/Portfolio-SETU_×_VAHAAN-0E7C7B?style=flat-square)](https://setu-vaahan.witty-loon-6439.chatgpt.site/)
[![Email](https://img.shields.io/badge/Email-yashchavan1214%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:yashchavan1214@gmail.com)

</div>

## Profile

I focus on applied LLM engineering: defining strict NLP contracts, building and auditing data, adapting small models under hardware constraints, evaluating failure modes, and turning selected artifacts into reproducible services.

My current work is one connected engineering lifecycle:

**SETU** defines, trains, and evaluates a Hinglish support-understanding model.  
**VAHAAN** converts, qualifies, packages, and serves the selected SETU release.

I am seeking a remote AI Engineering internship involving LLM/NLP evaluation, model testing, troubleshooting, serving, and technical documentation.

## Selected projects

### SETU — Hinglish Support Understanding

> Structured NLP with Qwen3.5-2B, MLX QLoRA, strict evaluation, and reproducible synthetic data.

[Repository](https://github.com/cyash24f3/setu) ·
[Public showcase](https://setu-vaahan.witty-loon-6439.chatgpt.site/) ·
[Model](https://huggingface.co/cyash1204/setu-qwen35-2b-lora) ·
[Dataset](https://huggingface.co/datasets/cyash1204/setu-hinglish-support-6000)

- Designed a deterministic **6,000-record** Hinglish/English dataset covering **50 support scenarios** and a strict ten-field output contract.
- Enforced entity grounding, duplicate checks, taxonomy invariants, and group-aware **4,800 / 600 / 600** train-validation-test splits.
- Fine-tuned a 4-bit **Qwen3.5-2B** with MLX QLoRA on Apple silicon using rank 8 adapters across the last 12 layers.
- Selected checkpoint 700 using validation loss after an 800-step reference run.
- Evaluated all 600 held-out synthetic rows without post-hoc output repair.

| Held-out result | Value |
|:---|---:|
| Strict schema validity | **96.33%** |
| Intent accuracy | **94.33%** |
| Issue-type accuracy | **95.50%** |
| Mean correct fields | **8.99 / 10** |
| All-ten-field exact match | **46.67%** |
| Primary weakness | Language mix: **68.5%** |

The evaluation suite includes deterministic-rule and untuned-model baselines, strict parsing, per-field accuracy and macro F1, bootstrap intervals, behavioral slices, resumable prediction artifacts, and row-level error reports.

### VAHAAN — Portable Model Release & Serving

> MLX-to-GGUF portability, llama.cpp inference, FastAPI service engineering, Docker, and observability.

[Repository](https://github.com/cyash24f3/vaahan) ·
[Public evidence site](https://setu-vaahan.witty-loon-6439.chatgpt.site/) ·
[GGUF LoRA](https://huggingface.co/cyash1204/setu-qwen35-2b-lora)

- Converted the selected MLX adapter through PEFT layout into a llama.cpp-compatible F16 LoRA artifact.
- Diagnosed and rejected a faulty direct fused conversion after it produced invalid generations.
- Compared Q4_K_M and Q8_0 bases on a fixed, scenario-balanced 50-row equivalence canary.
- Selected Q8_0 for stronger structured fidelity despite its higher local latency.

| Portability canary | Q4_K_M | Q8_0 selected |
|:---|---:|---:|
| Strict schema validity | 90% | **92%** |
| Exact agreement with MLX | 56% | **62%** |
| Mean matching fields | 8.66 / 10 | **8.88 / 10** |

The service includes:

- Typed FastAPI and Pydantic request/response contracts
- Supervised llama.cpp process lifecycle and readiness
- Immutable release manifests and SHA-256 artifact verification
- Strict model-output validation and typed failures
- Bounded concurrency, rate limiting, and timeouts
- Privacy-safe structured logging and Prometheus metrics
- Liveness, readiness, and release-version endpoints
- Non-root Docker packaging, CI, linting, type checking, and API/service tests

**Deployment boundary:** the public URL is an evidence showcase. The verified Q8 llama.cpp model service performs real inference locally; I do not present the static site as publicly hosted live model compute.

## Engineering stack

| Area | Tools and concepts |
|:---|:---|
| Languages | Python, SQL, Java, C++ |
| LLM / NLP | Transformers, LoRA, QLoRA, structured generation, prompt contracts |
| Frameworks | PyTorch, MLX-LM, Hugging Face, scikit-learn, FastAPI, Pydantic |
| Model runtimes | MLX, llama.cpp, GGUF |
| Evaluation | Schema validity, exact/field metrics, macro F1, bootstrap intervals, slice and error analysis |
| Engineering | REST, OpenAPI, Docker, pytest, mypy, GitHub Actions, Linux |
| Experimentation | Weights & Biases, Jupyter, reproducible virtual environments |

## How I approach an AI system

```text
Task contract
  → data generation and validation
  → leakage-aware split and baselines
  → parameter-efficient fine-tuning
  → strict held-out evaluation and error analysis
  → cross-runtime conversion and equivalence canary
  → release manifest and verified artifacts
  → bounded API serving, observability, and containerization
```

## Education

**Indian Institute of Technology Madras**  
BS in Data Science & Applications · CGPA 8.94 · 2024–October 2027  
Completed the Diplomas in Programming and Data Science.

**BITS Pilani**  
BE Chemical Engineering · Academic break to pursue AI/ML · 2023–present.

---

<div align="center">

Open to remote, six-month AI Engineering internships.

</div>
