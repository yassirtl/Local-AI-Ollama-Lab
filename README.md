# Lab: Local AI with Ollama

PhD lab on running and developing local AI applications with Ollama and Python.

## Files
| Path | Description |
|---|---|
| `LAB_Local_AI_Ollama.ipynb` | Lab notebook (Parts 1 to 19) |
| `image.jpg` | Test image for the vision part (Part 14) |

The notebook creates the other files when it runs (`documents/`, `rag.py`, `benchmark.py`, the Flask apps and the `LocalAI_Lab/` folder).

## Models
| Role | Model |
|---|---|
| Model 1 | `qwen3.5:9b` |
| Model 2 and vision | `gemma3:4b` |
| Embeddings | `nomic-embed-text` |

## How to run
Open `LAB_Local_AI_Ollama.ipynb` in Google Colab with a GPU runtime (T4) and run the cells in order. The first cells install Ollama and start the server.

On your own computer, install Ollama from <https://ollama.com/download> and run the notebook with Jupyter.
