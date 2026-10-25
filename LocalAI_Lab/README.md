# FSTT Local AI Assistant

A fully local assistant: Flask web interface → Ollama → local LLM, with a keyword (TF-IDF) retriever over `documents/`,
conversation history, structured (JSON) answers and the response time.

## Setup
```bash
ollama pull qwen3.5:9b
pip install flask requests psutil pandas
```

## Run
```bash
cd source
python app.py            # http://127.0.0.1:5001
python chatbot.py        # console chatbot
python benchmark.py qwen3.5:9b gemma3:4b
```
Environment variables: `MODEL`, `OLLAMA_URL`, `PORT`.
