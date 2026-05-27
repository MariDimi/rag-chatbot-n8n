# rag-chatbot-n8n

This folder contains workflow exports from n8n v2.0.2 in JSON format.
> Note: Triggers are missing in most workflows. You will need to add them manually after importing.

# Requirements
Before using these workflows, make sure you have the following set up:

- Google Drive — Your PDF files should be stored in a Google Drive folder
- Ollama (local) — The workflows use local Ollama models by default. The LLM component can be swapped for any other model you have an API key for
- Supabase account — Free tier is sufficient → supabase.com
- Cohere account — Free tier is sufficient → cohere.com

# Workflows
## Agent
The main agent for the default RAG system. Includes a toggle between Supabase and Pinecone as the vector store.
## Multi-Agent
A multi-agent workflow designed for metadata filtering.
## RAG DB — Create / Update / Delete
Three workflows for managing the RAG database:

- Create — builds the main vector database
- Update — adds new content with versioning
- Delete — removes outdated files

## Summary DB
One workflow that generates summaries of documents and stores them in a secondary database. Works as a complement to the main database and is required for the multi-agent system.
## Evaluation
One workflow for evaluating the system using RAGAS metrics.

# How to Import

1. Open n8n
2. Go to Workflows → Import
3. Select the desired .json file
4. Add your trigger manually after importing
