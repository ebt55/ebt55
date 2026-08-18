<h1 align="center">Hey, I'm Ebin Babu Thomas 👋</h1>

<p align="center"><b>Backend / Applied AI Engineer</b> — agent reliability · verification · evaluation · RAG · fine-tuning · inference</p>

<p align="center">
  <a href="mailto:ebinbabuthomas@gmail.com">
    <img src="https://img.shields.io/badge/Email-ebinbabuthomas%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  <a href="https://peerlist.io/ebinbt">
    <img src="https://img.shields.io/badge/Peerlist-ebinbt-00AA45?style=for-the-badge&logo=peerlist&logoColor=white" alt="Peerlist">
  </a>
  <a href="https://www.linkedin.com/in/ebinbt">
    <img src="https://img.shields.io/badge/LinkedIn-ebinbt-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <img src="https://img.shields.io/badge/Kerala%2C%20India-Remote-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location">
</p>

3.5 years shipping applied-AI backends end-to-end for startup clients in the US, Canada, Europe, and Australia — from ambiguous requirements to deployed systems. Since mid-2026 I build **AI systems that have to prove what they claim**: evidence-gated agents, durable human-in-the-loop control over MCP tools, and preregistered behavioural experiments on open models. I publish the failed tests alongside the passing ones.

> 💼 **Open to backend / applied-AI / AI-safety engineering roles, fellowships, and contract work.**

---

## 🔬 Current work (Aug 2026)

