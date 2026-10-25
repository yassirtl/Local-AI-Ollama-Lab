# FSTT Local AI Assistant

A fully local assistant: Flask web interface → Ollama → local LLM, with a keyword (TF-IDF) retriever over `documents/`,
conversation history, structured (JSON) answers and the response time.
Each answer is also recorded in `source/response_times.csv` (time, question, seconds, tokens, tokens/s).

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
Environment variables: `MODEL`, `OLLAMA_URL`, `PORT`, `HOST` (default `127.0.0.1`).

## Documents
`ai.txt`, `machine_learning.txt`, `reinforcement_learning.txt` and `deep_learning.txt` are the course files of the mini-RAG
(the deliverable list calls the last ones `ml.txt` and `rl.txt`; the lab code creates them with the long names).
`course.txt` is the short course file of Part 12.
