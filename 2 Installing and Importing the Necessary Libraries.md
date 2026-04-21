# **2. Installing and Importing the Necessary Libraries**


```python
# Installing the necessary libraries with specified versions
!pip install -q openai==1.66.3 \
                tqdm==4.67.0 \
                tiktoken==0.9.0 \
                pypdf==5.4.0 \
                langchain==0.3.20 \
                langchain-community==0.3.19 \
                langchain-chroma==0.2.2 \
                langchain-openai==0.3.9 \
                chromadb==0.6.3
```

These library packages together form a modern Retrieval‑Augmented Generation (RAG) stack for reading PDFs, chunking text, embedding it, storing it in a vector database, and querying it with OpenAI models.

**Note:**
- After running the above cell, restart the runtime (for Google Colab) or notebook kernel (for Jupyter Notebook), and run all cells sequentially from the next cell.
- On executing the above line of code, a warning regarding package dependencies might appear. This error message can be ignored as the above code ensures that all necessary libraries and their dependencies are maintained to successfully execute the code in this notebook.

```python
# Importing the necessary libraries
# Mandatory: Run this AFTER restarting the runtime following the installation step.

import os                   # File paths, environment variables
import json                 # JSON handling
import time                 # Timing utilities
from datetime import datetime

import numpy as np          # Numerical operations (used in RAG similarity search)
import pandas as pd         # DataFrame loading and manipulation
from tqdm import tqdm       # Progress bars for iteration and apply()

# OpenAI-compatible client (used to call Gemini models via Generative Language API)
from openai import OpenAI

# Tokenizer utilities (for token-aware chunking)
import tiktoken

# PDF parsing (extract text from HR policy PDFs)
import pypdf

# LangChain utilities for text splitting and PDF loading
from langchain.text_splitter import RecursiveCharacterTextSplitter
from langchain_community.document_loaders import PyPDFDirectoryLoader

# LangChain document structure (stores text chunks + metadata)
from langchain_core.documents import Document

# LangChain/OpenAI embedding wrapper
from langchain_openai import OpenAIEmbeddings

# Chroma integration via LangChain
from langchain_chroma import Chroma

# ChromaDB vector database (stores embeddings for retrieval)
import chromadb

# Reduce excessive Chroma logs
import logging
logging.getLogger("chromadb").setLevel(logging.CRITICAL)

print("All libraries imported successfully.")
```

```markdown
All libraries imported successfully.
