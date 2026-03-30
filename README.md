📄 DOC-AI — RAG PDF Chatbot

An AI-powered document assistant that lets users upload PDFs and chat with them using LLM + RAG (Retrieval Augmented Generation).

Built as a full-stack AI application for portfolio and deployment.

🚀 Features

• Upload PDF documents
• Ask questions about uploaded files
• AI answers using document context
• Source-aware responses (no hallucination mode)
• Session reset (new chat = new knowledge base)
• Clean chat UI
• Ready for cloud deployment

🧠 How it Works (RAG Pipeline)
User uploads a PDF
Text is extracted & chunked
Chunks → embeddings
Stored in Chroma Vector Database
User asks a question
Relevant chunks retrieved
LLM generates contextual answer

This prevents hallucinations and ensures answers come from the document.

🏗️ Tech Stack
Frontend
Reflex (Python full-stack framework)
Reactive chat UI
Backend
Python
LangChain
ChromaDB (Vector Database)
Ollama / OpenAI compatible LLM
AI / NLP
Embedding model
Retrieval Augmented Generation (RAG)
📂 Project Structure
DOC_AI/
│
├── app/                # Reflex frontend
│   ├── state.py
│   ├── ui.py
│   └── app.py
│
├── backend/
│   ├── rag.py          # RAG pipeline
│   ├── ingest.py
│   └── utils.py
│
├── documents/          # Uploaded PDFs
├── chroma_db/          # Vector database
├── .env                # API keys
└── README.md
⚙️ Setup Instructions
1️⃣ Clone repo
git clone https://github.com/your-username/doc-ai.git
cd doc-ai
2️⃣ Create virtual environment
python -m venv venv
venv\Scripts\activate   # Windows
3️⃣ Install dependencies
pip install -r requirements.txt
4️⃣ Add API key

Create .env file in root folder:

OPENAI_API_KEY=your_api_key_here
5️⃣ Run the app
reflex run

App runs at:

http://localhost:3000

🔄 Reset Session Feature

Click Clear History to:

• Delete chat history
• Reset vector database
• Start fresh conversation

This mimics ChatGPT “New Chat”.
