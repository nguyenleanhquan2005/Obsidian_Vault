- [[Artificial Intelligence]] (AI)
<aside> 🧠

**AI engineering** is the practice of turning AI capabilities into _reliable, secure, and cost-effective_ software systems that work in the real world.

</aside>

###     **Key Subfields**:
- [ ]  [[Machine Learning]] (ML)
- [ ] [[Deep Learning.canvas|Deep Learning]]
- [ ] [[Digital Speech Processing]] (NLP)
- [ ] [[Computer Vision]]
- [ ] [[AWS certificate]]
- [ ] [[Robotics]]
- [ ] [[Expert Systems]]
- [ ] [[Planning & Scheduling]]
### What AI engineering includes

- **Problem framing**
    - Define what “good” looks like.
    - Decide whether AI is actually needed.
    - Choose success metrics that match user value.
- **Data work**
    - Collect, label, and validate data.
    - Build data pipelines and contracts.
    - Manage privacy, consent, and retention.
- **Model development (when training is needed)**
    - Select architectures and baselines.
    - Train, evaluate, and compare.
    - Track experiments and reproduce results.
    - **Deep learning fundamentals (quick map)**
        - Core idea: neural networks learn representations end-to-end with backprop + gradient descent.
        - Common architectures: **MLP**, **CNN**, **RNN/LSTM/GRU**, **Transformers**.
        - Training loop: data → forward pass → loss → backprop → optimizer step.
        - Key practices: regularization (weight decay, dropout), data augmentation, early stopping.
        - Risks: overfitting, data leakage, distribution shift.
        - Useful habit: always define metrics + build an evaluation set before tuning.
- **LLM application engineering (often without training)**
    - Prompting and structured outputs.
    - Retrieval-Augmented Generation (RAG).
    - Tool use, function calling, and agents.
    - Guardrails and safety constraints.
- **Production engineering**
    - Deploy, scale, monitor, and roll back.
    - Manage latency, throughput, and cost.
    - Incident response and on-call playbooks.

### Core building blocks (typical architecture)

1. **Product layer**
    - UI and workflows that help users ask the right questions.
    - Feedback capture: thumbs up or down, edits, and corrections.
2. **Orchestration layer**
    - Routing: decide which model or approach to use.
    - Tool calling: search, databases, calculators, internal APIs.
    - State management: short-term session state and long-term memory.
3. **Knowledge layer**
    - Document ingestion: parsing, chunking, and cleaning.
    - Indexing: embeddings, hybrid search, metadata filters.
    - Governance: who can access what content.
4. **Model layer**
    - Foundation models (LLMs or vision models).
    - Fine-tuned models or adapters (when needed).
    - Evaluation harnesses and guardrails.
5. **Observability layer**
    - Logs, traces, and metrics.
    - Quality monitoring: drift, regressions, refusal rates.
    - Cost monitoring: tokens, cache hit rates, tool usage.

### Key skills for an AI engineer

- **Software engineering fundamentals**
    - APIs, testing, CI/CD, code quality, and maintainability.
- **ML and statistics basics**
    - Data leakage, bias, overfitting, calibration, and uncertainty.
- **Prompting and LLM systems**
    - Few-shot examples, output schemas, and tool integration.
- **Data engineering**
    - ETL pipelines, data validation, and dataset versioning.
- **Security and compliance**
    - PII handling, access control, secret management, and threat modeling.
- **Product thinking**
    - Human-in-the-loop design and clear failure modes.

### Practical patterns

#### 1) Retrieval-Augmented Generation (RAG)

Use RAG when answers must reflect _your documents_.

- Index internal content.
- Retrieve relevant chunks.
- Generate with citations or references.
- Add feedback loops to improve retrieval and chunking.

#### 2) Structured outputs

Ask the model to return JSON-like objects.

- Improves reliability.
- Makes downstream automation easier.
- Enables strict validation and retries.

#### 3) Tool-first reasoning

Instead of “guessing,” the system calls tools.

- Search internal docs.
- Query a database.
- Run calculations.
- Create tickets, drafts, and summaries.

#### 4) Caching and cost control

- Cache embeddings and frequent responses.
- Use smaller models for simpler steps.
- Add timeouts and fallback paths.

### Evaluation: what “good” looks like

AI engineering is mostly evaluation.

- **Offline evaluation**
    - Golden datasets, rubric scoring, and regression tests.
- **Online evaluation**
    - A/B tests, user feedback, and task success rate.
- **Model + system metrics**
    - Latency (p50, p95), cost per task, error rate.
    - Hallucination indicators and citation coverage.

### Reliability and safety

- **Common failure modes**
    - Hallucinations.
    - Prompt injection.
    - Data exposure.
    - Overconfident outputs.
- **Mitigations**
    - Retrieval with source control.
    - Input sanitization and allow-lists for tools.
    - Output validation with retries.
    - Red-teaming and adversarial tests.

### Example use cases

- Customer support copilots.
- Internal knowledge assistants.
- Document processing and extraction.
- Code review helpers and dev productivity tools.
- Personalized study assistants.

### Simple starter checklist

- [ ] Define the user task and success metric.
- [ ] Identify data sources and access rules.
- [ ] Build a baseline (often: RAG + structured output).
- [ ] Create an evaluation set and regression tests.
- [ ] Add monitoring for quality, latency, and cost.
- [ ] Plan for human review and safe fallbacks.



### Glossary (quick)


- **RAG**: Retrieval-Augmented Generation, combines search with generation.
- **Embeddings**: Vector representations used for semantic search.
- **Guardrails**: Rules and validators that constrain behavior.
- **Drift**: Changes over time that reduce performance.











# **CTCP Sách và Thiết bị Giáo dục Miền Nam** (**HNX: [SMN](https://finance.vietstock.vn/SMN-ctcp-sach-va-thiet-bi-giao-duc-mien-nam.htm)**)

# **CTCP An Tiến Industries** (**HOSE: [HII](https://finance.vietstock.vn/HII-ctcp-an-tien-industries.htm)**)

# **Tổng Công ty Dầu Việt Nam - CTCP** (**UPCoM: [OIL](https://finance.vietstock.vn/OIL-tong-cong-ty-dau-viet-nam-ctcp.htm)**)

# **CTCP Sản xuất và Công nghệ Nhựa Pha Lê** (**HOSE: [PLP](https://finance.vietstock.vn/PLP-ctcp-san-xuat-va-cong-nghe-nhua-pha-le.htm)**)

# **CTCP Masan High-Tech Materials** (**UPCoM: [MSR](https://finance.vietstock.vn/MSR-ctcp-masan-high-tech-materials.htm)**)

# **CTCP Khoáng sản Bình Định** (**HOSE: [BMC](https://finance.vietstock.vn/BMC-ctcp-khoang-san-binh-dinh.htm)**)


