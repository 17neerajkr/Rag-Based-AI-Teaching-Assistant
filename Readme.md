# RAG-Based AI Teaching Assistant

## Project Overview

An AI-powered Teaching Assistant built using Retrieval-Augmented Generation (RAG) architecture that answers user queries from educational video content.

The system processes video lectures, converts them into transcripts, generates embeddings, retrieves relevant context, and produces intelligent responses using an LLM.

---

## Features

- Video → Audio conversion
- Speech-to-Text transcription
- Transcript preprocessing
- Embedding generation
- Semantic search using cosine similarity
- Context retrieval
- LLM-based question answering

---

## Tech Stack

- Python
- FFmpeg
- Whisper
- Ollama
- LLaMA
- BGE-M3 Embeddings
- Scikit-learn
- Joblib

---

## Workflow

### Step 1 — Add Videos

Move video files into:

```txt
/videos
```

### Step 2 — Video to Audio

Run:

```bash
python video_to_mp3.py
```

Convert videos into MP3 files.

### Step 3 — Audio to Transcript

Run:

```bash
python mp3_to_json.py
```

Generate transcript JSON files using Whisper.

### Step 4 — Generate Embeddings

Run:

```bash
python preprocess_json.py
```

Creates embeddings dataframe and saves Joblib file.

### Step 5 — Ask Questions

Load embeddings into memory.

User query → Similarity search → Context retrieval → LLM response generation.

---

## Project Structure

```txt
project/
│
├── videos/
├── mp3/
├── json/
├── embeddings/
├── scripts/
│   ├── video_to_mp3.py
│   ├── mp3_to_json.py
│   ├── preprocess_json.py
│
├── requirements.txt
└── README.md
```

---

## Installation

```bash
git clone YOUR_REPO_LINK
cd Rag-Based-AI-Teaching-Assistant

pip install -r requirements.txt
```

---

## Results

- Processed 100+ lecture videos
- Generated 1000+ embeddings
- Implemented semantic retrieval
- Built timestamp-aware AI answering system

---

## Future Improvements

- Streamlit Web UI
- Multi-language support
- Real-time lecture Q&A
- Vector Database integration
