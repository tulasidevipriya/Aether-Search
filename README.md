# Aether Search: Powered by Endee

Aether Search is a high-performance demonstration of **Endee**, a lightweight, embedded vector database designed for Semantic Search, Retrieval-Augmented Generation (RAG), and AI-driven recommendations.

![Project Preview](client/public/hero-network.png)

## 🚀 Overview

Traditional keyword search often fails to capture user intent. Aether Search demonstrates how vector search enables applications to understand context and meaning, providing more relevant results and grounded AI responses.

### Key Features
- **Semantic Search**: Real-time vector similarity search with score visualization.
- **RAG Pipeline**: Integration showing how retrieved context grounds LLM generations.
- **System Architecture**: Documentation of the data ingestion and retrieval workflow.
- **Embedded Performance**: Optimized for local development and edge deployment.

## 🛠 Technical Approach

Aether Search utilizes a modern RAG (Retrieval-Augmented Generation) architecture:
1.  **Ingestion**: Documents are chunked and converted into vector embeddings using OpenAI's `text-embedding-3-small` model.
2.  **Storage**: Vectors and metadata are stored in the **Endee** vector database for low-latency retrieval.
3.  **Retrieval**: User queries are embedded and compared against the database using cosine similarity.
4.  **Generation**: The most relevant context is injected into a prompt to provide accurate, source-backed answers.

## 📦 How Endee is Used

Endee serves as the core vector engine, providing:
- **Efficient Indexing**: Fast addition of high-dimensional vectors.
- **Similarity Search**: Optimized K-Nearest Neighbors (KNN) search.
- **Metadata Management**: Seamless linking of vectors to source content.
- **Embedded Footprint**: No need for external database infrastructure, making it perfect for rapid prototyping and local AI apps.

## ⚙️ Setup & Execution

### Prerequisites
- Node.js v18+
- npm / yarn
- OpenAI API Key

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/aether-search.git
   cd aether-search
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure environment variables:
   Create a `.env` file in the root:
   ```env
   OPENAI_API_KEY=sk-your-key-here
   ENDEE_DB_PATH=./data/vectors
   ```

4. Run the development server:
   ```bash
   npm run dev
   ```

The application will be available at `http://localhost:5000`.

## 📜 License
MIT
