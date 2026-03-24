# Swami Vivekananda -- The knowledge 
![colombo to almora](https://github.com/user-attachments/assets/073ae9f4-adbc-4d53-885e-fcf72c56cf73)

**Vivek Vaani** is a Retrieval-Augmented Generation (RAG) based AI assistant built with Streamlit. It allows users to ask questions and gain insights grounded in the teachings and lectures of Swami Vivekananda, specifically from his classic book *"Lectures from Colombo to Almora"*. 

## 🌟 Features
- **Conversational Interface:** An intuitive chat interface built with Streamlit.
- **Context-Aware Responses:** Uses Google Gemini (`gemini-2.5-flash`) to generate accurate answers based purely on the provided text.
- **Fast and Efficient Retrieval:** Employs `FastEmbedEmbeddings` and ChromaDB to parse and query the source content quickly.
- **PDF Document Processing:** Automatically extracts and chunks text from the source PDF securely on the local machine.

## 🛠️ Tech Stack
- **Frontend:** [Streamlit](https://streamlit.io/)
- **LLM Engine:** [Google Gemini API](https://ai.google.dev/) (`genai.Client`)
- **Embeddings:** [FastEmbed](https://qdrant.github.io/fastembed/) (`thenlper/gte-large`)
- **Vector Database:** [Chroma](https://www.trychroma.com/)
- **Orchestration:** [LangChain](https://www.langchain.com/) (Document loaders, Text Splitters, Output Parsers)

## 🚀 Getting Started

### Prerequisites

1. **Python 3.8+** installed on your system.
2. A **Google Gemini API Key**.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/adityakanamadi281/Vivek_Vaani.git 
   cd Vivek_Vaani
   ```

2. Set up a virtual environment (optional but recommended):
   ```bash
   uv venv
   ```

3. Install the required dependencies:
   ```bash
   uv pip install -r requirements.txt
   ```

4. Create a `.env` file in the root directory and add your Google Gemini API key:
   ```env
   GEMINI_API_KEY=your_api_key_here
   ```

5. Ensure that the source PDF is present in the specified directory (`data/Lectures_from_Colombo_To_Almora.pdf`).

### Running the App

Run the Streamlit application using the following command:
```bash
streamlit run app.py
```
After running the command, an interface will open in your default browser where you can start asking questions.

## 📂 Project Structure

- `app.py`: The main entry point for the Streamlit application containing the RAG pipeline.
- `src/`: Directory containing inference scripts and custom logic.
- `data/`: Directory for storing source documents like the target PDF.
- `chroma_db/`: Directory where the persistent vector database is saved.
