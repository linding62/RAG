# 📘 Retrieval‑Augmented Generation (RAG) System  
*A complete, end‑to‑end implementation using Gemini, LangChain, and ChromaDB*

---

## 🚀 Overview

This repository provides a fully documented, step‑by‑step implementation of a **Retrieval‑Augmented Generation (RAG)** system using:

- **Gemini** for LLM reasoning  
- **LangChain** for orchestration  
- **ChromaDB** for vector storage  
- **PDF ingestion + chunking** for context retrieval  

The project is structured as a clear, educational walkthrough — ideal for learning, teaching, or adapting into production.

---

## 🧱 Architecture

```
PDFs → Chunking → Embeddings → Vector DB (Chroma) → Retriever → Gemini → Final Answer
```

**Core components:**

- **Gemini API** — LLM for grounded generation  
- **LangChain** — pipeline and retrieval orchestration  
- **ChromaDB** — persistent vector store  
- **tiktoken** — token‑aware chunking  
- **pypdf** — PDF parsing  

---

## 📂 Repository Structure

```
RAG/
│
├── 0 README.md
├── 0 Table of Contents.md
├── 1 Introduction.md
├── 2 Installing and Importing the Necessary Libraries.md
├── 3 Setting up the Gemini API key (Colab Secrets).md
├── 4. Setting up the Gemini client.md
│
├── 5. RAG System_5.1. Problem Statement.md
├── 5. RAG System_5.2 Load PDFs and Chunking.md
├── 5. RAG System_5.3 Create Vector Database & Embedding.md
├── 5. RAG System_5.4 Build Retriever.md
│
├── 6. Conclusion.md
│
└── assets/
      ├── Import Gemini API Key step 1.png
      ├── Import Gemini API Key step 2.png
      └── ...
```

Each file corresponds to a specific stage of the RAG pipeline.

---

## 🛠️ Installation

Install all required libraries:

```bash
pip install -q \
  openai==1.66.3 \
  tqdm==4.67.0 \
  tiktoken==0.9.0 \
  pypdf==5.4.0 \
  langchain==0.3.20 \
  langchain-community==0.3.19 \
  langchain-chroma==0.2.2 \
  langchain-openai==0.3.9 \
  chromadb==0.6.3
```

---

## 🔑 Setting Up the Gemini API Key

See:

```
3 Setting up the Gemini API key (Colab Secrets).md
```

This section includes screenshots showing:

- How to open Colab Secrets  
- How to import a Gemini API key  
- How to create a new key in Google AI Studio  
- How to store it as `GEMINI_API_KEY`  

---

## 🤖 Initializing the Gemini Client

Covered in:

```
4. Setting up the Gemini client.md
```

You’ll:

- How to load the API key  
- How to initialize the Gemini client  
- How to test your first request  

---

## 📄 Loading PDFs & Chunking

Covered in:

```
5. RAG System_5.2 Load PDFs and Chunking.md
```

Includes:

- PDF extraction  
- Token‑aware chunking  
- Overlap strategies  
- Chunk preview examples  

---

## 🧬 Creating the Vector Database

Covered in:

```
5. RAG System_5.3 Create Vector Database & Embedding.md
```

You’ll:

- How to initialize Chroma  
- How to embed chunks  
- How to persist the vector store  

---

## 🔍 Building the Retriever

Covered in:

```
5. RAG System_5.4 Build Retriever & LLM Answering.md
```

This section explains:

- Query embedding  
- Top‑K retrieval  
- Returning source documents  
- Integrating with Gemini for grounded answers  

---

## 🧪 Example Query

```python
query = "What is the company’s parental leave policy?"
response = answer_question(query)
print(response)
```

**Example Output:**

```
The company provides 12 weeks of paid parental leave...
```

---

## 🏁 Conclusion

See:

```
6. Conclusion.md
```

This summarizes:

- What the RAG system accomplishes  
- How the pipeline works end‑to‑end  
- Next steps for scaling and deployment  

---
