# QA System with Google Gemini and LlamaIndex

This project is a Question Answering (QA) system that leverages Google Gemini LLM and document embeddings using [llama-index](https://github.com/jerryjliu/llama_index). It enables semantic search and question answering over your own documents, with an interactive Jupyter notebook and a Streamlit app for experimentation.

---

## Features

- **Document Ingestion:** Load and process documents from a directory.
- **Embeddings:** Use Gemini embeddings for semantic understanding.
- **LLM Integration:** Query Google Gemini LLM for answers.
- **Indexing:** Build a vector store index for efficient retrieval.
- **Interactive Notebook:** Step-by-step code in `notebooks/expriments.ipynb`.
- **Streamlit App:** User-friendly interface for QA (see `notebooks/StreamlitApp.py`).

---

## Project Structure

```
qasystem/
│
├── Data/                      # Place your PDF or text documents here
├── QAWithPDF/                 # Core modules (if any)
├── notebooks/
│   ├── expriments.ipynb       # Main Jupyter notebook
│   └── StreamlitApp.py        # Streamlit app for QA
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation
```

---

## Setup

1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/qasystem.git
    cd qasystem
    ```

2. **Install dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

3. **Set up your Google API key:**
    - Create a `.env` file in the root directory.
    - Add your key:
      ```
      GOOGLE_API_KEY=your_google_api_key_here
      ```

---

## Usage

### Jupyter Notebook

1. Place your documents (PDFs, text files) in the `Data/` directory.
2. Open `notebooks/expriments.ipynb` in Jupyter.
3. Run the cells to:
    - Load your API key and dependencies.
    - List available Gemini models.
    - Load and preview your documents.
    - Initialize Gemini LLM and embedding models.
    - Build the vector index.
    - Query the index with natural language questions.

### Streamlit App

To run the Streamlit app for a web-based interface:
```sh
streamlit run notebooks/StreamlitApp.py
```

---

## Example Workflow (Notebook)

- **Load API Key:**  
  Uses `dotenv` to securely load your Google API key.
- **List Gemini Models:**  
  See which Gemini models are available for use.
- **Document Loading:**  
  Reads all files from the `Data/` directory.
- **Embedding & Indexing:**  
  Embeds documents and builds a vector index.
- **Querying:**  
  Ask questions like `"What is X?"` and get answers from your documents.

---

## Requirements

See `requirements.txt` for all dependencies, including:
- llama-index
- google-generativeai
- llama-index-llms-gemini
- pypdf
- python-dotenv
- IPython
- streamlit

---

**Author:** Aditya Sethi
