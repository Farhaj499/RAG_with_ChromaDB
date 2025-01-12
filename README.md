# Extractive Question Answering with ChromaDB, and Gemini

This project implements an Extractive Question Answering (EQA) system that extracts answers from a set of downloaded text files based on user queries. It utilizes ChromaDB as a vector database to store document embeddings for efficient retrieval of relevant information. Gemini is then used to refine the extracted information, providing more relevant, concise, and human-like responses.

## Overview

The project follows these steps:

1.  **Data Download:** The script downloads the compressed archive "new_articles.zip" from Dropbox using the provided link.
2.  **Text Extraction:** The downloaded archive is unzipped, and all text files within are extracted.
3.  **Text Preprocessing:** Each text file is preprocessed to clean and normalize the text content (optional).
4.  **Embedding Generation:** Embeddings are created for each preprocessed text document using a chosen embedding model (e.g., Sentence Transformers).
5.  **Data Storage in ChromaDB:** Text documents and their corresponding embeddings are stored in ChromaDB.
6.  **Retrieval:** When a user asks a question, the system generates an embedding for the query and retrieves the most similar documents from ChromaDB using cosine similarity.
7.  **Response Refinement with Gemini:** The retrieved text snippets are passed to the Gemini LLM, which refines the information to provide a more relevant, concise, and human-like response to the user's query.

## Technologies Used

*   ChromaDB: Vector database for storing and retrieving embeddings.
*   Hugging Face Transformers (optional): For generating document embeddings.
*   LangChain (optional): For streamlining document preprocessing and loading.
*   Python: Programming language for implementation.
*   Requests: To download the data from Dropbox.
*   File manipulation libraries (e.g., os, zipfile): For handling file downloads and extraction.
*   Gemini: Large Language Model for refining extracted information and generating human-like responses.
