# 🙃 Sarcasm Detection using Context-Aware Pragmatic Metacognitive Prompting (CPMP)

> *"Machines that don't just read words — but actually understand what we mean."*

---

## 📌 About the Project

Sarcasm is one of the most challenging aspects of Natural Language Processing. This research project proposes a novel framework — **Context-Aware Pragmatic Metacognitive Prompting (CPMP)** — that goes beyond surface-level pattern matching to detect sarcasm the way humans do: with cultural awareness, contextual reasoning, and self-reflection.

The framework is evaluated on the **MaSaC** dataset — a Hinglish (Hindi + English) code-mixed corpus — and benchmarked against state-of-the-art LLMs including **GPT-4o** and **LLaMA-3-8B**.

---

## 🔍 Problem Statement

Standard AI models fail to detect sarcasm because:
- They interpret language **literally**, missing ironic intent
- They lack **cultural and contextual grounding**
- They cannot handle **code-mixed** languages like Hinglish
- They treat sarcasm as binary, ignoring its **spectrum of intensity**

---

## 💡 Proposed Framework: CPMP

The pipeline consists of **4 sequential phases**:

| Phase | Component | Function |
|-------|-----------|----------|
| I | **Context-Aware Retrieval** | Fetches real-world definitions for regional slang via search APIs |
| II | **Pragmatic Analysis** | Analyzes text through 4 linguistic lenses |
| III | **Metacognitive Reflection** | Model critiques its own reasoning to fix errors |
| IV | **Evaluative Output** | Issues a **Sarcasm Intensity Score** (0.0 – 1.0) |

### 🔬 The 4 Pragmatic Lenses (Phase II)
- **Implicature** — What is implied beyond the literal words?
- **Presupposition** — What assumptions underlie the statement?
- **Pretense** — Is the speaker adopting a facade for ironic effect?
- **Echoic Reminder** — Is there a reference to a failed expectation or subverted norm?

---

## 🛠️ Tech Stack

- **Language:** Python
- **Models Evaluated:** GPT-4o, Claude 3.5 Sonnet, LLaMA-3-8B
- **Dataset:** MaSaC (Hinglish Sarcasm Corpus), SARC (Reddit)
- **Retrieval:** Google Search API (for cultural grounding)
- **Libraries:** Transformers, LangChain, Pandas, NumPy

---

## 📂 Project Structure

```
sarcasm-detection/
├── data/
│   ├── masac/              # Hinglish dataset
│   └── sarc/               # Reddit-based dataset
├── prompts/
│   ├── grounding.txt       # Phase I prompt templates
│   ├── pragmatic.txt       # Phase II 4-lens analysis prompts
│   └── reflection.txt      # Phase III metacognitive prompts
├── src/
│   ├── retrieval.py        # Context-aware retrieval pipeline
│   ├── analysis.py         # Pragmatic analysis module
│   ├── reflection.py       # Metacognitive loop
│   └── evaluate.py         # Scoring and metrics
├── notebooks/
│   └── sarcasm_cpmp.ipynb  # Main experiment notebook
├── requirements.txt
└── README.md
```

---

## ⚙️ How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/sanikaa12-art/sarcasm.git
   cd sarcasm
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up API keys** (in a `.env` file):
   ```
   OPENAI_API_KEY=your_key_here
   GOOGLE_SEARCH_API_KEY=your_key_here
   ```

4. **Run the notebook:**
   ```bash
   jupyter notebook notebooks/sarcasm_cpmp.ipynb
   ```

---

## 📊 Evaluation Metrics

| Metric | Description |
|--------|-------------|
| **Macro-F1** | Primary classification metric |
| **Precision** | Accuracy of sarcasm predictions |
| **Recall** | Focus metric — catching *hidden* cultural sarcasm |
| **Sarcasm Intensity Score** | Continuous score (0.0–1.0) for nuanced detection |

> *Recall is prioritized to measure success in retrieving culturally masked sarcastic cases typically missed by non-context-aware baselines.*

---

## 📝 Key Findings

- CPMP outperforms standard Chain-of-Thought prompting on culturally diverse datasets
- **GPT-4o** achieves best results with sequential reasoning (CoC/GoC strategies)
- **LLaMA-3-8B** responds better to holistic prompting (Tensor of Cues)
- External retrieval significantly reduces "cultural hallucination" in model outputs

---

## 📄 Related Work

This project builds upon a chronological review of sarcasm detection research, including:
- Tepperman et al. (2006) — Prosodic cues for spoken sarcasm
- Riloff et al. (2013) — Sarcasm as positive sentiment + negative situation
- Khodak et al. (2018) — SARC: Large self-annotated Reddit corpus
- SarcasmBench (2024) — Benchmarking LLMs on sarcasm understanding
- Pragmatic Metacognitive Prompting (PMP) — The base framework extended here

---

## 🙋‍♀️ Author

**Sanikaa** — [GitHub](https://github.com/sanikaa12-art)

---

## 📃 License

This project is for academic/research purposes.
