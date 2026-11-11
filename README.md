# LedgerLink-AI
LedgerLink AI, is a smart pre-accounting assistant built for small business owners who are drowning in messy paperwork like WhatsApp receipt photos and crumpled bills.

# LedgerLink AI 📊🤖

**A deterministic pre-accounting agent that converts messy MSME data into structured compliance ledgers without crossing the legal filing boundary.**

---

## 🚀 The Problem: The MSME Data Crisis
Micro-enterprise owners (traders, small manufacturers, transporters) lose 15-20 hours a month managing compliance paperwork. Their financial records exist as blurry photos, scattered voice notes, and chaotic WhatsApp text. By the time this unstructured data reaches a part-time accountant, it is often too late—resulting in delayed e-way bills, stalled consignments, and compliance penalties.

## 💡 Our Solution: Agentic Pre-Accounting
LedgerLink AI is a cognitive bridge between human chaos and machine rigidity. Instead of relying on a Large Language Model (LLM) to "do taxes" (which leads to dangerous mathematical hallucinations), we implemented a **Deterministic Pipeline**:

1. **The AI Extractor (Cognitive Bridge):** Reads the messy input (e.g., a WhatsApp message) and locks the extracted entities into a strict, validated schema.
2. **The Python Verifier (Programmatic Guardrails):** Pure Python code takes over to run the math. It calculates GST compliance, checks for missing data, and flags if an invoice crosses the ₹50,000 threshold requiring an urgent e-way bill.
3. **The Accountant Handoff:** Generates a perfectly structured, error-free JSON ledger marked *"Ready for Accountant Review."* 

We prepare the data; the accountant files it 5x faster.

## 🛠️ Architecture & Tech Stack
* **Language:** Python
* **AI Model:** Google Gemini (via `google-generativeai` SDK)
* **Schema Enforcement:** Pydantic (Strict typing for JSON output)
* **Environment:** Google Colab

---

## ⚙️ How to Run Locally (Google Colab)

We designed this project to be instantly reproducible for hackathon judges. You do not need to clone this repository to a local machine.

### Step 1: Set up your API Key
1. Get a free Gemini API key from [Google AI Studio](https://aistudio.google.com/).
2. Open a new [Google Colab Notebook](https://colab.research.google.com/).
3. Click the **Key icon (Secrets)** on the left sidebar.
4. Add a new secret named exactly `GEMINI_API_KEY` and paste your key.
5. Toggle the button to grant notebook access.

### Step 2: Run the Pipeline
Copy the main code block from `main.py` (or paste the provided Python script) into a Colab cell. The script will automatically install dependencies:
```python
!pip install -q -U google-generativeai pydantic
