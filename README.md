# Gen-AI-Literature-Review-Assistant# System / RAG Setup

## Overview

This component implements the Retrieval-Augmented Generation (RAG) system for the AI Literature Review Assistant.

The workflow is built in Dify (running locally via Docker) and connects user queries to an academic PDF knowledge base to generate grounded answers.

Architecture:

User Input → Knowledge Retrieval → LLM → Answer


## System Architecture

The workflow consists of four connected nodes:

1. User Input  
   Accepts a natural language question about the uploaded research paper.

2. Knowledge Retrieval  
   Retrieves relevant document chunks from the selected PDF in the Dify knowledge base.

3. LLM (Gemini 2.5 Flash – Free Tier)  
   Generates an answer using the retrieved context.

4. Answer Node  
   Returns the final response to the user.

Responses are grounded in the uploaded document.


## Model and Environment

- Platform: Dify (Docker local instance)
- LLM: Gemini 2.5 Flash (free tier)
- Retrieval: Dify Knowledge Base with uploaded academic PDF(s)

Note: Gemini free-tier rate limits may produce temporary quota errors.


## How to Reproduce / Import

1. Open Dify Studio.
2. Click "Import DSL".
3. Upload the exported workflow file located in this folder.
4. Add your own Gemini API key.
5. Upload PDF(s) into the Knowledge Base.
6. Connect the Knowledge Base to the Knowledge Retrieval node if needed.
7. Run Preview and test research-related questions.


## Scope of Responsibility

This folder covers the System / RAG Setup portion of the project.

Other components handled by team members:

- Prompt design
- Paper selection / knowledge base curation
- Slides and documentation


## Folder Contents

- Exported Dify workflow file (DSL/YAML)
- This README
