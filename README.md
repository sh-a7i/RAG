# KnowledgeSphere: AI-Powered RAG Knowledge Assistant

KnowledgeSphere is a Retrieval-Augmented Generation (RAG) application that lets you chat with your documents. Upload PDFs, ask questions in natural language, and get answers grounded in your source material — complete with inline citations and a split-screen PDF viewer that jumps straight to the cited page.

## Features

- 📄 **Multi-file PDF ingestion** — upload and index multiple documents at once
- 💬 **Conversational chat interface** — ask follow-up questions with full chat history context
- 🔗 **Inline page citations** — click a source button to jump directly to the cited page in the PDF viewer
- 🖥️ **Split-screen PDF viewer** — read answers and source documents side by side
- 🔍 **Hybrid retrieval** — combines semantic and keyword-based (BM25) search for more accurate results
- ⚡ **Fast inference** — powered by Groq for low-latency LLM responses

## Tech Stack

- **Frontend:** Streamlit
- **LLM Orchestration:** LangChain
- **LLM Inference:** Groq
- **Vector Store:** ChromaDB
- **Document Parsing:** Unstructured

## Getting Started

### Prerequisites
- Python 3.10+
- A Groq API key ([console.groq.com](https://console.groq.com))

### Installation

\`\`\`bash
git clone https://github.com/angiedmn/KnowledgeSphere.git
cd KnowledgeSphere
python -m venv venv
venv\Scripts\activate  # On Windows
pip install -r requirements.txt
\`\`\`

### Configuration
Create a `.env` file in the root directory:
GROQ_API_KEY=your_api_key_here

### Running the App
streamlit run streamlit_app.py

## Project Structure
├── app.py                    # Main application entry point
├── streamlit_app.py          # Streamlit UI
├── conversational_RAG.py     # Core RAG pipeline logic
├── ingestion.py               # Document ingestion pipeline
├── generation.py              # Answer generation logic
├── Hybrid_retriever.py       # Hybrid (semantic + keyword) retrieval
├── mul_query.py               # Multi-query retrieval logic
├── config.py                  # Configuration and constants
└── stored_docs/                # Uploaded document storage
