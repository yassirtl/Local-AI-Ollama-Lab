# Lab: Local AI with Ollama

PhD lab on running and developing local AI applications with Ollama and Python.

## Files
| Path | Description |
|---|---|
| `LAB_Local_AI_Ollama.ipynb` | Notebook with code, outputs and answers (Parts 1 to 19, Q1 to Q15) |
| `image.jpg` | Test image for the vision part (Part 14) |
| `LocalAI_Lab/report.pdf` | Lab report |
| `LocalAI_Lab/source/` | Final project: Flask app, `chatbot.py`, `rag.py`, `benchmark.py`, HTML template |
| `LocalAI_Lab/documents/` | Course documents used by the retriever |
| `LocalAI_Lab/screenshots/` | Screenshots 01 to 06 (installation, model, chatbot, Python, RAG, web app) |

When it runs, the notebook also creates working files next to it (`documents/`, `rag.py`, `benchmark.py`, the small Flask app of Part 15).

## Models
| Role | Model |
|---|---|
| Model 1 | `qwen3.5:9b` |
| Model 2 and vision | `gemma3:4b` |
| Embeddings | `nomic-embed-text` |

## Results (Colab, T4 GPU)
| Experiment | qwen3.5:9b | gemma3:4b |
|---|---|---|
| Memory on the GPU | 5.61 GB | 2.88 GB |
| Load time (cold start) | 35.8 s | 13.0 s |
| Generation speed | 26.2 tokens/s | 51.6 tokens/s |
| `is_prime` written by the model | correct (tested on -5..19999) | correct (tested on -5..19999) |
| Quality /5 | 5 | 4 |

| Experiment | Result |
|---|---|
| Conversation memory | Works by resending the history; the model itself keeps nothing |
| Structured output (JSON Schema) | Always valid JSON, but the content can still be wrong |
| Document grounding / mini-RAG | Off-topic questions answered with "Information not available." |
| Keyword vs embedding retrieval | Embeddings find the right document when the words differ |
| Vision (gemma3:4b) | Correct description of the test image in 24 s |
| Mini-project | Flask assistant with RAG, history, JSON answers; response times recorded in a CSV file (1.8 s normal answer, 5.8 s JSON answer) |
| Console chatbot (`chatbot.py`) | Remembers the name given in the first message |

## How to run
Open `LAB_Local_AI_Ollama.ipynb` in Google Colab with a GPU runtime (T4) and run the cells in order. The first cells install Ollama and start the server.

On your own computer, install Ollama from <https://ollama.com/download> and run the notebook with Jupyter.
