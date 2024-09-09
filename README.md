# AI Chatbot for a Large Hospital System

This **Graph RAG Hospital chatbot** is designed to provide quick answers to various questions about a large hospital system, following questions are listed below:

- What is the current wait time at XYZ hospital?
- Which hospital has the shortest wait time right now?
- At which hospitals are patients reporting issues with billing and insurance?
- Have there been any complaints about cleanliness at the hospitals?
- What feedback have patients given about the communication of doctors and nurses?
- What are patients saying about the nursing staff at XYZ hospital?
- How many visits are currently open and what is their average duration in days?
- Which physician has the shortest average visit duration in days?
- How much was billed for patient 789’s stay?
- Which hospital treated the most Cigna patients in 2023?
- What is the average billing amount for emergency visits by hospital?

This chatbot utilizes **Large Language Models (LLM)**, **Retrieval-Augmented Generation (RAG)** techniques, and **Graph Database (Neo4j)**, drawing on various data sources to answer these questions.

# Project Design

This project features a versatile chatbot capable of intelligently selecting the appropriate tools to deliver accurate and relevant responses. The chatbot uses a combination of techniques to interact with external APIs, query graph databases, and perform semantic searches within a vector database.

## Features

- **Agent-Based Tool Selection**: The chatbot employs an LLM agent to decide the best tool to use for each query.
- **Function Calling with External APIs**: It can call external APIs to fetch the necessary data.
- **Cypher Query Generation**: It generates Cypher query languages to extract information from a graph database using LLMs.
- **RAG Technology for Semantic Search**: It uses Retrieval-Augmented Generation (RAG) technology to perform semantic searches within the vector database.
- **LLM for Response Generation**: It utilizes OpenAI LLMs to generate appropriate and coherent responses based on the retrieved information.

## How It Works

1. **Agent-Based Decision Making**: The chatbot's agent evaluates the user's query and determines the most suitable tool to use.
2. **Retrieval**: This chatbot can retrieve relavant information from both structured and unstructured text sources.<br>
   2.1. **Structured**: When a semantic search is needed, the agent uses OpenAI embedding models to search within the vector database and retrieve the most relevant information.<br>
   2.2. **Unstructured**: For queries that can be answered using the graph database, the agent will generate and execute Cypher queries.<br>
3. **External API Calls**: If the query requires data from an external source, the agent will call the relevant API and fetch the data.
4. **RAG**: When semantic search or API calling is finished, the agent uses RAG technology to feed the relevant retrieved information and user question into LLM. 
5. **Response Generation**: The chatbot then uses the LLM to generate a well-formed response based on retrieved information and user question.


## Installation

To run this project, follow these steps:

1. **Clone the repository**:
    ```sh
    git clone https://github.com/javaidiqbal11/Graph-RAG-Hospital-Chatbot.git
    ```

2. **Navigate to the project directory**:
    ```sh
    cd Graph-RAG-Hospital-Chatbot
    ```

3. **Set up a virtual environment**:
    ```sh
    python -m venv env
    source env/bin/activate  
    ```

4. **Install dependencies**:
    ```sh
    pip install -r requirements.txt
    ```
