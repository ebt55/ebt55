<h1 align="center">Hey, I'm Ebin Babu Thomas 👋</h1>

<p align="center"><b>Backend / Applied AI Engineer</b> — RAG pipelines · LLM agents · fine-tuning · inference</p>

<p align="center">
  <a href="mailto:ebinbabuthomas@gmail.com">
    <img src="https://img.shields.io/badge/Email-ebinbabuthomas%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  <a href="https://peerlist.io/ebinbt">
    <img src="https://img.shields.io/badge/Peerlist-ebinbt-00AA45?style=for-the-badge&logo=peerlist&logoColor=white" alt="Peerlist">
  </a>
  <img src="https://img.shields.io/badge/Kerala%2C%20India-Remote-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location">
</p>

3.5 years shipping applied-AI backends end-to-end for startup clients in the US, Canada, Europe, and Australia — from ambiguous requirements to deployed systems. I like simple, well-scoped solutions, and I'm particularly interested in **AI systems that can prove what they claim**.

> 💼 **Open to backend / applied-AI roles and freelance engagements.**

---

## 🔭 Featured — Pre-Approvals Reviewer

*An audit-grade website-verification agent (Claude + Playwright).*

Built around a real workflow at a NY disability-services nonprofit: before a purchase from a self-directed, Medicaid-audited budget is approved, a reviewer must verify the provider's public website and file date-stamped evidence — today done by hand, one site at a time.

<p>
  <a href="https://github.com/ebt55/preapproval-verification-challenge">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=ebt55&repo=preapproval-verification-challenge&theme=transparent" alt="preapproval-verification-challenge repo card">
  </a>
</p>

- **Five-stage pipeline** — PDF form → vision-based structured extraction (Claude) → category-routed **YAML checklists** a non-engineer can edit → **deterministic** fee-cap & eligibility checks → **browser research agent** (Anthropic SDK tool runner + Playwright) → HTML/JSON report + evidence folder.
- **Fabrication is structurally impossible, not just discouraged** — the model decides, but deterministic code produces the evidence: a "Found" can't be recorded without a real on-disk screenshot; quotes are rejected unless they appear verbatim on a visited page; timestamps, URLs, and SHA-256 hashes are burned in by code the model never touches.
- **Honest uncertainty as a feature** — only the website-verifiable subset of each checklist is answered; everything else is explicitly *"Internal — not answered"*, never guessed. For an audit tool, an honest "couldn't verify" is a correct answer; a fabricated "verified" is catastrophic.
- **Layered validation** — 18 deterministic tests, a rerunnable integrity audit over every evidence package, human ground-truthing of negative findings, and planted-trap cases the agent caught. Validation surfaced a real prompt bug — fixed and verified on rerun.

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
  <img src="https://skillicons.dev/icons?i=python,fastapi,docker,kubernetes,mongodb,postgres,aws,gcp,terraform,git,linux,nextjs&perline=12" alt="Python, FastAPI, Docker, Kubernetes, MongoDB, PostgreSQL, AWS, GCP, Terraform, Git, Linux, Next.js">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude%20%2F%20Anthropic%20SDK-D97757?style=flat-square&logo=claude&logoColor=white" alt="Claude / Anthropic SDK">
  <img src="https://img.shields.io/badge/OpenAI%20API-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI API">
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face">
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain">
  <img src="https://img.shields.io/badge/PydanticAI-E92063?style=flat-square&logo=pydantic&logoColor=white" alt="PydanticAI">
  <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square" alt="Qdrant">
  <img src="https://img.shields.io/badge/vLLM-4B8BBE?style=flat-square" alt="vLLM">
  <img src="https://img.shields.io/badge/LoRA%20%2F%20QLoRA-9C27B0?style=flat-square" alt="LoRA / QLoRA">
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright">
  <img src="https://img.shields.io/badge/RAG-FF6F00?style=flat-square" alt="RAG">
</p>

---

## 📫 Reach me

- 📧 [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)
- 🟢 Peerlist — [peerlist.io/ebinbt](https://peerlist.io/ebinbt)

<!-- TODO(Ebin): uncomment and fill these in as the profiles go live —
- 💼 LinkedIn — https://www.linkedin.com/in/YOUR-HANDLE
- 🧑‍💻 Upwork — YOUR-UPWORK-PROFILE-URL
- ✨ Contra — YOUR-CONTRA-PROFILE-URL
- 🌐 Portfolio — YOUR-SITE-URL
-->
