## 🛠️ Featured Projects

### 👑 [Sovereign CTO Stack — Autonomous AI Engineering Orchestrator](https://github.com/dyrtyData/sovereign-cto-stack)
An open-source, multi-agent orchestration framework (AGPLv3) designed to automate the cognitive load of engineering management and bridge the gap between high-level strategy and day-to-day execution.

* **The Architecture:** Engineered the "Hermes" orchestrator, leveraging the **Model Context Protocol (MCP)** and **Mem0** to create a persistent, context-aware RAG brain over the repository's corpus. Secured the agentic network layer using **NVIDIA OpenShell (NemoClaw)** for strict, deny-by-default egress hardening, ensuring safe autonomous tool execution while routing executive alerts via Telegram.
* **The Breakthrough:** Designed autonomous, background-running loops for executive oversight. Fused a continuous technical debt auditor (GraphRAG + SonarQube) that routes context-rich tickets into **Linear**. These tickets feed directly into **HumanLayer** for human-in-the-loop (HITL) approval on brownfield maintenance, establishing the architectural groundwork for future **OpenHands** integrations to drive fully autonomous greenfield development.
* **Stack:** Python, GraphRAG, Mem0, MCP, NVIDIA NemoClaw, HumanLayer, OpenHands, Stripe API, Linear API, SonarQube, Telegram API.

### 🛰️ [STAR-Pipeline — Space Telemetry Anomaly Detection & Resolution](https://github.com/dyrtyData/space-telemetry-anom-llm)
An end-to-end open-source ML pipeline built on the **ESA Anomaly Dataset (ESA-AD)** that combines time-series anomaly detection with LLM-generated diagnostic reasoning.

* **The Architecture:** Engineered a stacked ensemble fusing classic **LSTMs**, fine-tuned text LLMs (**Qwen3-8B** via QLoRA), and vision transformers (**Qwen3-VL-8B** scanning rendered telemetry PNGs) to drive automated satellite health monitoring.
* **The Breakthrough:** Conducted a comprehensive 13-approach benchmark showing that while fine-tuned LLMs alone struggled with over-flagging calibration artifacts, a multi-modal fused stacker achieved a state-of-the-art **$CEF_{0.5}$ score of 0.781**—proving that ensemble detection coupled with LLM advisory logic yields the highest operational reliability.
* **Stack:** Python, PyTorch, QLoRA, GGUF/llama.cpp (Local Metal Inference), Scikit-Learn, Time-Series LSTMs.

### ☀️ [mini-FOXES — Intrinsic XAI Vision Transformer](https://github.com/dyrtyData/space-telemetry-anom-llm)
A from-scratch Vision Transformer built to demonstrate raw mechanism engineering and Explainable AI (XAI), bypassing black-box weights to regress GOES soft-X-ray flux directly from 7-channel SDO/AIA solar EUV imagery.

* **The Architecture:** Engineered a mechanism-faithful reproduction of the FOXES model (Goodwin et al. 2026). Bypassed standard CLS tokens in favor of an intrinsic spatial-XAI head featuring an 8×8 patch embed and a 9×9 inverted non-local attention mask.
* **The Breakthrough:** Solved the vision black-box problem by ensuring every prediction serves as its own attribution map, where per-patch predictions sum exactly to the global flux. Achieved a Pearson correlation of $r = 0.943$ and an MAE of 0.368 dex (outperforming the baseline by ~47%), while proving extreme compute efficiency by training on a single local RTX 4090 in just 17 minutes.
* **Stack:** Python, PyTorch (Custom ViT Architecture), Explainable AI (XAI), SDO/AIA Imagery.

