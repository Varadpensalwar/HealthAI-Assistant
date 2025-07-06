# HealthAI-Assistant

## 🩺 Overview

HealthAI-Assistant is a medical chatbot that leverages AI to provide health-related information based on medical literature. The application uses a Retrieval-Augmented Generation (RAG) approach to answer user queries by referencing a medical knowledge base.

## ✨ Features

- Interactive chat interface for medical queries
- Retrieval-Augmented Generation (RAG) for accurate responses
- Integration with Pinecone vector database for efficient knowledge retrieval
- Powered by OpenAI's language models
- Responsive web interface

## 🛠️ Tech Stack

### Backend
- Python 3.10
- Flask (Web framework)
- LangChain (Framework for LLM applications)
- Pinecone (Vector database)
- OpenAI API (Language model)
- HuggingFace Embeddings (sentence-transformers)

### Frontend
- HTML/CSS
- JavaScript
- jQuery
- Bootstrap 4

## 📁 Project Structure

```
HealthAI-Assistant/
├── Data/
│   └── Medical_book.pdf         # Medical knowledge base
├── src/
│   ├── __init__.py
│   ├── helper.py                # Utility functions for document processing
│   └── prompt.py                # System prompts for the AI
├── static/
│   └── style.css                # CSS styling
├── templates/
│   └── chat.html                # Chat interface
├── app.py                       # Main Flask application
├── Dockerfile                   # Docker configuration
├── requirements.txt             # Python dependencies
├── setup.py                     # Package setup
├── store_index.py               # Script to create and populate Pinecone index
└── README.md                    # Project documentation
```

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or higher
- Pinecone API key
- OpenAI API key

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Varadpensalwar/HealthAI-Assistant.git
   cd HealthAI-Assistant
   ```

2. Create a virtual environment and activate it:
   ```bash
   conda create --name HealthAI-Assistant python=3.10
   conda activate HealthAI-Assistant
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the root directory with the following variables:
   ```env
   PINECONE_API_KEY=your_pinecone_api_key
   OPENAI_API_KEY=your_openai_api_key
   ```

### Setting Up the Vector Database

Before running the application, you need to create and populate the Pinecone index with the medical data:

```bash
python store_index.py
```

This script will:
- Load the medical PDF from the Data directory
- Split the text into chunks
- Create embeddings using HuggingFace's sentence transformer
- Store these embeddings in a Pinecone index

### Running the Application

Start the Flask application:

```bash
python app.py
```

The application will be available at [http://localhost:8080](http://localhost:8080).

## 🐳 Docker Deployment

You can also run the application using Docker:

1. Build the Docker image:
   ```bash
   docker build -t healthai-assistant .
   ```

2. Run the container:
   ```bash
   docker run -p 8080:8080 -e PINECONE_API_KEY=your_pinecone_api_key -e OPENAI_API_KEY=your_openai_api_key healthai-assistant
   ```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the terms of the license included in the [LICENSE](LICENSE) file.

## 📧 Contact

For questions or feedback, please contact:
- **Author:** Varad Pensalwar
- **GitHub:** [Varadpensalwar](https://github.com/Varadpensalwar)
- **Telegram:** [@Varadpensalwar](https://t.me/Varadpensalwar)
- **Issues:** [GitHub Issues](https://github.com/Varadpensalwar/VaradGPT-Bot/issues)

---

Made with ❤️ by [Varadpensalwar](https://github.com/Varadpensalwar)
