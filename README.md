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

## Challenges I Faced

### 1. Library Version Conflicts
LangChain updates very frequently. Modules like
`langchain.chains` and `langchain.text_splitter`
were moved in newer versions and stopped working.
I had to uninstall and reinstall multiple times
to find the correct compatible versions.

### 2. Model Decommissioned Error
The Groq model `llama3-8b-8192` was deprecated
and no longer supported. I researched and switched
to `llama-3.3-70b-versatile` which gave better
and more accurate results.

### 3. API Key Security Issue
I accidentally exposed my Groq API key on GitHub.
GitHub's secret scanning detected it immediately.
I deleted the key, created a new one, and learned
the importance of never sharing API keys publicly.

### 4. PDF File Path Error
On Windows, the relative file path was not working
and giving a ValueError. I used `os.getcwd()` to
find the correct current directory and fixed the
file path issue.

### 5. Wrong Answers from GPT2
Initially I used GPT2 model which was giving
completely wrong answers by ignoring the PDF
context. I switched to Groq LLaMA model which
reads the context properly and gives accurate
answers.

## What I Learned
- How RAG Pipeline works end to end
- Practical use of LangChain
- FAISS vector store for document search
- Groq API integration with LLaMA model
- API key security best practices
- Debugging and fixing real world errors