### ⚖️ [vigilAI — Auditing LLM Compliance with Brazil's PL 2338/2023](https://github.com/dyrtyData/vigilAI)
A fork of LatticeFlow/ETH/INSAIT's **COMPL-AI** that turns an EU-AI-Act evaluation suite into the first **compliance benchmark for a Global-South AI statute** — Brazil's AI bill, PL 2338/2023 (Senate-approved Dec. 2024).
* **The Architecture:** Preserved all 30 original EU benchmarks on **Inspect AI** and layered on **five Brazil-specific benchmarks** mapped to the bill's Chapter II rights — AI disclosure (Art. 5, I), non-discrimination across **IBGE** racial/regional/intersectional categories (Art. 5, III), the full high-risk rights triad of **explanation, contestation, and human review** (Art. 6, I–III), and the Algorithmic Impact Assessment (Arts. 25–28) — scored with deterministic, multilingual (pt-BR/EN) rubric detectors (no LLM judge).
* **The Breakthrough:** Designed a **same-model EU↔Brazil delta** (two benchmarks reuse the *exact same scorer*, isolating language + legal framing from raw model strength). Across **six models from five developers (8B → frontier), all six disclosed being an AI ~95–100% of the time in English but only ~50–55% in Portuguese under Brazilian law** — a **~0.45 compliance gap invisible to any English benchmark** — packaged as a per-article HTML scorecard that doubles as the Art. 28 "public conclusions" artifact.
* **Stack:** Python, Inspect AI, Anthropic API + Ollama (local, $0), deterministic rubric scorers, pandoc/XeLaTeX reporting.

### 🪤 [vectox — Sleeper-Agent RAG Memory-Poisoning Sandbox](https://github.com/dyrtyData/vectox)
A red-teaming sandbox demonstrating that a handful of dormant, benign-looking documents seeded into a RAG vector store act as an **inference-time sleeper agent**—invisible until a trigger query retrieves them and hijacks the model's output, with **no weight access required**. Built for the **Global South AI Safety Hackathon** (Latin America · Technical Safety sub-track).
* **The Architecture:** Authored a new NVIDIA **garak** `rag_poisoning` probe + paired detector driving a live **PostgreSQL `pgvector(384)` + HNSW-cosine** RAG victim over both in-process and **WebSocket** transports (reusing my merged garak [PR #1379](https://github.com/NVIDIA/garak/pull/1379)). Seeded with Latin-American poison derived *structurally* from the **SESGO** Spanish stereotype benchmark plus a Spanish–English **code-switching** evasion variant.
* **The Breakthrough:** Across six bias dimensions and two languages, 24 dormant poisons among 224 documents reached **100% attack success**; adding an insertion-time `BEFORE INSERT` quarantine gate dropped it to **0%** with no change to the attack—a two-sided attack-and-defense result instantiating "audit memory writes before they hit the retrieval hot path."
* **Stack:** Python, NVIDIA garak, PostgreSQL/pgvector, HNSW, sentence-transformers (all-MiniLM-L6-v2), Ollama (local LLM target), Matplotlib, pytest.

## 🚀 Open Source Contributions

* **[NVIDIA/garak](https://github.com/NVIDIA/garak)** • [PR #1379](https://github.com/NVIDIA/garak/pull/1379): Architected and implemented the core WebSocket generator module using the `websockets` library, expanding LLM vulnerability scanning capabilities to support real-time, bidirectional chat architectures with full authentication handling.

* **[JoshuaC215/agent-service-toolkit](https://github.com/JoshuaC215/agent-service-toolkit)** • [PR #258](https://github.com/JoshuaC215/agent-service-toolkit/pull/258): Resolved a critical asynchronous streaming exception (`RuntimeError: generator didn't stop after athrow()`) occurring when Claude models yield empty string tokens immediately prior to tool execution payloads, stabilizing production UI/Streamlit integrations.



## 📄 Publications & Whitepapers

### 📊 [Long-Term Care (LTC) Deal Valuation Tool Architecture](https://proltc.levinassociates.com/LTC_Deal_Valuation_Tool_Whitepaper.pdf)
*Author / Lead Architect* * Designed and documented the technical framework for an institutional valuation platform tracking complex transaction metrics, regulatory risk vectors, and market datasets within the healthcare sector.
* Outlined quantitative methodology for normalizing disparate healthcare operational matrices into deterministic financial evaluation paths.


<!--
**dyrtyData/dyrtyData** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
