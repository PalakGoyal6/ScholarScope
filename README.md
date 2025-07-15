# 🧠 AI Research Paper Assistant (Multi-PDF)

An intelligent Streamlit-based app for **summarizing**, **querying**, and **comparing** academic research papers. Upload multiple PDFs, ask natural language questions, get concise AI-generated answers, and view exactly where the answer comes from — all in one place.


<p align="center">
  <img src="https://github.com/user-attachments/assets/143a17d9-dccf-4bf1-92f4-d87604087a5b" width="300" />
  <img src="https://github.com/user-attachments/assets/af227ac6-45a2-4913-aaf9-e2c4db431a1b" width="300" />
  <img src="https://github.com/user-attachments/assets/022b9256-a7dc-4ce3-8225-b14053501c73" width="300" />
</p>


## 🔍 Features

### 📥 Upload Multiple PDFs
- Upload one or more research papers in `.pdf` format.
- Each paper is processed and stored with full text and structure.

### 🧾 AI-Powered Summarization
- Summarizes each paper into **5–7 bullet points** using the `Cypher-Alpha` model via OpenRouter.
- Automatically calculates:
  - Word count
  - Number of pages
  - Estimated reading time
- Option to **download summaries** as `.txt`.

### 🧠 Question & Answer (Q&A)
- Ask any natural language question for a selected paper.
- Internally:
  - Paper is chunked and embedded using `MiniLM-L6-v2` from HuggingFace.
  - FAISS is used for vector-based semantic similarity search.
  - Relevant chunks are passed to Cypher-Alpha for concise, referenced answers.
- Tracks and shows **referenced CHUNKs** in response.

### 👁️ Visual "Chunk Viewer"
- Click "View Chunk" to see:
  - The **page image** from where the chunk was extracted.
  - The **matched chunk text**.
- Helps connect answers to source material directly.

### 🧪 AI Comparison of Papers
- If more than one paper is uploaded:
  - Displays summaries **side by side**.
  - Generates a comparative analysis using LLM.
  - Download the **AI-generated comparison**.

### 🗂 Chat History (Per-Paper)
- Tracks all questions & answers per uploaded paper.
- Lets users revisit previous Q&A sessions independently for each document.


## 🔗 Live Demo

Try the app here: [ScholarScope](https://scholarscope-66caiyfefwz2gqz5ssifox.streamlit.app/)
