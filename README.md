# Dharmic Intelligence Platform

Where epic wisdom meets modern moral dilemmas.

## Overview

The Dharmic Intelligence Platform is a prototype web application that maps user moral dilemmas to passages from the Mahābhārata, uses semantic search to retrieve relevant contexts, and adapts narrative-driven responses to the user's age, education level, and cultural framing. It is **not** here to tell you what to do. It's here to make you pause, think, and possibly imagine what Bhishma might have said, but without the long lectures (well… mostly).

## Features

- **Semantic Search:** Finds the most relevant Mahābhārata passages to your query.
- **Adaptive Narratives:** Alters tone and content based on age, education, and culture settings.
- **Source Transparency:** Shows where the ideas came from (no "mystical AI says so" black box).
- **Extensible Backend:** Fine-tune or swap models, add new datasets, build new personas.
- **Single Page UI:** Click, type, reflect.

A little preview before I get to host this ;)
  <img width="1721" height="913" alt="Screenshot 2025-08-13 001718" src="https://github.com/user-attachments/assets/49320c42-8408-4054-92d3-8b0f357fe3ed" />


## Project Structure

```
dharmic-intel/
├─ backend/
│  ├─ app.py              # Flask API
│  ├─ ingest.py           # Build FAISS index from dataset
│  ├─ utils.py            # Helper functions
│  ├─ fine_tune.py        # Optional fine-tuning script
│  └─ requirements.txt
├─ frontend/
│  ├─ index.html          # UI layout
│  ├─ styles.css
│  └─ main.js
├─ dataset/
│  └─ mahabharata.txt     # Your dataset (not included)
└─ README.md
```

## Quick Start

### 1. Install dependencies

```bash
python -m venv venv
source venv/bin/activate      # Windows: .\venv\Scripts\activate
pip install -r backend/requirements.txt
```

### 2. Add your dataset

Place your Mahābhārata .txt file inside:

```bash
dataset/mahabharata.txt
```

### 3. Build embeddings & FAISS index

```bash
python backend/ingest.py
```

### 4. Run the server

```bash
python backend/app.py
```

Then open http://127.0.0.1:7860 in your browser.

## Troubleshooting

- **"Index not found"**: Run `ingest.py` before starting the server.
- **CORS issues**: Always open via Flask's server, not directly from file explorer.
- **Slow embeddings**: Consider a GPU or a smaller model.

## Example Query & Response

**User Query:** "My boss is asking me to lie to a client about project delays. What should I do?"

**Platform Response:** 
> In the Kurukshetra war, when Yudhishthira was asked to speak an untruth to help defeat Drona, he chose a middle path - speaking words that were technically true but allowed for misinterpretation. Consider whether there are ways to communicate the situation to your client that maintain honesty while being diplomatic about timelines and challenges...

*Source: Drona Parva, Chapter 164*

## Contributing

Contributions welcome! If you can make it faster, wiser, or more entertaining, open a pull request. Just… don't ask Duryodhana to do the code review.

## Disclaimer

This project is for educational and interpretive purposes only. It does not provide official moral, legal, or spiritual advice — although it might occasionally sound like your relatives giving life lessons.


## Acknowledgments

- The timeless wisdom of Vyasa and the Mahābhārata
- The open-source community for the tools that made this possible
- Anyone brave enough to seek ancient wisdom for modern problems
