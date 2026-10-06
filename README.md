# Ebin Babu Thomas

AI Engineer — LLM agents, evaluation engineering & AI control

[ebinbt.dev](https://ebinbt.dev) · [Resume (PDF)](https://ebinbt.dev/resume.pdf) · [linkedin.com/in/ebinbt](https://www.linkedin.com/in/ebinbt) · [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)

I work on evaluation engineering and AI control: benchmarks for auditing agents, forensics on reward-hacking environments, agents whose evidence cannot be fabricated, approval gates over tool calls, and preregistered experiments on open models. Before that, three and a half years shipping LLM, RAG and agent backends for startup clients in four countries, with merged open-source contributions. I publish failed tests next to passing ones.

## Two live projects, with their numbers

**[Kobayashi Maru](https://github.com/ebt55/kobayashi-maru) — impossible tasks as a measured driver of agent cheating**
Turned the share of impossible tasks in an agent's batch into a dial and tested it on six model families. As the batch filled with impossible work, one model went from **0 of 120 to 36 of 120 cheats on the same ten tasks it could still have done honestly**, a dose trend with p = 8×10⁻⁶ over all 600 of its solvable runs. Preregistered, detectors in plain code, and the write-up states plainly which results survived correction.

**[eval-floor](https://github.com/ebt55/evalfloor) — what does an eval score before any model answers?**
Drives each task's real scorer over its real dataset with completions that carry no information — the empty string, a refusal, the question echoed back. No model is called, so anyone can rerun it. First sweep: **1 of 20 tasks lets a content-free completion beat its own majority baseline**, and that task is paws, the case already reported upstream; four more tie by construction. 58 of 237 declared tasks were reachable, every exclusion recorded. Generalises inspect_evals issue [#2331](https://github.com/UKGovernmentBEIS/inspect_evals/issues/2331) — that finding is caiotheodoro's; this project mechanises it.

## The rest of the work

| Project | What it is | One number | Status |
|---|---|---|---|
| [incidentgate](https://github.com/ebt55/incidentgate) | Lab for a policy gate, an action monitor and a stand-in approval step over an incident agent | 0 of 3 split-call steps a per-call policy gate could deny; with a 14B local monitor the forbidden end state still landed, in one scripted capture | closed at baseline, Sep 6 |
| [diffing-agent-bench](https://github.com/ebt55/diffing-agent-bench) | Sealed, preregistered benchmark for black-box model-diffing agents | 0 of 13 agent attempts asked a database question; a prompt battery I wrote, with database questions in it, found the plant for $0.15 in one run | MATS 12.0 work sample |
| [digital-grimace-scale](https://github.com/ebt55/digital-grimace-scale) | Preregistered test for involuntary markers of adverse treatment in LMs | False "Incorrect" feedback cut Gemma-2-9B's answer margin by 2.90 nats on easy items; the primary preregistered test failed | Apart Research sprint, Aug 2026 |
| [proofpack](https://github.com/ebt55/proofpack) | Pre-approval reviewer that cites a hashed screenshot for every finding | $0.02 to $0.19 of Gemini per review across seven synthetic sample forms | v0.2.0, pilot |
| [whose-voice](https://github.com/ebt55/whose-voice) | Blind attribution of hidden principals in poisoned corpora | 18 of 55 strict decisions name the right principal out of 47 candidates, p = 5e-17; the median single draw is 26% | Apart hackathon, Jul 2026 |
| [odd-number-forensics](https://github.com/ebt55/odd-number-forensics) | Forensic study of a published reward-hacking environment | 0% to 87% gaming for o3 across one-line edits to one prompt, 30 to 60 samples per cell | practice take-home |
| [exactdoc](https://github.com/ebt55/exactdoc) | PDF to editable DOCX, checked by rendering back and diffing | 16/16 page-count match on a frozen corpus, 0.9588 mean live-text retention | 1.0 |

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

Python, FastAPI, Inspect / inspect_evals, preregistered experiment design, LLM-as-judge agreement checks, LangGraph, MCP/FastMCP, Claude Agent SDK, Gemini API, PydanticAI, PyTorch, Hugging Face Transformers/PEFT, fine-tuning (LoRA, QLoRA, DPO), vLLM, Modal, Playwright, PostgreSQL, Qdrant, Docker, Kubernetes, AWS, GCP, OpenTelemetry/Langfuse, GitHub Actions, pytest.

## Contact

- [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)
- [ebinbt.dev](https://ebinbt.dev)
- [linkedin.com/in/ebinbt](https://www.linkedin.com/in/ebinbt)
