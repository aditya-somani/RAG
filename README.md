# RAG Implementation with LangGraph

A comprehensive Retrieval-Augmented Generation (RAG) system built with LangGraph, LangChain, and ChromaDB. This project demonstrates how to build an end-to-end RAG pipeline for querying documents using Large Language Models.

## Features

- **Document Processing**: Load and process PDF documents
- **Intelligent Chunking**: Split documents while preserving context
- **Vector Storage**: Store embeddings in ChromaDB for fast retrieval
- **Semantic Search**: Retrieve relevant context using similarity search
- **LLM Integration**: Generate accurate answers using Google's Gemini model
- **LangGraph Workflow**: Orchestrate the entire RAG pipeline with state management

## Prerequisites

- Python 3.11 or higher
- [UV](https://github.com/astral-sh/uv) package manager (Simply run - `pip install uv` in terminal)
- Google API key for Gemini (set in environment variables) - Get it from [Google AI Studio](https://aistudio.google.com/)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/aditya-somani/RAG.git
   cd RAG
   ```

2. **Install dependencies using UV**
   ```bash
   uv sync
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory from `.env.example`:
   ```bash
   cp .env.example .env
   ```
   Then edit `.env` and add your Google API key.

## Usage

### Running the Jupyter Notebook

1. **Start Jupyter Notebook**
   ```bash
   uv run jupyter notebook
   ```

2. **Open `rag.ipynb`** and follow the cells sequentially:
   - Initialize ChromaDB and embeddings
   - Load and process your PDF documents
   - Store embeddings in ChromaDB
   - Query the RAG system

### Quick Query (After Initial Setup)

Once documents are stored in ChromaDB, use the direct query function:

```python
from rag.ipynb import query_rag_direct

answer = query_rag_direct("Your question here")
```

## Project Structure

```
RAG/
├── rag.ipynb              # Main Jupyter notebook with RAG pipeline
├── pyproject.toml         # Project dependencies and configuration
├── uv.lock                # Locked dependency versions
├── chroma_db/             # ChromaDB vector database (auto-generated)
└── README.md              # This file
```

## Technologies Used

- **LangGraph**: Workflow orchestration and state management
- **LangChain**: LLM framework and document processing
- **ChromaDB**: Vector database for embedding storage
- **Google Gemini**: Large Language Model for answer generation
- **UV**: Fast Python package manager

## Author

**Aditya Somani**

- LinkedIn: [Aditya Somani](https://www.linkedin.com/in/aditya-somani-03631727b/)
- Email: [Mail](adityasomani456@gmail.com)

## License

This project is open source and available for educational purposes.

