# -pdf-chatbot-rag
PDF Chatbot using RAG Pipeline with LangChain and Groq
# PDF Chatbot using RAG Pipeline

## What it does
Ask any question from a PDF file and get accurate answers using RAG.

## Tech Stack
- LangChain
- FAISS
- HuggingFace Embeddings
- Groq LLaMA 3.3
- PyPDF

## How it works
1. PDF load karo
2. Text chunks banao
3. FAISS vector store mein save karo
4. Question poochho
5. RAG pipeline accurate answer deta hai

## Setup
pip install langchain-groq langchain-community faiss-cpu pypdf sentence-transformers
