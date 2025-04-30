# 🧠 RAG Chatbot with TinyLlama

This project is a lightweight, local **Retrieval-Augmented Generation (RAG)** chatbot built using Hugging Face’s **TinyLlama** and **FAISS**. It lets you ask natural language questions and get accurate, document-grounded answers — all running locally.

---

## 🚀 Features

- 🔍 Retrieve relevant content from your own `.txt` documents
- 🧠 Use semantic search (via embeddings) with FAISS
- 🤖 Generate answers using TinyLlama or other Hugging Face models
- 📄 Avoid hallucination — only respond using retrieved context
- 🖥️ Runs entirely on your own machine (works even on CPU)

---

## 📁 Repository Structure

```
RAG_Chatbot_With_TinyLlama/
├── knowledge_base/           # Folder for your input .txt documents
│   ├── company_policy.txt    # Example file
│
├── RAG.ipynb                 # Jupyter notebook with the full working chatbot
├── README.md                 # This file
```

> ℹ️ Additional modular scripts like `retriever.py`, `generator.py`, or `app.py` can be added for structured production code if needed.

---

## 📚 How It Works

1. 🔹 **User types a question**
2. 🔹 The query is embedded using a SentenceTransformer
3. 🔹 FAISS searches your documents for the most relevant chunks
4. 🔹 The top result is inserted into a prompt
5. 🔹 TinyLlama generates a short, accurate answer using that context
6. 🔹 You see the response in your notebook or interface

---

## 📦 Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/<your_username>/RAG_Chatbot_With_TinyLlama.git
cd RAG_Chatbot_With_TinyLlama
pip install -r requirements.txt
```

Recommended dependencies (add to `requirements.txt`):
```
transformers
sentence-transformers
faiss-cpu
accelerate
gradio
```

---

## 🧪 Example Query

**User:** How many days can I take leave?  
**Bot:** Employees are entitled to 20 days of paid vacation per year.

---

## 📝 To Do

- [ ] Add document source citation to answers
- [ ] Support for multi-turn conversation
- [ ] Modularize code into scripts
- [ ] Add Streamlit or Gradio interface

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

---

## 📜 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

- [TinyLlama Model](https://huggingface.co/TinyLlama)
- [FAISS](https://github.com/facebookresearch/faiss)
- [Hugging Face Transformers](https://huggingface.co/transformers/)
