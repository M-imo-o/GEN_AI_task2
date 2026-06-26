# 🌐 Website Content RAG Assistant

A Retrieval-Augmented Generation (RAG) application built using **LangChain**, **FAISS**, **Hugging Face Embeddings**, **Groq LLM**, and **Gradio**. The application allows users to load the content of a website using its URL and ask questions that are answered strictly from the website's content.

---

## 📌 Features

* 🌐 Load website content using a URL
* ✂️ Split website content into semantic chunks
* 🔎 Generate embeddings using Hugging Face sentence-transformers
* 🗄️ Store embeddings in a FAISS vector database
* 🤖 Ask natural language questions about the website
* 🎛️ Adjustable response temperature (0.0–1.0)
* 🛡️ Built-in prompt injection and jailbreak protection
* 🔒 Content safety filtering for unsafe or malicious queries
* 📄 Displays the retrieved source chunks used to generate the answer
* ❌ Reduces hallucinations by answering only from retrieved website content

---

## 🛠️ Technologies Used

* Python
* LangChain
* Gradio
* FAISS
* Hugging Face Embeddings
* Groq API (Llama 3.3 70B)
* BeautifulSoup (via WebBaseLoader)

---

## 📂 Project Workflow

1. Enter a website URL.
2. Click **Load Website**.
3. The website is loaded and split into chunks.
4. Embeddings are generated for each chunk.
5. Chunks are stored in a FAISS vector database.
6. Ask questions about the website.
7. The system retrieves the most relevant chunks.
8. The LLM generates an answer using only the retrieved context.
9. Retrieved source chunks are displayed for transparency.

---
Output ss:

<img width="1902" height="896" alt="Screenshot 2026-06-26 225220" src="https://github.com/user-attachments/assets/ae0e055f-9040-4535-9eda-c54c6f360e0c" />

<img width="1875" height="891" alt="Screenshot 2026-06-26 225308" src="https://github.com/user-attachments/assets/1f10722b-e9ab-4f4f-ab13-759f819167cd" />

<img width="1879" height="893" alt="Screenshot 2026-06-26 225343" src="https://github.com/user-attachments/assets/8110a956-4ba5-41f8-9286-4365fceb8c9f" />

<img width="1877" height="876" alt="Screenshot 2026-06-26 225432" src="https://github.com/user-attachments/assets/4f0e5e4c-c7ec-48a9-8e6c-d06c911e9eca" />


## 🛡️ Guardrails Implemented

* Prompt Injection Detection
* Jailbreak Protection
* Regex-based malicious query filtering
* LLM-based content safety classifier
* Sensitive information request detection
* Hallucination minimization
* Context-only answering

---

## 📸 User Interface

The application provides:

* Website URL input
* Load Website button
* Status display
* Temperature slider
* Question input
* Get Answer button
* AI Answer panel
* Retrieved Source Chunks panel

---

## ▶️ How to Run

1. Clone this repository.
2. Install the required dependencies.
3. Set your `GROQ_API_KEY`.
4. Run the application.

```bash
pip install -r requirements.txt
python app.py
```

---

## 📦 Required Packages

* gradio
* langchain
* langchain-community
* langchain-groq
* langchain-huggingface
* faiss-cpu
* sentence-transformers
* beautifulsoup4
* lxml



