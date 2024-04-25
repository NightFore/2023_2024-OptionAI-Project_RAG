# RAG System Using Llama2 With Hugging Face and Gradio

This project utilizes Llama2 (Llama-2-7b-chat-hf) with Hugging Face to implement a Retrieval-Augmented Generation (RAG) system within the Google Colab environment. It employs a virtual environment and Google Drive to store essential packages. Additionally, the application is deployed on Gradio to provide a user-friendly interface for interacting with the RAG system and facilitating easy sharing.

## Setup

The setup section covers the following aspects:

- Constants and Configuration: Defines project-specific constants such as project name, virtual environment directory, necessary packages to install, data directory, model name, tokenizer name, and embedding model name.
- Mount Google Drive: Functions to mount Google Drive if not already mounted.
- Retrieve Project Folder Path: Retrieves the path to the project folder based on the provided project name and base folder location.
- Setting Up Virtual Environment: Initializes a virtual environment for the project to store installed packages.
- Install Packages: Installs necessary packages into the virtual environment.
- Library Imports: Imports required libraries and sets up the environment for the RAG system.

## Initializing the Q&A Assistant

This section establishes the necessary prompts and initializes the Hugging Face LLM to create an interactive Q&A assistant. It includes:

- System Prompt and Query Wrapper: Definition of the system prompt and query wrapper prompt for the Q&A assistant.
- Initializing the Hugging Face LLM: Initialization of the HuggingFaceLLM model for language generation.
- Example Interaction with the Assistant: Demonstration of the assistant's functionality by interacting with it.

## Setting Up the Information Retrieval System

Before utilizing the information retrieval system, several components need to be set up and initialized, including:

- Initializing HuggingFace Embeddings: Initialization of the HuggingFaceEmbeddings model for embedding documents.
- Creating Service Context: Creation of a service context for indexing and querying.
- Loading and Creating Index: Loading documents from a directory and creating a vector store index.
- Converting Index to Query Engine: Conversion of the index into a query engine for performing queries.

## Gradio Interface

With everything set up, an interface is deployed using Gradio to interact with the RAG system in a more user-friendly manner. Users can ask questions and receive responses from the RAG system via the interface.

## Usage

To use this notebook:

1. **Set up the project**: Define the directory name of the project in the constants (`PROJECT_NAME`). Ensure that the required documents are placed in a folder defined as `DATA_DIRECTORY` before launching the script.
2. **Mount Google Drive**: Grant necessary permissions for Google Drive access.
3. **Initialize the virtual environment**: This step downloads all required packages to the Google Colab environment inside the folder defined by `ENV_DIRECTORY`.
4. **Install necessary packages**: Install the required packages for the project.
5. **Initialize the Q&A assistant**: Interact with the assistant to verify its functionality.
6. **Set up the information retrieval system**: Perform document indexing and querying.
7. **Deploy the Gradio interface**: Launch the interface to interact with the RAG system.

Note 1: Ensure that necessary permissions for Google Drive access are granted and that the Hugging Face token is provided. Optionally, you can add the `HF_TOKEN` as a secret key on Google Colab to avoid manual login on Hugging Face when prompted.

Note 2: This script was only tested with PDF documents.

## License

This project is licensed under the terms of the MIT License. See the [LICENSE](LICENSE) file for details.