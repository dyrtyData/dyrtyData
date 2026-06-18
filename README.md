## 🛠️ Featured Projects

### 🛰️ [STAR-Pipeline — Space Telemetry Anomaly Detection & Resolution](https://github.com/dyrtyData/space-telemetry-anom-llm)
An end-to-end open-source ML pipeline built on the **ESA Anomaly Dataset (ESA-AD)** that combines time-series anomaly detection with LLM-generated diagnostic reasoning.

* **The Architecture:** Engineered a stacked ensemble fusing classic **LSTMs**, fine-tuned text LLMs (**Qwen3-8B** via QLoRA), and vision transformers (**Qwen3-VL-8B** scanning rendered telemetry PNGs) to drive automated satellite health monitoring.
* **The Breakthrough:** Conducted a comprehensive 13-approach benchmark showing that while fine-tuned LLMs alone struggled with over-flagging calibration artifacts, a multi-modal fused stacker achieved a state-of-the-art **$CEF_{0.5}$ score of 0.781**—proving that ensemble detection coupled with LLM advisory logic yields the highest operational reliability.
* **Stack:** Python, PyTorch, QLoRA, GGUF/llama.cpp (Local Metal Inference), Scikit-Learn, Time-Series LSTMs.



## 🚀 Open Source Contributions

* **[NVIDIA/garak](https://github.com/NVIDIA/garak)** • [PR #1379](https://github.com/NVIDIA/garak/pull/1379): Architected and implemented the core WebSocket generator module using the `websockets` library, expanding LLM vulnerability scanning capabilities to support real-time, bidirectional chat architectures with full authentication handling.

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
