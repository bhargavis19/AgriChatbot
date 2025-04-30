
# 🌾 AgriChatbot: A Retrieval-Augmented Conversational Agent for Agricultural Advisory

AgriChatbot is an AI-powered chatbot that helps farmers and agricultural researchers by providing contextual answers to crop-related questions, such as pest management and disease diagnosis. It combines information retrieval from scientific literature with language generation to give meaningful, accurate responses.

---

## 📘 Project Overview

In rural agricultural communities, farmers often lack timely access to expert knowledge. This chatbot addresses that gap by using Retrieval-Augmented Generation (RAG) — first retrieving relevant snippets from agricultural research papers, then generating natural-language answers based on that context.

The chatbot simulates realistic conversations between farmers, with a focus on Hindi-to-English accuracy, farming practices, and pest/disease control in crops like tomato.

---

## 🧠 How It Works

1. **User asks a question** related to agriculture.
2. **Retriever module** searches for relevant paragraphs from a local database of scientific papers using semantic similarity (FAISS + SentenceTransformers).
3. **Generator module** takes the question and retrieved passages as input and generates an answer using a language model (e.g., GPT-2 or another lightweight LLM).
4. **Answer is displayed** in conversational tone, optimized for agricultural advisory.

---

## 📂 Data Source

The chatbot uses real scientific papers as its knowledge base:

- *Module of Integrated Insect Pest Management on Tomato*
- *Integrated Pest Management in the Academic Greenhouse Setting: A Case Study Using Solanum spp.*
- *Cronartium Rust Sporulation on Hemiparasitic Plants*

Each document was:

- Converted from PDF to text
- Chunked into small, readable passages
- Embedded into vector format using `SentenceTransformer`
- Indexed using `FAISS` for fast retrieval

---

## 🛠️ Code Structure

```
├── chatbot.py           # Main chatbot interface
├── retriever.py         # Search and embedding logic
├── generator.py         # Response generation logic
├── /data                # Raw and processed research papers
├── /embeddings          # FAISS index and vector storage
├── system_diagram.png   # Visual system overview
└── README.md            # This file
```

---

## 💬 Example Use

```text
👩‍🌾 Ask your agriculture-related question (or type 'exit' to quit):
What is the disease affecting my tomato plant?

🤖 Chatbot:
The text does not provide information about a specific disease, but highlights pests like the tomato fruitworm and red spider mite, with IPM methods for managing them.
```

---

## 🔍 Technologies Used

- Hugging Face Transformers (GPT-2 / T5)
- SentenceTransformers for embedding
- FAISS for dense vector retrieval
- PyTorch for model inference
- Kaggle GPU runtime

---

## 📈 Results

- ✅ High relevance of retrieved passages
- 🧑‍🌾 Farmer-friendly language in responses
- ⚡ Real-time interaction loop
- 📄 Domain-specific accuracy from curated literature

---

## 🔭 Future Improvements

- Support for **Hindi / multilingual input**
- **Mobile app** or WhatsApp interface
- Larger and **continually updated dataset**
- Fine-tuned generation model on agricultural dialogues

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgements

- Hugging Face 🤗
- ResearchGate authors for open access content
- FAISS team at Meta AI
- Kaggle for GPU runtime
