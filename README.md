## **► Mini RAG System Project**
---
<p align="center">
  <img src="https://conversed.ai/wp-content/uploads/2025/04/RAG-Conversed.ai_.jpg" alt="RAG System Diagram" width="600"/>
</p>
---

### ► Project Overview

This project implements a foundational Retrieval-Augmented Generation (RAG) system using Python and components from Hugging Face Transformers. It demonstrates how to combine information retrieval with question answering to provide more accurate and contextually relevant responses.
---
### ► Core Components

#### 1. Retriever
-   **Model:** `sentence-transformers/all-MiniLM-L6-v2` (for generating embeddings)
-   **Functionality:** Responsible for indexing a `knowledge_base` (a collection of sentences) and, given a user query, efficiently identifying and retrieving the most semantically relevant document(s) from that base. This is achieved by comparing the query's embedding with the embeddings of the knowledge base documents using cosine similarity.

#### 2. Generator
-   **Model:** `distilbert-base-cased-distilled-squad` (a question-answering model)
-   **Functionality:** Takes a user's question and the context provided by the retriever. Its role is to accurately extract the most probable answer span directly from the retrieved context, enhancing the relevance and specificity of the response.
---
### ► How It Works

The RAG system operates in a two-step process:

1.  **✦ Retrieval:** When a question is posed, the retriever first searches a pre-indexed `knowledge_base` to find the most relevant pieces of information.
2.  **✦ Generation:** These retrieved snippets of information (context) are then fed into the generator model along with the original question. The generator uses this context to formulate a precise answer.
---
###  ► Tasks Completed

This project includes a series of tasks designed to build, test, and expand the RAG system:

-   **✦ Task 1: Execute and Understand**
    -   Ran the initial RAG assessment and verified its perfect score (6/6).
    -   Analyzed the retrieval and generation steps for each question, confirming correct functionality.
-   **✦ Task 2: Add a New Question**
    -   Extended the assessment with an additional question about existing knowledge (e.g., "How long is the Great Wall of China?").
    -   Ensured the system correctly retrieved the relevant context and generated the accurate answer, achieving an 8/8 score.
-   **✦ Task 3: Add New Knowledge & Test It**
    -   Expanded the system's `knowledge_base` with a new fact (e.g., "The deepest part of the world's oceans is the Mariana Trench...").
    -   Re-encoded the updated knowledge base to ensure the retriever was aware of the new information.
    -   Added a new test question specifically targeting this added knowledge, confirming the system's ability to learn and answer based on new facts, achieving a 2/2 score for this specific task.
---
###  ► Project Structure

-   `mini_rag_system_homework.ipynb`: The main Jupyter Notebook containing all the Python code, explanations, and completed tasks for setting up, evaluating, and extending the RAG system.
---
###  ► Getting Started

To run this project:

1.  Clone this repository: `git clone https://github.com/Salma-Talat-Shaheen/mini-rag-system-project/blob/main/Model_3_Section_1_Homework.ipynb`
2.  Open the `Model_3_Section_1_Homework.ipynb` file in Google Colab or a local Jupyter environment.
3.  Execute the cells sequentially to build, test, and interact with the RAG system.

---
