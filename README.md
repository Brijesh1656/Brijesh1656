# Brijesh Singh

**I measure what happens to retrieval quality as an AI agent keeps reasoning, using a tutoring system I built and put in front of real users.**

Independent researcher and AI/ML engineer · Hyderabad, India

---

## 🔬 Research

### Retrieval Degradation in Multi-Turn Agentic RAG Systems
*Observations from a Production Deployment*

Single-turn RAG benchmarks assume one query and one retrieval. Agentic systems don't work that way: each reasoning turn retrieves again, on top of a context window that keeps growing. I instrumented a live system to see what that does.

**150 sessions · 550 turns · real users**

- Mean retrieval relevance fell **6.6%** between turn 1 and turn 4 (p < 0.0001), while context grew **4.3×** (482 → 2,095 tokens)
- Context length and retrieval similarity were negatively correlated (**r = −0.283, p < 0.0001**)
- A simple context-length signal (AUROC 0.695) beat my composite turn-aware estimator (0.634) at flagging degraded retrieval
- Keeping the original query anchored through every turn appears to protect answer quality even as retrieval similarity drops

Limitations are stated in the paper: one system, one domain (math), a closed-source LLM, and only 8 incorrect labels, so the estimator results are preliminary.

📄 **[Paper, data and code →](https://github.com/Brijesh1656/rag-degradation-paper)**

*I'm looking for an arXiv cs.CL endorser for this paper. If that's you, please email me.*

---

## 🛠️ Things I've built

**[Math-Professor-Ai](https://github.com/Brijesh1656/Math-Professor-Ai)** · [live](https://math-professor-agent-k6h4.vercel.app)
The deployed system behind the paper. A dual-model Gemini 2.5 tutor that splits a problem into sub-queries, retrieves for each (TF-IDF, then a knowledge base, then web search), and logs retrieval quality at every turn.

**[Stock-Analysis-Pro](https://github.com/Brijesh1656/Stock-Analysis-Pro)** · [live](https://stock-analysispro.streamlit.app/)
Technical analysis app with RSI, MACD and Bollinger indicators, strategy backtesting (Sharpe, drawdown, win rate), and chart reading by a local Llama vision model. Exports PDF and CSV.

**[SAKURA](https://github.com/Brijesh1656/SAKURA)**
Keeps an anime character looking like the same character across AI-generated images, using face embeddings and CLIP for identity plus style preservation. Detects the GPU and tunes batch size automatically. FastAPI, React, Docker.

**[SMART-FACTORY-ANALYTICS](https://github.com/Brijesh1656/SMART-FACTORY-ANALYTICS)**
Predictive maintenance, anomaly detection and yield estimation on simulated sensor data, with a Next.js dashboard. *A simulation project, not a real factory system.*

**[GeminiFlow](https://github.com/Brijesh1656/GeminiFlow)**
Gemini chatbot with conversational memory.

---

## 🌐 Open source

**Merged** into [Alibaba-NLP/DeepResearch #133](https://github.com/Alibaba-NLP/DeepResearch/pull/133): replaced a fake `"EMPTY"` API key with a clear error telling users exactly what to set (fixes #130).

---

## 🧰 Stack

Python · TypeScript · FastAPI · Next.js · React · scikit-learn · Docker · Linux · LaTeX

## 🎓 Background

BBA in Business Analytics, ROOTS Collegium, Hyderabad (Osmania University), 2026
IBM Data Science Professional Certificate
Self-taught in ML and AI

---

## 📫 Contact

[singh.brijesh.ac@gmail.com](mailto:singh.brijesh.ac@gmail.com) · [LinkedIn](https://www.linkedin.com/in/brijesh-singh-b84275307) · [ORCID](https://orcid.org/0009-0009-7293-0550) · [Portfolio](https://brijeshsingh-ai.netlify.app)
