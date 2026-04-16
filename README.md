👽 RAG PDFBot - Enterprise Edition (FastAPI + Streamlit)
Developed by tsskrishna. This is a high-performance, production-ready RAG (Retrieval-Augmented Generation) system. It features a complete separation of concerns with a FastAPI backend handling the heavy AI logic and a Streamlit frontend providing a seamless user experience.
🏗️ Architecture Overview
This project implements a modular RAG pipeline designed for scalability:
Frontend: Streamlit-based client for PDF uploads and real-time chat.
Backend: FastAPI server managing vector embeddings and LLM orchestration.
Database: ChromaDB for high-speed semantic search.
🚀 Key Features
Multi-PDF Support: Upload and analyze multiple documents simultaneously.
Provider Agnostic: Seamlessly switch between Groq and Google Gemini LLMs.
Vector Inspector: Real-time transparency into the retrieval process.
Advanced Chunking: Uses TokenTextSplitter for precise context window management.
Async Processing: Built on FastAPI to handle concurrent user requests efficiently.
Exportable Insights: Download chat history as CSV for auditing and review.
🛠️ Tech Stack
Orchestration: LangChain
API Framework: FastAPI
UI Framework: Streamlit
Vector Store: ChromaDB
Embeddings: HuggingFace & Google GenAI
Parsing: PyPDF
📦 Installation & Setup
Clone the repository:
git clone [https://github.com/tsskrishna/rag-bot-fastapi.git](https://github.com/tsskrishna/rag-bot-fastapi.git)
cd rag-bot-fastapi


Setup Virtual Environment:
python -m venv venv
# Windows
venv\Scripts\activate
# Mac/Linux
source venv\bin\activate


Install Backend Dependencies:
cd server
pip install -r requirements.txt


Install Frontend Dependencies:
cd ../client
pip install -r requirements.txt


🔐 Configuration
Create a .env file in the root directory:
GROQ_API_KEY=your-groq-key
GOOGLE_API_KEY=your-google-key


▶️ Execution Instructions
1. Start the FastAPI Backend:
cd server
uvicorn main:app --reload


2. Start the Streamlit Frontend:
cd client
streamlit run app.py


📁 Project Structure
rag-bot-fastapi/
├── client/          # Streamlit Frontend (UI & Components)
├── server/          # FastAPI Backend (Routes & Core AI Logic)
│   ├── api/         # Endpoints & Pydantic Schemas
│   ├── core/        # Document processing & Vector DB management
│   └── main.py      # Entry point
└── README.md


🤝 Acknowledgements
LangChain for the orchestration framework.
Google & Groq for providing state-of-the-art LLM access.
Chroma for the vector database implementation.
