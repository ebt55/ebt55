# Ebin Babu Thomas

Independent researcher · agent evaluations

[ebinbt.dev](https://ebinbt.dev) · [Resume (PDF)](https://ebinbt.dev/resume.pdf) · [linkedin.com/in/ebinbt](https://www.linkedin.com/in/ebinbt) · [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)

I build small evaluations of agent and model behaviour, and publish the code, the data and what failed. Three and a half years as an AI engineer, shipping LLM, RAG and agent backends for startup clients in the US, Canada, Europe and Australia. One merged open-source PR, listed below.

## Two projects

**[Kobayashi Maru](https://github.com/ebt55/kobayashi-maru): impossible tasks and agent cheating on the tasks beside them**
Turned the share of impossible tasks in an agent's batch into a dial and tested it on six models. Only one of the six spread clearly: DeepSeek-V4.1-flash went from **0 of 120 to 36 of 120 cheats on the solvable tasks at the top dose**, the same ten tasks it could still have done honestly, a dose trend with p = 8×10⁻⁶ over all 600 of its solvable runs. Preregistered, detectors in plain code, and the write-up states plainly which results survived correction.

**[diffing-agent-bench](https://github.com/ebt55/diffing-agent-bench): a sealed benchmark for black-box model-diffing agents**
Five LoRA finetunes of one base model, labels sealed before any run, each pair audited blind by an LLM agent asked to find what differs. In 13 attempts, my implementation of a published auditing recipe never asked the database question that finds the planted preference. A fixed 50-prompt battery I wrote, with four database questions in it, found it in one run. 8 of 40 audits run on the frontier model ended with no verdict, cut off by the provider's content classifier while the agent wrote test prompts. Every detection cell is 5 runs or fewer. The recipe is from Neel Nanda's group; this was my MATS 12 work sample.

## The rest of the work

| Project | What it is | One number | Status |
|---|---|---|---|
| [incidentgate](https://github.com/ebt55/incidentgate) | Lab for a policy gate, an action monitor and a stand-in approval step over an incident agent | 0 of 3 split-call steps a per-call policy gate could deny; with a 14B local monitor the forbidden end state still landed, in one scripted capture | closed at baseline, Sep 6 |
| [digital-grimace-scale](https://github.com/ebt55/digital-grimace-scale) | Preregistered test for involuntary markers of adverse treatment in LMs | False "Incorrect" feedback cut Gemma-2-9B's answer margin by 2.90 nats on easy items; the primary preregistered test failed | Apart Research sprint, Aug 2026 |
| [proofpack](https://github.com/ebt55/proofpack) | Pre-approval reviewer that cites a hashed screenshot for every finding | $0.02 to $0.19 of Gemini per review across seven synthetic sample forms | v0.2.0, no users yet |
| [whose-voice](https://github.com/ebt55/whose-voice) | Blind attribution of the principal behind a poisoned corpus, given one clean reference corpus from the same generator | 18 of 55 pooled decisions over five corpora name the right principal out of 47 candidates, chance 2.1%; the median single draw is 26% | Apart hackathon, Jul 2026; corrected Sep 2026 |
| [eval-floor](https://github.com/ebt55/evalfloor) | Runs each eval task's real scorer over its real dataset with completions that carry no information; no model is called | 1 of 20 tasks lets a content-free completion beat its own majority baseline, the case caiotheodoro reported first in inspect_evals [#2331](https://github.com/UKGovernmentBEIS/inspect_evals/issues/2331); four more tie by construction | first sweep |
| [odd-number-forensics](https://github.com/ebt55/odd-number-forensics) | Forensic study of a published reward-hacking environment | under 2% to 87% gaming for o3 across one-line edits to one prompt, 30 to 60 samples per cell | practice take-home |
| [exactdoc](https://github.com/ebt55/exactdoc) | PDF to editable DOCX, checked by rendering back and diffing | 16/16 page-count match on a frozen corpus, 0.9588 mean live-text retention | 1.0 |

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

Python, FastAPI, Inspect, LangGraph, Claude Agent SDK, PyTorch, Hugging Face Transformers and PEFT, vLLM, Playwright, PostgreSQL, Qdrant, Docker, pytest.

## Contact

- [ebinbabuthomas@gmail.com](mailto:ebinbabuthomas@gmail.com)
- [ebinbt.dev](https://ebinbt.dev)
- [linkedin.com/in/ebinbt](https://www.linkedin.com/in/ebinbt)
