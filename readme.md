#  Conversational PDF RAG Chatbot with Chat History

A mini RAG application built using **LangChain**, **Streamlit**, **Groq's LLaMA3 model**, and **Chroma vector store**, allowing users to upload PDF documents and chat conversationally with them — preserving **chat history** across a session.

---

##  What It Does

- Upload a **PDF file** and chat with its content
- Uses **LangChain's History-Aware Retrieval Chain**
- Automatically rewrites follow-up questions to be **contextual**
- Answers are generated using **Groq-hosted LLaMA3-8b**
- Stores and displays **chat history** session-wise

---

##  How It Works

| Component                  | Role                                                                 |
|---------------------------|----------------------------------------------------------------------|
| `LangChain`               | Chain creation, prompt templates, memory integration                 |
| `ChatGroq`                | LLM used for both retriever and answer generation (LLaMA3-8b)         |
| `Chroma` VectorStore      | Stores PDF chunks for fast retrieval                                 |
| `HuggingFace Embeddings`  | `all-MiniLM-L6-v2` model used for chunk embedding                    |
| `Streamlit`               | UI for uploading PDFs and asking questions                           |
| `RunnableWithMessageHistory` | Maintains chat history session-wise using LangChain memory        |

