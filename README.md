# ⚖️ Local AI Legal Agent Team

This project is a powerful **local legal document analysis tool** built with **Streamlit**, **Qdrant**, and **LLM agents (Ollama / LLaMA3)**. It allows you to upload legal documents (PDFs) and run intelligent analyses like contract review, legal research, compliance checks, and more — **all running locally** with privacy and control.

---

## 📁 Project Contents

- `local_legal_agent.py` – Main Streamlit app
- Requires Qdrant running locally on `http://localhost:6333`
- Supports PDF upload and vector-based semantic search

---

## 🧠 How It Works

1. **Upload PDF** → Chunked and embedded into Qdrant
2. **Legal Knowledge Base** → Created from vectorized text
3. **AI Agents** → LLaMA3-powered specialists:
   - 📚 Legal Researcher
   - 📄 Contract Analyst
   - 🧠 Legal Strategist
4. **Team Agent** → Coordinates all sub-agents for robust analysis

---

## 🚀 Getting Started

### ✅ Prerequisites

- Python 3.9+
- Ollama (LLaMA3 model installed locally)
- Qdrant (running locally on port 6333)

### ✅ Install Python Dependencies

```bash
pip install streamlit agno
⚠️ agno is the framework used for agent orchestration. Make sure it's installed and up to date.

✅ Start Qdrant Locally
bash
Copy
Edit
docker run -p 6333:6333 -p 6334:6334 qdrant/qdrant
This sets up the local vector database required to store and query document chunks.

✅ Launch the App
bash
Copy
Edit
streamlit run local_legal_agent.py
📄 Features
📥 Upload legal PDFs (e.g., contracts, policies)

🧠 Auto-vectorize documents using OllamaEmbedder

🤖 Auto-initialize AI agent team:

Contract Analyst

Legal Researcher

Legal Strategist

🔍 Choose from 5 smart analysis modes:

Contract Review

Legal Research

Risk Assessment

Compliance Check

Custom Query

📌 Get structured output in tabs:

Analysis

Key Points

Recommendations

🧩 Example Use Cases
Law Firms: Rapid contract analysis and risk identification

Compliance Teams: Automated document checks

Startups: Legal validation of partnership agreements

Researchers: Extracting key legal insights from case studies

🛠️ Technologies Used
Component	Tool / Library
Frontend	Streamlit
LLM Model	Ollama (LLaMA3)
Vector DB	Qdrant (local)
Agents	agno
Embedding	OllamaEmbedder
Knowledge Base	PDFKnowledgeBase

📌 Notes
All computation is local — no cloud APIs needed

Make sure Ollama is running and the LLaMA3 model (llama3.1:8b) is downloaded

App verifies the knowledge base before allowing analysis

📄 License
MIT License – free to use and adapt.

🙋 Want to Extend?
You can:

Integrate with private cloud LLMs

Add file type support (e.g. DOCX)

Connect to CRM, case logs, or legal databases

Add summarization or citation outputs
