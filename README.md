# 🤖 Two-way-RAG

<div align="center">

<!-- TODO: Add project logo (e.g., an icon representing AI/interaction) -->

[![GitHub stars](https://img.shields.io/github/stars/ambrose-kutti/Two-way-RAG?style=for-the-badge)](https://github.com/ambrose-kutti/Two-way-RAG/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/ambrose-kutti/Two-way-RAG?style=for-the-badge)](https://github.com/ambrose-kutti/Two-way-RAG/network)
[![GitHub issues](https://img.shields.io/github/issues/ambrose-kutti/Two-way-RAG?style=for-the-badge)](https://github.com/ambrose-kutti/Two-way-RAG/issues)
[![GitHub license](https://img.shields.io/github/license/ambrose-kutti/Two-way-RAG?style=for-the-badge)](LICENSE)

**An interactive Retrieval Augmented Generation (RAG) system enabling dynamic, context-aware conversational AI through a bidirectional approach.**

<!-- TODO: Add live demo link if available -->
<!-- [Live Demo](https://demo-link.com) | -->
<!-- TODO: Add documentation link if available -->
<!-- [Documentation](https://docs-link.com) -->

</div>

## 📖 Overview

Two-way-RAG is a robust web application that leverages Retrieval Augmented Generation (RAG) to provide highly contextual and accurate responses to user queries. Unlike traditional RAG systems, this project incorporates a "two-way" mechanism, where both the initial query and the retrieved documents dynamically inform and refine each other, leading to a more coherent and precise generative process. It features a user-friendly interface for document ingestion and interactive querying, making complex AI interactions accessible.

## ✨ Features

-   **Interactive Web Interface**: A clean, responsive user interface for seamless interaction with the RAG system.
-   **Document Ingestion**: Easily upload and process various document types (e.g., PDF, TXT) to build your knowledge base.
-   **Semantic Retrieval**: Utilizes advanced embedding models to perform context-aware searches over ingested documents, fetching the most relevant information.
-   **LLM Integration**: Seamlessly integrates with Large Language Models (LLMs) to generate natural, human-like, and factually grounded responses.
-   **Two-way Contextualization**: Dynamically refines both document retrieval and LLM generation based on the evolving conversational context and query nuances.
-   **Configurable Environment**: Supports easy configuration of LLM providers, embedding models, and vector database settings via environment variables.

## 🖥️ Screenshots

<!-- TODO: Add actual screenshots of the application, showing document upload, query interface, and responses. -->
<!-- ![Screenshot 1](path-to-screenshot-1.png) -->
<!-- ![Screenshot 2](path-to-screenshot-2.png) -->

## 🛠️ Tech Stack

**Backend:**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1A900A?style=for-the-badge&logo=langchain&logoColor=white)
![Transformers](https://img.shields.io/badge/HuggingFace_Transformers-FFD21C?style=for-the-badge&logo=huggingface&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)

**Vector Database:**
![ChromaDB](https://img.shields.io/badge/ChromaDB-0062FF?style=for-the-badge&logo=chroma&logoColor=white)

**Frontend:**
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 🚀 Quick Start

Follow these steps to get Two-way-RAG up and running on your local machine.

### Prerequisites

Before you begin, ensure you have the following installed:

-   **Python**: Version 3.9 or higher (recommended 3.10+)
-   **pip**: Python package installer (usually comes with Python)

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/ambrose-kutti/Two-way-RAG.git
    cd Two-way-RAG
    ```

2.  **Install dependencies**
    It's recommended to use a virtual environment.

    ```bash
    # Create a virtual environment
    python -m venv venv

    # Activate the virtual environment
    # On Windows
    .\venv\Scripts\activate
    # On macOS/Linux
    source venv/bin/activate

    # Install Python dependencies
    pip install -r requirements.txt
    ```

3.  **Environment setup**
    Create a `.env` file in the root directory by copying the example. Then, configure your environment variables.

    ```bash
    # No .env.example found, creating a minimal one for demonstration
    cp .env.example .env # If it existed, otherwise create manually
    ```
    
4.  **Vector Database setup**
    This project uses ChromaDB, which by default runs in-memory or on disk. The `VECTOR_DB_PATH` in your `.env` file determines where the data is stored. No separate server setup is typically required for local development. The database will be initialized automatically on first use if the path does not exist.

5.  **Start development server**
    ```bash
    python main.py
    ```

6.  **Open your browser**
    Visit `http://localhost:5000` (or the port indicated in your console) to access the application.

## 📁 Project Structure

```
Two-way-RAG/
├── .gitignore          # Specifies intentionally untracked files to ignore
├── main.py             # Main Fastapi application entry point, RAG pipeline, and API logic
├── requirements.txt    # Lists all Python dependencies
├── static/             # Contains static assets like CSS, JavaScript, and images
│   ├── css/            # Stylesheets for the web interface
│   └── js/             # Client-side JavaScript for interactive elements
└── templates/          # HTML templates rendered by Fastapi
    └── index.html      # The main page template for the application
```

## ⚙️ Configuration

### Environment Variables
Environment variables are loaded from the `.env` file to manage sensitive information and configurable parameters.

| Variable             | Description                                          | Default (inferred)     | Required |
|----------------------|------------------------------------------------------|------------------------|----------|
| `VECTOR_DB_PATH`     | Filesystem path for the ChromaDB persistence.        | `./chroma_data`        | No       |
| `EMBEDDING_MODEL_NAME` | The name or path of the embedding model to use.      | `all-MiniLM-L6-v2`     | No       |
| `LLM_MODEL_NAME`     | The specific LLM model identifier                    . |  | Yes     |

## 🔧 Development

### Available Scripts

The primary script for running the application is `main.py`.

| Command              | Description                                        |
|----------------------|----------------------------------------------------|
| `python main.py`     | Starts the Flask development server.               |

### Development Workflow

1.  Ensure your virtual environment is activated (`source venv/bin/activate`).
2.  Make changes to `main.py` for backend logic or `templates/index.html`, `static/css/`, `static/js/` for frontend adjustments.
3.  The Flask development server, when run with `python main.py`, typically includes a reloader that automatically restarts the server upon code changes.

## 📚 API Reference

The application serves as a web interface with a backend API.

### `/` (GET)
-   **Description**: Renders the main application interface (`index.html`). This is where users interact with the RAG system.

### `/upload` (POST)
-   **Description**: Handles the upload and processing of documents.
    -   Takes a file input (e.g., PDF, TXT).
    -   Processes the document (chunking, embedding).
    -   Adds the document's embeddings to the vector database.
-   **Request Body**: `multipart/form-data` containing the document file.

### `/query` (POST)
-   **Description**: Processes a user query against the loaded knowledge base using the two-way RAG mechanism.
    -   Retrieves relevant documents.
    -   Augments the query with retrieved context.
    -   Sends the augmented prompt to the LLM.
    -   Returns the LLM's generated response.
-   **Request Body**:
    ```json
    {
        "query": "Your question here..."
    }
    ```
-   **Response**:
    ```json
    {
        "response": "The LLM's generated answer based on retrieval."
    }
    ```

## 🤝 Contributing

We welcome contributions to improve Two-way-RAG! If you're interested in contributing, please consider the following:

-   Fork the repository.
-   Create a new branch for your feature or bug fix.
-   Implement your changes, ensuring code quality and adherence to existing patterns.
-   Open a pull request with a clear description of your changes.

### Development Setup for Contributors

Follow the **Quick Start** instructions to set up your development environment. Ensure you activate your virtual environment before running any commands.

## 📄 License

This project is open-source. Please see the [LICENSE](LICENSE) file for details.
<!-- TODO: Add a LICENSE file with the chosen license (e.g., MIT, Apache 2.0) -->

## 🙏 Acknowledgments

-   **Flask**: For providing a lightweight and powerful web framework.
-   **LangChain**: For simplifying the orchestration of LLM applications.
-   **Hugging Face Transformers**: For access to state-of-the-art NLP models.
-   **ChromaDB**: For an excellent open-source vector database solution.
-   **OpenAI/Other LLM Providers**: For powerful generative AI models.

## 📞 Support & Contact

-   🐛 Issues: If you encounter any problems or have suggestions, please open an issue on the [GitHub Issues](https://github.com/ambrose-kutti/Two-way-RAG/issues) page.
-   👤 Author: Ambrose Kutti

---

<div align="center">

**⭐ Star this repo if you find it helpful or interesting!**

Made with ❤️ by [Ambrose Kutti](https://github.com/ambrose-kutti)

</div>
