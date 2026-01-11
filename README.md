# 🤖 Agentic Financial Analyst (RAG + LLM)

An **end-to-end Agentic Financial Analyst** that uses **LangChain + RAG** to analyze **PDF financial reports** and **CSV revenue data**, compute trends using **pandas**, and answer **natural‑language questions** via an **LLM agent**.

Built to be demo‑friendly, and easy to extend using **Python, SQL-style analytics, and modern LLM tooling**.

---

## 🚀 Features

* 📄 Upload **PDF financial reports** (earnings, annual reports)
* 📊 Upload **CSV revenue data** for structured analysis
* 🔍 **RAG pipeline** with chunking + vector embeddings (Chroma)
* 🧮 **Agent tools** for revenue trend & YoY growth analysis
* 💬 Ask natural‑language questions like:

  * *"What is the revenue trend over time?"*
  * *"Is revenue growing year over year?"*
  * *"Summarize financial performance from the report"*
* 🖥️ **Streamlit UI** for demos
* 🧠 Uses **Groq LLaMA‑3** (fast + free tier)

---

## 🧱 Project Structure

```text
financial-analyst-agent/
├── app.py                 # Streamlit UI
├── agent.py               # LLM agent + tools
├── analysis_tools.py      # Pandas-based financial analysis
├── rag_pipeline.py        # PDF/CSV loading + vector store
├── requirements.txt       # Dependencies
├── data/                  # Sample PDFs / CSVs
├── tests/                 # Simple test scripts
├── .env.example           # API key template
├── demo.gif               # Demo recording
└── README.md
```

---

## ⚙️ Tech Stack

* **Python 3.10+**
* **LangChain (Agents + RAG)**
* **Groq (LLaMA‑3‑8B)**
* **ChromaDB** – vector store
* **HuggingFace embeddings** (local, no OpenAI key needed)
* **PyMuPDF** – fast PDF text extraction
* **Pandas** – revenue & trend analysis
* **Streamlit** – UI
---

Upload:

* A **financial PDF** (earnings / annual report)
* Optional **CSV** with revenue data

Then ask questions in plain English.

## 🧠 How It Works (Architecture)

1. **Document Ingestion**

   * PDFs → PyMuPDF → LangChain Documents
   * CSVs → Pandas → text or structured parsing

2. **Text Chunking & Embeddings**

   * RecursiveCharacterTextSplitter
   * HuggingFace MiniLM embeddings

3. **Vector Store (RAG)**

   * ChromaDB for similarity search

4. **LLM Agent**

   * Retrieves relevant chunks
   * Calls custom tools for calculations

5. **Analysis Tool**

   * Pandas computes:

     * Total revenue
     * YoY growth
     * Trend direction

---

## 📊 Sample Queries

```text
• What are the revenue trends over time?
• Is the company's revenue growing year over year?
• Summarize key financial insights from the report
• What was the latest quarter's performance?
```




