# 💬 RAG-chat

<div align="center">

![GitHub stars](https://img.shields.io/github/stars/ambrose-kutti/RAG-chat?style=for-the-badge&logo=github)
[![GitHub forks](https://img.shields.io/github/forks/ambrose-kutti/RAG-chat?style=for-the-badge&logo=git)](https://github.com/ambrose-kutti/RAG-chat/network)
[![GitHub issues](https://img.shields.io/github/issues/ambrose-kutti/RAG-chat?style=for-the-badge&logo=github)](https://github.com/ambrose-kutti/RAG-chat/issues)
[![GitHub license](https://img.shields.io/github/license/ambrose-kutti/RAG-chat?style=for-the-badge)](LICENSE)

**An intelligent RAG-powered chatbot for contextual conversations and document interaction.**

</div>

## 📖 Overview

RAG-chat is a web application designed to provide contextual answers by leveraging Retrieval Augmented Generation (RAG). It allows users to upload TXT document which are then used to augment a Large Language Model (LLM)'s responses. This ensures that the chatbot provides accurate, relevant, and up-to-date information directly from your provided sources.

## ✨ Features

-   **Interactive Chat Interface**: A user-friendly web interface for engaging in natural language conversations.
-   **Source Data Ingestion**:
    -   📚 **Document Upload**: Process and embed content from TXT files.
-   **Retrieval Augmented Generation (RAG)**: Dynamically retrieve relevant information from ingested data to inform LLM responses.
-   **Vector Store Integration**: Utilizes ChromaDB for efficient storage and retrieval of document embeddings.
-   **Flexible LLM Support**: Built with LangChain, enabling easy integration with various LLMs.
-   **Persistent Context**: Maintains a knowledge base derived from all ingested sources for comprehensive query handling.

## 🛠️ Tech Stack

**Backend:**
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![LangChain](https://img.shields.io/badge/LangChain-263238?style=for-the-badge&logo=langchain&logoColor=white)](https://www.langchain.com/)
[![ChromaDB](https://img.shields.io/badge/ChromaDB-005C1F?style=for-the-badge&logo=chroma&logoColor=white)](https://www.trychroma.com/)
[![Sentence-Transformers](https://img.shields.io/badge/Sentence--Transformers-000000?style=for-the-badge&logo=huggingface&logoColor=white)](https://www.sbert.net/)
[![Unstructured.io](https://img.shields.io/badge/Unstructured.io-000000?style=for-the-badge)](https://unstructured.io/)

**Frontend:**
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

**DevOps & Tools:**
[![python-dotenv](https://img.shields.io/badge/python--dotenv-lightgreen?style=for-the-badge)](https://pypi.org/project/python-dotenv/)

## 🚀 Quick Start

Follow these steps to get RAG-chat up and running on your local machine.

### Prerequisites

-   **Python 3.9+** (recommended)
-   `pip` package manager

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/ambrose-kutti/RAG-chat.git
    cd RAG-chat
    ```

2.  **Create and activate a virtual environment** (recommended)
    ```bash
    python -m venv venv
    # On Windows
    venv\Scripts\activate
    # On macOS/Linux
    source venv/bin/activate
    ```

3.  **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Environment setup**
    Create a `.env` file in the root directory of the project based on the `.env.example` structure.
    ```bash
    cp .env.example .env
    ```

5.  **Run the application**
    ```bash
    python main.py
    ```

6.  **Open your browser**
    Visit `http://localhost:5000` (or the port indicated in your console) to access the chat interface.

## 📁 Project Structure

```
RAG-chat/
├── .gitignore          # Specifies intentionally untracked files to ignore
├── main.py             # Main Fatapi application logic and entry point
├── requirements.txt    # Python dependencies for the project
├── static/             # Static assets (CSS, JavaScript, images)
│   ├── css/            # Stylesheets
│   │   └── style.css
│   └── js/             # Client-side JavaScript
│       └── script.js
└── templates/          # HTML templates rendered by Fastapi (Jinja2)
    └── index.html      # The main chat interface
```

## ⚙️ Configuration

### Configuration Files

-   **`requirements.txt`**: Defines all necessary Python packages.

## 🔧 Development

### Development Workflow

1.  Ensure your virtual environment is activated (`source venv/bin/activate`).
2.  Make changes to `main.py` for backend logic, `templates/index.html` for the UI structure, or `static/css/style.css` and `static/js/script.js` for styling and client-side interactivity.
3.  The Flask development server automatically reloads on code changes, so you typically just need to save your files.

## 🚀 Deployment

### Production Build

Since this is a Fastapi application, there isn't a separate "build" step in the same way a frontend framework might have. The `main.py` application is run directly.

### Deployment Options

-   **Traditional Hosting**: Deploy to any server that can run Python applications (e.g., Gunicorn + Nginx, Apache with WSGI). Ensure all `requirements.txt` dependencies are installed and the `.env` file is properly configured on the production server.
-   **Docker**: Create a `Dockerfile` to containerize the application for easier deployment across various environments.

## 🤝 Contributing

We welcome contributions to RAG-chat! If you have suggestions for improvements, new features, or bug fixes, please open an issue or submit a pull request.

### Development Setup for Contributors

1.  Follow the **Quick Start** section to set up the project locally.
2.  Create a new branch for your feature or bug fix: `git checkout -b feature/your-feature-name`.
3.  Ensure your code adheres to a consistent style.
4.  Commit your changes with a descriptive message.
5.  Push your branch and open a pull request.

## 📄 License

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.

## 🙏 Acknowledgments

-   **LangChain**: For simplifying the development of LLM-powered applications.
-   **ChromaDB**: For providing an efficient open-source vector database.
-   **Flask**: For the lightweight web framework.
-   **Unstructured.io**: For robust document parsing capabilities.
-   The open-source community for countless valuable libraries.

## 📞 Support & Contact

-   🐛 Issues: [GitHub Issues](https://github.com/ambrose-kutti/RAG-chat/issues)
-   📧 Contact: [ambrose.kutti@example.com](mailto:ambrose.kutti@example.com) <!-- TODO: Add actual contact email -->

---

<div align="center">

**⭐ Star this repo if you find it helpful!**

Made with ❤️ by [ambrose-kutti](https://github.com/ambrose-kutti)

</div>
