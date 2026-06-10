# Supply Chain Chatbot using Flowise

This project implements a Retrieval-Augmented Generation (RAG) chatbot using Flowise to answer questions about a supplier network. The chatbot uses the provided datasets and documents as its knowledge base and delivers context-aware responses through a web interface.

## Project Overview

The objective of this project is to build a chatbot capable of answering questions related to suppliers, products, supply chain relationships, and supporting documentation using Retrieval-Augmented Generation (RAG).

The chatbot is developed using Flowise and embedded into a simple HTML webpage. Users can interact with the chatbot through the web interface, and responses are generated using relevant information retrieved from structured and unstructured data sources.

## Architecture

The solution combines multiple data sources:

- CSV datasets are stored and queried using PostgreSQL.
- PDF documents are processed using text retrieval techniques.
- Flowise orchestrates the retrieval and generation workflow.
- Grok AI is used as the Large Language Model (LLM) for response generation.

## Features

- Retrieval-Augmented Generation (RAG) architecture
- Flowise-powered conversational interface
- PostgreSQL-based retrieval for structured CSV data
- Text retrieval from PDF documents
- Context-aware question answering
- Supply chain and supplier network analysis
- Publicly accessible deployment
- Responsive web-based frontend

## Technologies Used

- Flowise AI
- Grok AI
- PostgreSQL
- Retrieval-Augmented Generation (RAG)
- Document Retrieval
- HTML
- CSS
- JavaScript

## Data Sources

### Structured Data

CSV datasets containing supplier and supply chain information are stored in PostgreSQL and queried during retrieval.

### Unstructured Data

PDF documents are processed and indexed for text retrieval, allowing the chatbot to answer questions based on document content.

## Project Structure

```text
.
├── index.html
└── README.md
```

## Implementation

The chatbot is hosted through Flowise Cloud and embedded into the webpage using the Flowise Embed SDK.

```javascript
Chatbot.initFull({
    chatflowid: "30db7cce-16e8-4ed1-b555-01796c687693",
    apiHost: "https://cloud.flowiseai.com",
})
```

### Workflow

1. User submits a question through the chatbot interface.
2. Flowise determines the appropriate retrieval source.
3. Relevant records are retrieved from PostgreSQL for CSV-based queries.
4. Relevant passages are retrieved from indexed PDF documents using text retrieval.
5. Retrieved context is sent to Grok AI.
6. Grok AI generates a context-aware response.
7. The response is displayed to the user.

## Deployment

The application is deployed as a static website and can be accessed through a public URL.

The frontend consists of a single HTML page that embeds the Flowise chatbot, making it suitable for deployment on platforms such as GitHub Pages, Netlify, or Vercel.

## Author

**Name:** ASNS

**GitHub:** https://github.com/Kool-Cool

**Email:** 22f2001265@ds.study.iitm.ac.in

## License

This project was developed for educational and academic purposes.