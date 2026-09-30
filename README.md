# AI Research Paper Assistant

An NLP-based research paper assistant that uses sentence embeddings and FAISS similarity search to retrieve relevant information from research papers.

## Project Overview

This project demonstrates a retrieval-based approach for interacting with research papers. A PDF research paper is converted into text, cleaned, divided into sentence-based chunks, transformed into vector embeddings, and indexed using FAISS.

When a user asks a question, the system converts the question into an embedding and retrieves the most semantically relevant passages from the paper.

The project implements the **retrieval component of a Retrieval-Augmented Generation (RAG) system**.

## Technologies Used

* Python
* Sentence Transformers
* FAISS
* NumPy
* PyPDF
* Google Colab

## Pipeline

**PDF → Text Extraction → Text Cleaning → Sentence Chunking → Embeddings → FAISS Index → Semantic Retrieval**

## How It Works

1. A research paper is loaded from a PDF.
2. The text is extracted and cleaned.
3. The paper is divided into manageable sentence-based chunks.
4. Each chunk is converted into a numerical embedding using Sentence Transformers.
5. FAISS indexes the embeddings for efficient similarity search.
6. A user's question is also converted into an embedding.
7. The system retrieves the most semantically relevant passages from the paper.
8. The retrieved passages are displayed as evidence for the user.

## Paper Used

**A Survey of Large Language Models**

Wayne Xin Zhao et al.

## Example

The assistant can be asked:

> What special abilities do large language models exhibit?

The system retrieves relevant passages discussing topics such as instruction following, reasoning, task-solving capabilities, and emergent abilities.

## Project Objective

The goal of this project is to demonstrate how semantic search can be used to retrieve relevant evidence from a research paper.

Instead of relying only on keyword matching, the system uses sentence embeddings to capture the semantic meaning of the question and the paper's content.

This project provides a foundation for a more complete RAG system, where a language model could later use the retrieved evidence to generate a natural-language answer.