| Project | One line | Headline number | Stack |
|---|---|---|---|
| [**digital-grimace-scale**](https://github.com/ebt55/digital-grimace-scale) | Preregistered study: do LMs show involuntary markers of adverse treatment? Primary test failed & published; a second channel found. | DPO removed **65.8%** of distress language, margin effect **unchanged** | vLLM · Modal · QLoRA-DPO · logprobs |
| [**incidentgate**](https://github.com/ebt55/incidentgate) 🚧 | Lab measuring how policy gates + monitor + human approval change an incident agent under crashes & hostile input | **434/434** kill-point recoveries, 0 duplicate mutations | LangGraph · FastMCP · Postgres · OTel/Langfuse |
| [**proofpack**](https://github.com/ebt55/proofpack) | Pre-approval review agent whose evidence can't be fabricated — every "Found" cites a hashed screenshot | **$0.02–0.19** / review, ~3 min vs 20–40 min manual | Gemini · Claude Agent SDK · Playwright |
| [**exactdoc**](https://github.com/ebt55/exactdoc) | PDF → *editable* DOCX, verified by rendering back and diffing word positions | **16/16** corpus, 0.9588 text retention, 663 tests | PDFium · OOXML · LibreOffice |
| [**whose-voice**](https://github.com/ebt55/whose-voice) | Blind attribution of hidden principals in poisoned training corpora — and where it breaks | **12–44%** top-1 of 47 (chance 2.1%) | sentence-transformers · bootstrap/permutation |

<details>
<summary><b>Details ▾</b></summary>

### 🧪 Digital Grimace Scale — *do LMs show involuntary markers of adverse treatment?*

<p>
  <a href="https://github.com/ebt55/digital-grimace-scale">
    <img src="https://img.shields.io/badge/GitHub-digital--grimace--scale-181717?style=for-the-badge&logo=github&logoColor=white" alt="digital-grimace-scale on GitHub">
  </a>
  <img src="https://img.shields.io/badge/Apart%20Research-Digital%20Minds%20Sprint%202026-6C3FC5?style=for-the-badge" alt="Apart Research Digital Minds sprint">
</p>

- **Preregistered 2×2×2 design** — difficulty × feedback validity × tone; strings, gates and metrics frozen before analysis; 40-item bank + 86 held-out ARC items; gemma-2-9b-it (primary), Qwen-3B, Llama-3.1-8B.
- **The primary test failed — and is published as a FAIL.** A re-preregistered iteration found an answer-margin channel: three rounds of false feedback −2.90 nats [−3.97, −1.84]; hostile tone −7.87 to −16.13 nats; family permutation p = 0.005; larger on fresh ARC items.
- **Channel dissociation** — a QLoRA-DPO adapter removed 65.8% of distress *language* but left the internal margin effect unchanged or larger. **The report can be trained away while the behaviour stays.**
- **Reproducible** — vLLM on Modal, ~650 tests, SHA-256-frozen scripts, byte-identical figure regeneration; limitations listed as first-class results.

### 🚧 IncidentGate — *governed incident-remediation agent lab* (in development)

<p>
  <a href="https://github.com/ebt55/incidentgate">
    <img src="https://img.shields.io/badge/GitHub-incidentgate-181717?style=for-the-badge&logo=github&logoColor=white" alt="incidentgate on GitHub">
  </a>
  <img src="https://img.shields.io/badge/status-in%20development-F9A825?style=for-the-badge" alt="in development">
</p>

- **A measurement lab, not a product** — how do deterministic policy gates, an advisory action monitor and human approval change an incident agent's behaviour under crashes, misleading evidence and hostile input?
- **Enforced mutation chain** — evidence → policy gate → monitor → durable pre-approval audit → **single-use approval token** (bound to action hash, actor, expiry, incident) → atomic idempotent op → post-commit verification. Forbidden actions are unreachable via closed `Literal` types.
- **Durability proof** — worker killed with `os._exit(137)` at every LangGraph node boundary: **594 kill points / 27 scenarios, 434/434 cells recovered identically**, zero lost incidents, zero duplicate mutations.
- **Honest status** — three-condition harness replays 30/30; model not yet in the decision path; MCP servers in-process only. LangGraph · FastMCP · PostgreSQL · OpenTelemetry → Langfuse.

### 🧾 ProofPack — *the AI pre-approval reviewer that brings the receipts*

<p>
  <a href="https://github.com/ebt55/proofpack">
    <img src="https://img.shields.io/badge/GitHub-proofpack-181717?style=for-the-badge&logo=github&logoColor=white" alt="proofpack on GitHub">
  </a>
  <img src="https://img.shields.io/badge/main-Gemini%203.7%20Flash-4285F4?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini on main">
  <img src="https://img.shields.io/badge/claude--sdk-Claude%20Agent%20SDK-D97757?style=for-the-badge&logo=claude&logoColor=white" alt="Claude Agent SDK branch">
</p>

Successor to my *Pre-Approvals Reviewer* — built around a real workflow at NY disability-services nonprofits: before a purchase from a self-directed, Medicaid-audited budget is approved, a reviewer must verify the provider's public website and file date-stamped evidence.

- **Five-stage pipeline** — PDF form → structured extraction → category-routed **YAML checklists** a non-engineer can edit → **deterministic** fee-cap & eligibility checks → **browser research agent** (Playwright) → HTML/JSON report + evidence folder with SHA-256 manifest.
- **Fabrication is structurally impossible, not just discouraged** — a "Found" can't be recorded without a real on-disk capture; quotes are rejected unless they appear verbatim on a visited page; timestamps, URLs and hashes are written by code the model never touches.
- **Honest uncertainty as a feature** — unverifiable items stay *"Internal — not answered"*; "Not Found" is a correct answer, not a failure. Humans keep every approve/deny decision.
- **Measured** — $0.02–$0.19 per review (≈$0.10 avg), ~3 min vs 20–40 min manual; 45 offline tests + rerunnable integrity audit; negatives ground-truthed by hand.

### 📝 ExactDoc — *measurement-validated PDF → DOCX*

<p>
  <a href="https://github.com/ebt55/exactdoc">
    <img src="https://img.shields.io/badge/GitHub-exactdoc-181717?style=for-the-badge&logo=github&logoColor=white" alt="exactdoc on GitHub">
  </a>
</p>

- Emits genuinely **editable** Word structure — real paragraphs, headings, lists, tables, multi-column sections — not text boxes.
- **Render-back verification** — every DOCX is rendered back to PDF and word positions diffed against the source. Frozen 16-doc corpus: **16/16 convert, 0.9588 mean live-text retention, 1.045 pt median drift**; 663 tests; SHA-256-pinned corpus.

### 🕵️ whose-voice — *blind principal attribution from poisoned corpora*

<p>
  <a href="https://github.com/ebt55/whose-voice">
    <img src="https://img.shields.io/badge/GitHub-whose--voice-181717?style=for-the-badge&logo=github&logoColor=white" alt="whose-voice on GitHub">
  </a>
  <img src="https://img.shields.io/badge/Apart%20%C3%97%20Formation-Secret%20Loyalties%20Hackathon-6C3FC5?style=for-the-badge" alt="Secret Loyalties hackathon">
</p>

- Recovers hidden "secret loyalty" principals at **12–44% top-1 of 47** (chance 2.1%, permutation p ≤ 0.025) with off-the-shelf embedders and no clean reference — and maps where it breaks: realistic poison densities, attribution ≠ detection, trigger-conditional loyalties.
- 21 validation tests with planted-signal / no-signal controls that inverted three early claims; ~48-hour solo build.

</details>

---

## 🧰 Selected earlier work (2022–2025)

Built at **Zackriya Solutions** for startup clients — most code is private client work; public artifacts are linked. Open-source contributions from this period live under my work account **[@ebinzack15](https://github.com/ebinzack15)**.

### 🤖 Applied AI & LLM systems

- 🏠 **Natural-language real-estate search** — plain-English → SQL over Cloud SQL via GPT-3.5, with a "Did you mean?" suggester; FastAPI on GCP Cloud Run, load-tested with Locust for peak traffic.
- 📄 **DocuAI — semantic document search** — chunks & indexes 1000+ documents in Qdrant and returns the most relevant parent documents by semantic similarity; Next.js frontend. → [Live demo](https://docuai.zackriya.com/dashboard)
- 🗣️ **Speech-assessment backend (EdTech)** — speech scores from 1-minute candidate videos via Whisper ASR + Microsoft Pronunciation API; deployed on AWS Fargate; scores aligned with ground-truth data.
- 💸 **FinBot — fine-tuned financial assistant** — Mistral-7B fine-tuned with QLoRA (HF SFT trainer) + a financial-news pipeline (Alpaca → Bytewax → Qdrant); served on GKE with vLLM on an L4 GPU.
  <br>→ Kaggle notebooks: [Fine-tuning with QLoRA](https://www.kaggle.com/code/ebinbt007/fine-tuning-mistral-7b-with-qlora-for-financial) · [Merging LoRA adapters](https://www.kaggle.com/code/ebinbt007/merging-lora-adapters-with-base-model) · [Inference](https://www.kaggle.com/code/ebinbt007/inferencing-custom-mistral-7b-llm-on-kaggle)
- 🎧 **Customer-support RAG backend** — document-ingestion and retrieval API over a vector database, behind a customer-service plugin.

### ⚙️ Data engineering & backend tooling

- 📡 **IoT data handler** — live MQTT sensor streams → MongoDB for a bioreactor startup (client later secured funding), plus a stream mocker for local development.
- 📑 **BPMN → PDF report engine** — parses BPMN files and generates complex PDF reports with nested tables and embedded diagram images.
- 🏥 **Healthcare data processing** — CSV/JSON cleaning pipelines, PDF compliance reports, and byte-pattern error-detection filters for medical-device data.

### 🌱 Open source

- **[Meetily](https://github.com/Zackriya-Solutions/meetily)** (privacy-first meeting notes — GitHub Trending) — backend cleanup, OpenAI provider support, and a CLI testing script. → [Merged PR #75](https://github.com/Zackriya-Solutions/meetily/pull/75)
- **bpmn-io/refactorings** — proposed and built a cosine-similarity connector-template recommender (SentenceTransformer embeddings) as a lightweight, customizable alternative to LLM function calls. → [Issue #33](https://github.com/bpmn-io/refactorings/issues/33) · [Implementation fork](https://github.com/Zackriya-Solutions/refactorings)

---

## 🛠️ Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,fastapi,docker,kubernetes,postgres,mongodb,aws,gcp,terraform,git,linux,nextjs&perline=12" alt="Python, FastAPI, Docker, Kubernetes, PostgreSQL, MongoDB, AWS, GCP, Terraform, Git, Linux, Next.js">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude%20Agent%20SDK-D97757?style=flat-square&logo=claude&logoColor=white" alt="Claude Agent SDK">
  <img src="https://img.shields.io/badge/Gemini%20API-4285F4?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini API">
  <img src="https://img.shields.io/badge/OpenAI%20API-412991?style=flat-square" alt="OpenAI API">
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langgraph&logoColor=white" alt="LangGraph">
  <img src="https://img.shields.io/badge/MCP%20%2F%20FastMCP-000000?style=flat-square" alt="MCP / FastMCP">
  <img src="https://img.shields.io/badge/PydanticAI-E92063?style=flat-square&logo=pydantic&logoColor=white" alt="PydanticAI">
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face">
  <img src="https://img.shields.io/badge/vLLM-4B8BBE?style=flat-square" alt="vLLM">
  <img src="https://img.shields.io/badge/Modal-7FEE64?style=flat-square&logo=modal&logoColor=black" alt="Modal">
  <img src="https://img.shields.io/badge/LoRA%20%2F%20QLoRA%20%2F%20DPO-9C27B0?style=flat-square" alt="LoRA / QLoRA / DPO">
  <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square" alt="Qdrant">
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square" alt="Playwright">
  <img src="https://img.shields.io/badge/OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white" alt="OpenTelemetry">
  <img src="https://img.shields.io/badge/Langfuse-000000?style=flat-square" alt="Langfuse">
  <img src="https://img.shields.io/badge/RAG-FF6F00?style=flat-square" alt="RAG">
</p>

---

## 📫 Reach me

- 📧 [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)
- 💼 LinkedIn — [linkedin.com/in/ebinbt](https://www.linkedin.com/in/ebinbt)
- 🟢 Peerlist — [peerlist.io/ebinbt](https://peerlist.io/ebinbt)

<!-- TODO(Ebin): uncomment and fill these in as the profiles go live —
- 🧑‍💻 Upwork — YOUR-UPWORK-PROFILE-URL
- ✨ Contra — YOUR-CONTRA-PROFILE-URL
- 🌐 Portfolio — YOUR-SITE-URL
-->
