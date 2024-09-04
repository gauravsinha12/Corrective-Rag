# Corrective RAG (Retrieval-Augmented Generation) Pipeline

This project implements a Corrective Retrieval-Augmented Generation (RAG) pipeline using the `langchain` framework. The pipeline retrieves relevant documents based on a user's query, grades their relevance, possibly rephrases the query, and generates a final response using a large language model (LLM). If the retrieved documents are not relevant, corrective actions such as query transformation or web search are performed before generating the final answer.

## Features

- **Document Retrieval:** Load documents from a URL and split them into manageable chunks.
- **Vector Store:** Store the split documents in a vector store and retrieve relevant documents based on query embeddings.
- **Relevance Grading:** Assess the relevance of retrieved documents to the query using a prompt template and LLM.
- **Query Rewriting:** Rephrase the query if retrieved documents are not relevant.
- **Web Search:** Perform a web search if the rephrased query still doesn't yield relevant documents.
- **StateGraph Workflow:** A structured workflow with conditional branching based on the relevance of retrieved documents.

## Installation

To install the necessary packages, run the following command:

```bash
pip install langchain-community langchain-openai tiktoken langchainhub chromadb langchain langgraph tavily-python gpt4all python-dotenv beautifulsoup4 unstructured[all-docs] pypdf
  
