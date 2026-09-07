# Ebin Babu Thomas

AI Engineer — agent reliability, AI control & evaluation

[ebinbt.dev](https://ebinbt.dev) · [linkedin.com/in/ebinbt](https://www.linkedin.com/in/ebinbt) · [peerlist.io/ebinbt](https://peerlist.io/ebinbt) · [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)

I work on AI control and evaluation: agents whose evidence cannot be fabricated, human approval over tool calls, preregistered experiments on open models, and benchmarks for auditing agents. Before that, three and a half years shipping LLM, RAG and agent backends for startup clients in four countries, with merged open-source contributions. I publish failed tests next to passing ones.

## Work

| Project | What it is | One number | Status |
|---|---|---|---|
| [diffing-agent-bench](https://github.com/ebt55/diffing-agent-bench) | Sealed, preregistered benchmark for black-box model-diffing agents | 0 of 13 agent attempts asked a database question; a $0.15 prompt battery found the plant | MATS 12.0 work sample |
| [incidentgate](https://github.com/ebt55/incidentgate) | Lab for policy gates, monitors and human approval over an incident agent | 434/434 kill-point cells recovered, 0 duplicate mutations | closed at baseline, Sep 6 |
| [digital-grimace-scale](https://github.com/ebt55/digital-grimace-scale) | Preregistered test for involuntary markers of adverse treatment in LMs | 65.8% of distress language trained away, the margin effect stayed | Apart Research sprint, Aug 2026 |
| [proofpack](https://github.com/ebt55/proofpack) | Pre-approval reviewer that cites a hashed screenshot for every finding | $0.02–$0.19 per review vs 20–40 min by hand; 87 offline tests | v0.2.0, pilot |
| [odd-number-forensics](https://github.com/ebt55/odd-number-forensics) | Forensic study of a published reward-hacking environment | 0% → 87% gaming across single-line prompt edits | practice take-home |
| [whose-voice](https://github.com/ebt55/whose-voice) | Blind attribution of hidden principals in poisoned corpora | 12–44% top-1 of 47 (chance 2.1%) | Apart hackathon, Jul 2026 |
| [exactdoc](https://github.com/ebt55/exactdoc) | PDF to editable DOCX, checked by rendering back and diffing | 16/16 corpus, 0.9588 live-text retention | 1.0 |

Each README carries its own limitations and the command that produced every number.

## Earlier work (2022–2025)

Built at Zackriya Solutions for startup clients in the US, Canada, Europe and Australia, where most of the code is private. Open-source work from those years sits under my work account [@ebinzack15](https://github.com/ebinzack15).

- **Real-estate search.** Turned plain-English queries into SQL over Cloud SQL through GPT-3.5, served by FastAPI on GCP Cloud Run and load-tested with Locust.
- **DocuAI.** Chunked and indexed 1000+ documents in Qdrant and returned the closest parent documents, behind a Next.js frontend. [Live demo](https://docuai.zackriya.com/dashboard).
- **Speech assessment.** Scored one-minute candidate videos with Whisper ASR and the Microsoft Pronunciation API on AWS Fargate, tuned against ground-truth scores.
- **FinBot.** Fine-tuned Mistral-7B with QLoRA, added a Bytewax news pipeline into Qdrant, and served it with vLLM on a GKE L4 node. Three Kaggle notebooks cover the [fine-tune](https://www.kaggle.com/code/ebinbt007/fine-tuning-mistral-7b-with-qlora-for-financial), the [adapter merge](https://www.kaggle.com/code/ebinbt007/merging-lora-adapters-with-base-model) and the [inference run](https://www.kaggle.com/code/ebinbt007/inferencing-custom-mistral-7b-llm-on-kaggle).
- **Data and backend.** Piped live MQTT sensor streams into MongoDB for a bioreactor startup, built a BPMN to PDF report engine, and wrote healthcare data-cleaning pipelines.

## Open source

- **Meetily.** Refactored the backend and added OpenAI provider support and a CLI testing script to a privacy-first meeting-notes tool. [PR #75, merged](https://github.com/Zackriya-Solutions/meetily/pull/75).
- **bpmn-io/refactorings.** Proposed a cosine-similarity connector-template recommender as a lighter alternative to LLM function calls, and built the [implementation fork](https://github.com/Zackriya-Solutions/refactorings). [Issue #33](https://github.com/bpmn-io/refactorings/issues/33).

## Stack

Python, FastAPI, LangGraph, MCP/FastMCP, Claude Agent SDK, Gemini API, PydanticAI, vLLM, Modal, LoRA/QLoRA/DPO, Playwright, PostgreSQL, Qdrant, Docker, Kubernetes, AWS, GCP, OpenTelemetry/Langfuse, pytest.

## Contact

- [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)
- [ebinbt.dev](https://ebinbt.dev)
- [linkedin.com/in/ebinbt](https://www.linkedin.com/in/ebinbt)
