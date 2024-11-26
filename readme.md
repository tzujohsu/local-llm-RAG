## Retreival Augmented Generation (RAG) with Ollama

This project sets up a local LLM to perform Retreival Augmented Generation, enabling multi-round question-answering based on provided PDFs or .md files. Simply put, this chatbot can memorize previous conversations and answer your questions referencing the given files.

This repo is based on [local-LLM-with-RAG](https://github.com/amscotti/local-LLM-with-RAG?tab=readme-ov-file) by amscotti.

### Features
* Langchain: provides a standard interface for working with vector stores.
* Ollama: A streamlined tool to run open-source LLMs locally
* Streamlit UI: A simple, user-friendly interface to run the chatbot via Streamlit.
* Chroma: A vector database for storing and retrieving embeddings
* PyPDF: A Python library for reading and manipulating PDF files.

### Setup
1. Download [Ollama]() verson 0.1.26 or higher.
2. Clone this repository to your local environment.
3. Create a Python virtual environment: `python3 -m venv .venv`.
4. Activate the virtual environment: `source .venv/bin/activate` on Unix or MacOS, or `.\.venv\Scripts\activate` on Windows.
5. Install necessary packages: `pip install -r requirements.txt`
6. Run `python app.py` to start the program in your terminal, with optional arguments: `-m <model_name> -p <path_to_documents> -e <embedding_model_name>`
7. [Optional] Run `streamlit run ui.py` to start a web UI.



#### Note
* The default setting:
  * The path for reference files: **Document**
  * The embedding model: `nomic-embed-text`.
  * The LLM model: `mistral`.
* The model name list can be found on the [ollama page](https://github.com/ollama/ollama). Note that generally, 7B models can run with 8G RAM, 13B models require 16G RAM.
