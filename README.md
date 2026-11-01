# memory-enabled-chatbot-vector-embeddings
AI-powered chatbot using Qwen, Sentence Transformers, and ChromaDB to generate context-aware responses through vector embeddings, semantic search, and persistent conversational memory.
# Simple Chatbot Using Vector Embeddings

## Project Overview

This project implements a simple AI-powered chatbot with a memory mechanism. It uses vector embeddings to store and retrieve previous conversations, allowing the chatbot to provide context-aware responses based on relevant information from past interactions.

The chatbot uses a Qwen language model for response generation, Sentence Transformers for creating text embeddings, and ChromaDB as a persistent vector database for storing conversational memories.

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Qwen 2.5 (0.5B Instruct)
- Sentence Transformers
- ChromaDB
- Google Colab / Jupyter Notebook

## Key Features

- Generates conversational responses using a pretrained language model.
- Converts text into numerical vector embeddings.
- Stores user queries and assistant responses in ChromaDB.
- Retrieves relevant memories using semantic similarity search.
- Maintains conversation history with user and conversation identifiers.
- Supports persistent storage of conversational memory.
- Allows users to search and inspect previously stored conversations.

## How It Works

1. **Embedding Generation:** Sentence Transformers converts text into vector representations using the `all-MiniLM-L6-v2` model.
2. **Memory Storage:** ChromaDB stores conversation data, embeddings, timestamps, and metadata.
3. **Semantic Search:** User queries are converted into embeddings to retrieve relevant previous conversations.
4. **Context Building:** Retrieved memories are added to the prompt to provide additional context.
5. **Response Generation:** The Qwen language model generates a response based on the current query and retrieved context.
6. **Memory Persistence:** Both user queries and assistant responses are stored for future retrieval.

## Models Used

| Component | Model |
|---|---|
| Chat generation | Qwen/Qwen2.5-0.5B-Instruct |
| Text embeddings | all-MiniLM-L6-v2 |
| Vector database | ChromaDB |

## Installation

Install the required dependencies:

```bash
pip install chromadb sentence-transformers transformers accelerate einops torch
```

## Execution

1. Open the Jupyter Notebook in Google Colab or a local Python environment.
2. Install the required dependencies.
3. Load the embedding and language models.
4. Initialize the ChromaDB persistent collection.
5. Run the chatbot and enter queries interactively.
6. Test memory retrieval and database persistence.

## Learning Outcomes

Through this project, I explored how vector embeddings and semantic search can be used to build conversational AI systems. I also gained practical exposure to pretrained language models, vector databases, conversational memory management, and context-aware response generation.

## Future Improvements

- Add a user-friendly chatbot interface.
- Improve memory retrieval and relevance filtering.
- Support document-based question answering.
- Explore larger language models for improved response generation.
