
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


## 📈 Results

- ✅ High relevance of retrieved passages
- 🧑‍🌾 Farmer-friendly language in responses
- ⚡ Real-time interaction loop
- 📄 Domain-specific accuracy from curated literature

---
