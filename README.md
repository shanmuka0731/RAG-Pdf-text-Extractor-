# 📄 RAG PDF Text Extractor & Assistant

An intelligent **Retrieval-Augmented Generation (RAG)** pipeline built inside a Jupyter Notebook that extracts text from PDF documents, converts it into semantic embeddings, stores it in a vector database, and leverages a local **Ollama LLM** to answer questions based on the document content.

This project enables private, efficient, and context-aware document question answering without relying on cloud-based AI services.

---

## 🚀 Features

### 📑 Advanced PDF Processing

* Extracts text from single-page and multi-page PDF documents.
* Preserves document structure for improved contextual understanding.
* Handles large PDF files efficiently.

### 🧠 Retrieval-Augmented Generation (RAG)

* Splits document content into manageable chunks.
* Generates semantic embeddings for each chunk.
* Retrieves the most relevant document sections before generating answers.

### 🤖 Local LLM Inference

* Uses **Ollama** for running Large Language Models locally.
* Ensures privacy and security by keeping data on your machine.
* Supports models like **Llama 3**, **Mistral**, and other Ollama-compatible models.

### 🔍 High-Quality Embeddings

* Powered by **BAAI/bge-large-en-v1.5** embeddings from Hugging Face.
* Produces highly accurate semantic search results.
* Improves retrieval quality and answer relevance.

### 💬 Context-Aware Question Answering

* Answers questions strictly based on document content.
* Reduces hallucinations through retrieval grounding.
* Provides accurate and relevant responses.

---

## 🛠️ Tech Stack

| Technology              | Purpose                       |
| ----------------------- | ----------------------------- |
| Python 3.13+            | Core Programming Language     |
| Jupyter Notebook        | Development Environment       |
| LangChain               | RAG Pipeline Framework        |
| Ollama                  | Local LLM Runtime             |
| Hugging Face Embeddings | Semantic Embedding Generation |
| FAISS / Vector Store    | Document Retrieval            |
| PyPDF                   | PDF Text Extraction           |

---

## 📂 Project Structure

```bash
RAG-Pdf-text-Extractor-
│
├── RAG_PDF_Text_Extractor.ipynb
├── sample.pdf
├── requirements.txt
├── README.md
└── assets/
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/shanmuka0731/RAG-Pdf-text-Extractor-.git

cd RAG-Pdf-text-Extractor-
```

---

### 2️⃣ Create Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

---

### 3️⃣ Install Dependencies

```bash
pip install langchain-core
pip install langchain-community
pip install langchain-huggingface
pip install langchain-text-splitters
pip install faiss-cpu
pip install pypdf
pip install sentence-transformers
pip install ollama
```

Or install everything at once:

```bash
pip install langchain-core langchain-community langchain-huggingface langchain-text-splitters faiss-cpu pypdf sentence-transformers ollama
```

---

### 4️⃣ Install Ollama

Download and install Ollama:

https://ollama.com/download

Verify installation:

```bash
ollama --version
```

---

### 5️⃣ Pull Llama 3 Model

```bash
ollama pull llama3
```

You can also use:

```bash
ollama pull mistral
```

or

```bash
ollama pull llama3:8b
```

---

## ▶️ Running the Project

### Start Ollama

```bash
ollama serve
```

---

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```bash
RAG_PDF_Text_Extractor.ipynb
```

Run all cells sequentially.

---

## 🔄 Workflow

```text
PDF Document
      │
      ▼
Text Extraction
      │
      ▼
Chunking
      │
      ▼
Hugging Face Embeddings
      │
      ▼
Vector Store (FAISS)
      │
      ▼
User Query
      │
      ▼
Retriever
      │
      ▼
Relevant Context
      │
      ▼
Ollama (Llama 3)
      │
      ▼
Generated Answer
```

---

## 📖 Example Usage

### Sample Query

```text
What are the key responsibilities mentioned in the document?
```

### Generated Response

```text
According to the document, the key responsibilities include...
```

---

## 📊 Why RAG?

Traditional LLMs rely solely on pre-trained knowledge and may generate inaccurate information.

RAG improves reliability by:

* Retrieving relevant information from your documents.
* Providing context before answer generation.
* Reducing hallucinations.
* Enabling document-specific question answering.

---

## 🎯 Use Cases

* Research Paper Analysis
* Resume Parsing
* Legal Document Review
* Company Policy Search
* Academic Question Answering
* Knowledge Base Chatbots
* Contract Understanding

---

## 🔒 Privacy & Security

Since the project uses:

* Local Ollama models
* Local vector databases
* Local PDF processing

your data never leaves your machine.

---

## 📈 Future Enhancements

* Multi-PDF Support
* PDF Table Extraction
* OCR for Scanned Documents
* Streamlit Web Interface
* Chat History Memory
* Hybrid Search (Keyword + Semantic)
* Metadata Filtering

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature-name
```

3. Commit changes

```bash
git commit -m "Added new feature"
```

4. Push to GitHub

```bash
git push origin feature-name
```

5. Create a Pull Request

---

## 👨‍💻 Author

**Shanmuka Priya Salapu**

GitHub:
https://github.com/shanmuka0731

---

⭐ If you found this project useful, please consider giving the repository a star!
