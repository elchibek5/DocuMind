# DocuMind - AI Research Assistant 🧠

DocuMind is a Retrieval-Augmented Generation (RAG) application that allows users to chat with multiple PDF documents in natural language. It utilizes OpenAI's GPT models for reasoning and FAISS for semantic vector search, enabling instant information retrieval from dense technical documentation.

## 🚀 Tech Stack
* **Backend:** Python, LangChain
* **Frontend:** Streamlit
* **AI Engine:** OpenAI GPT-3.5 Turbo (LLM), OpenAI Embeddings
* **Vector Database:** FAISS (Facebook AI Similarity Search)
* **PDF Processing:** PyPDF2

## ⚙️ Architecture
1.  **Ingestion:** PDFs are parsed and split into chunks of 1000 characters.
2.  **Embedding:** Text chunks are converted into vector embeddings using OpenAI models.
3.  **Storage:** Vectors are stored in a local FAISS index for high-speed retrieval.
4.  **Retrieval:** User queries are converted to vectors; the system performs a cosine similarity search to find relevant text chunks.
5.  **Generation:** The top-k relevant chunks are fed into the LLM as context to generate an accurate answer.

## 🛠️ How to Run Locally
1.  **Clone the repository**
    ```bash
    git clone [https://github.com/elchibekd/DocuMind.git](https://github.com/elchibekd/DocuMind.git)
    cd DocuMind
    ```
2.  **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Set up environment variables**
    Create a `.env` file and add your OpenAI API key:
    ```bash
    OPENAI_API_KEY=your_api_key_here
    ```
4.  **Run the app**
    ```bash
    streamlit run app.py
    ```
