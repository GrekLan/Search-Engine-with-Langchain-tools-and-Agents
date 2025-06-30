
# AI-Powered Chat & Search Projects

This repository contains two Streamlit-based AI applications built with LangChain, Groq LLMs, and external tools:

1. **Conversational RAG Q&A Chatbot**  
2. **LangChain Multi‑Source Search Agent**

---

## 1. Conversational RAG Q&A Chatbot

A PDF‑powered, multi‑turn question‑answering chatbot built with LangChain, ChromaDB, and Groq LLMs. Upload one or more PDF documents and engage in context‑aware conversations that remember your chat history and deliver precise, concise answers.

### 🚀 Key Features
- **Retrieval‑Augmented Generation (RAG):**  
  Reformulates user questions against past chat context, then retrieves relevant document chunks to ensure accurate, standalone answers.
- **Persistent Chat History:**  
  Uses `RunnableWithMessageHistory` to store session‑specific histories—enabling seamless follow‑up questions and contextual continuity.
- **Vector Search with ChromaDB:**  
  Splits PDFs into embeddings via HuggingFace’s `all-MiniLM-L6-v2` model and performs semantic search over your uploaded files.
- **LangChain Prompt Templates & Agents:**  
  Leverages custom system prompts and LangChain’s history‑aware retriever for dynamic question reformulation and response synthesis.
- **Interactive Streamlit UI:**  
  Intuitive front‑end for PDF uploads, API‑key management, live chat, and session ID selection—no code required to get started.

### ⚙️ Tech Stack
- **Core:** Python, LangChain  
- **LLM:** Groq’s Gemma2 (via `langchain_groq`)  
- **Embeddings:** HuggingFace Embeddings (`all-MiniLM-L6-v2`)  
- **Vector Store:** ChromaDB  
- **UI:** Streamlit  
- **Document Loader:** `PyPDFLoader`  
- **Text Splitting:** `RecursiveCharacterTextSplitter`  
- **History Management:** LangChain Community `ChatMessageHistory`  

### 💡 Usage
1. Clone the repo and install dependencies:  
   ```bash
   git clone https://github.com/YourUsername/ai-chat-search.git
   cd ai-chat-search
   pip install -r requirements.txt
2. Create a .env file with your API keys:
  HF_TOKEN=<your_huggingface_token>
  GROQ_API_KEY=<your_groq_api_key>

3.Run the Streamlit app:
  streamlit run app_chat.py

4.In the browser UI:
  Enter your Groq API key.

Upload one or more PDF files.

Enter a unique Session ID.

Ask questions!
