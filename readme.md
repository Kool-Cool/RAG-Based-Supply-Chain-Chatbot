# Supply Chain Chatbot using Flowise

This project implements a Retrieval-Augmented Generation (RAG) chatbot using Flowise to answer questions about a supplier network. The chatbot uses structured and unstructured supply chain data and delivers context-aware responses through a web interface.

## Project Overview

The objective of this project is to build a chatbot capable of answering questions related to suppliers, products, supply chain relationships, and supporting documents using Retrieval-Augmented Generation (RAG).

The chatbot is developed using Flowise and embedded into a simple HTML webpage. Users can interact with the chatbot through the web interface, and responses are generated using relevant information retrieved from multiple data sources.

## Architecture

The system uses a multi-source RAG pipeline:

- CSV data is stored and queried using PostgreSQL
- PDF documents are processed using text retrieval techniques
- Vector embeddings are generated using Hugging Face embedding models
- Pinecone is used as the vector database for semantic search and retrieval
- Flowise orchestrates the full RAG workflow
- Grok AI is used as the LLM for final response generation

The overall architecture is shown below:

```
static/flow.png
```

## Features

- Retrieval-Augmented Generation (RAG) pipeline
- Flowise-powered conversational interface
- PostgreSQL-based structured data retrieval (CSV)
- PDF text retrieval for unstructured documents
- Pinecone vector database for semantic search
- Hugging Face embeddings for vector generation
- Context-aware supply chain question answering
- Web-based chatbot interface
- Public deployment support

## Technologies Used

- Flowise AI
- Grok AI
- PostgreSQL
- Pinecone
- Hugging Face Embeddings
- Retrieval-Augmented Generation (RAG)
- Document Text Retrieval
- HTML
- CSS
- JavaScript

## Data Sources

### Structured Data
CSV datasets are stored in PostgreSQL and used for querying supplier and supply chain information.

### Unstructured Data
PDF documents are processed and indexed for text retrieval to support document-based question answering.

## Project Structure

```text
.
├── index.html
├── static/
│   └── flow.png
└── README.md
```

## System Workflow

1. User submits a question through the chatbot UI.
2. Flowise receives and processes the query.
3. Relevant structured data is retrieved from PostgreSQL (CSV-based queries).
4. Relevant text is retrieved from PDF documents.
5. Embeddings are generated using Hugging Face models.
6. Vector search is performed using Pinecone.
7. Retrieved context is passed to Grok AI.
8. Grok AI generates a final response.
9. The response is returned to the user via the chatbot interface.

## Implementation

The chatbot is embedded into the webpage using Flowise Embed SDK.

```javascript
Chatbot.initFull({
    chatflowid: "30db7cce-16e8-4ed1-b555-01796c687693",
    apiHost: "https://cloud.flowiseai.com",
})
```

## Deployment

The project is deployed as a static website and can be hosted on:

- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

## Author

**Name:** Kool-Cool  
**GitHub:** https://github.com/Kool-Cool  
**Email:** 22f2001265@ds.study.iitm.ac.in  

