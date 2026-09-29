# AI Research Paper Assistant

An AI-powered research paper assistant that uses **Natural Language Processing (NLP), sentence embeddings, and vector similarity search** to retrieve relevant information from research papers.

## Project Overview

Reading long research papers can be time-consuming. This project demonstrates a simple **Retrieval-Augmented Generation (RAG)** workflow that allows users to ask questions about a research paper and retrieve the most relevant passages from it.

The project uses the paper **"A Survey of Large Language Models"** by Wayne Xin Zhao et al. as the source document.

## How It Works

The system follows this pipeline:

**Research Paper PDF → Text Extraction → Text Cleaning → Sentence Chunking → Embeddings → FAISS Vector Search → Relevant Evidence**

### 1. PDF Text Extraction

The research paper is loaded and its text is extracted using `pypdf`.

### 2. Text Cleaning

The reference section is removed to reduce irrelevant retrieval results.

### 3. Sentence Chunking

The extracted text is divided into smaller sentence-based chunks to make semantic retrieval more effective.

### 4. Embeddings

Each text chunk is converted into a numerical vector using the **Sentence Transformers** model:

`all-MiniLM-L6-v2`

### 5. Vector Search

The embeddings are stored in a **FAISS** index, allowing the system to find passages that are semantically similar to a user's question.

### 6. Question Retrieval

When a user asks a question, the question is also converted into an embedding. FAISS then retrieves the most relevant passages from the research paper.

## Technologies Used

* Python
* Google Colab
* PyPDF
* Sentence Transformers
* FAISS
* NumPy
* Pandas
* Hugging Face Transformers

## Example

**Question:**

> What special abilities do large language models exhibit?

The system retrieves relevant passages discussing capabilities such as:

* Instruction following
* Step-by-step reasoning
* Complex task solving
* In-context learning
* Improved generalization

## Project Results

The final system successfully:

* Extracts text from a 144-page research paper
* Removes the reference section
* Creates 350 semantic text chunks
* Generates 384-dimensional embeddings
* Stores the embeddings in a FAISS vector index
* Retrieves relevant evidence for natural-language questions

## Notebook

The complete implementation is available in:

`AI_Research_Paper_Assistant.ipynb`

## Future Improvements

Possible improvements include:

* Better PDF layout and table extraction
* Improved chunking based on document sections
* Source/page citations for retrieved passages
* A stronger instruction-tuned language model
* A web interface using Streamlit or Gradio
* Support for multiple research papers
* Automatic answer generation using retrieved evidence

## Learning Objective

This project demonstrates the fundamental components of a **Retrieval-Augmented Generation (RAG)** system and provides practical experience with document processing, embeddings, semantic search, and vector databases.
