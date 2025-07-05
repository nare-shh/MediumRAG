# Medium RAG Project

A Retrieval-Augmented Generation (RAG) system that ingests Medium blog articles and enables question-answering using vector similarity search.

## Overview

This project demonstrates a basic RAG pipeline that:
1. Ingests text documents and splits them into chunks
2. Generates embeddings and stores them in a vector database
3. Retrieves relevant context for user queries
4. Uses a language model to generate answers based on retrieved context

## Technical Stack

- **Python 3.x**
- **LangChain** - Document processing and RAG chain orchestration
- **OpenAI API** - Embeddings generation and language model
- **Pinecone** - Vector database for storing and searching embeddings
- **python-dotenv** - Environment variable management

## Files

- `ingestion.py` - Loads documents, splits text, generates embeddings, and stores in Pinecone
- `main.py` - Retrieval and question-answering pipeline
- `mediumblog1.txt` - Sample Medium blog article about vector databases
- `readme.md` - Project documentation

## Setup

1. Install required dependencies:
```bash
pip install langchain langchain-community langchain-openai langchain-pinecone python-dotenv
```

2. Create a `.env` file with your API keys:
```
OPENAI_API_KEY=your_openai_api_key
INDEX_NAME=your_pinecone_index_name
```

3. Run ingestion to populate the vector database:
```bash
python ingestion.py
```

4. Run the main script to query the system:
```bash
python main.py
```

## Usage

The system is configured to answer questions about Pinecone and vector databases based on the ingested Medium article content.