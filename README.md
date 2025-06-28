# RAG-based-PDF-Question-Answering-System

This project implements a **Retrieval-Augmented Generation (RAG)** system that allows users to upload PDF documents and ask questions based on their content. It combines modern NLP techniques like document chunking, semantic embedding, and language model inference to provide accurate answers grounded in the uploaded documents.

##  Features

- 📄 Upload any PDF document
- 🔍 Automatically extract and split text into meaningful chunks
- 🧠 Generate embeddings using Sentence Transformers
- 🧾 Store and retrieve relevant context using Chroma Vector Store
- 🤖 Generate context-aware answers using Hugging Face language models (e.g., `flan-t5-large`)
- 🌐 Interactive user interface using **Gradio**

##  Tech Stack

| Tool | Purpose |
|------|---------|
| `PyPDF2` | PDF text extraction |
| `langchain` | Text chunking and retrieval framework |
| `sentence-transformers` | Dense embedding generation |
| `chromadb` | Local vector database |
| `Hugging Face Transformers` | LLM API for generation |
| `Gradio` | Web interface for user interaction |

##  System Architecture

```mermaid
graph LR
A[PDF Upload] --> B[Text Extraction]
B --> C[Text Chunking]
C --> D[Embedding with Sentence Transformers]
D --> E[Store in Chroma Vector DB]
F[User Question] --> G[Retrieve Relevant Chunks]
G --> H[Send Context + Question to LLM]
H --> I[Answer Generated]
I --> J[Displayed via Gradio UI]
