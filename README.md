# My LLM Notebooks

My personal notebook collection for learning how large language models work, built up chapter by chapter: tokens and embeddings, classification, clustering, prompting, RAG, multimodal models and fine-tuning. Everything here is code I ran, changed and debugged myself while studying, and I keep it as a reference to come back to.

## What's inside

| # | Notebook | What I practice there |
|---|----------|-----------------------|
| 01 | [Introduction to language models](01-introduction-to-language-models/01-introduction-to-language-models.ipynb) | Loading a model and generating text |
| 02 | [Tokens and embeddings](02-tokens-and-embeddings/02-tokens-and-embeddings.ipynb) | Tokenizers, token embeddings, word2vec-style embeddings |
| 03 | [Inside transformer LLMs](03-inside-transformer-llms/03-inside-transformer-llms.ipynb) | What happens inside a generative transformer |
| 04 | [Text classification](04-text-classification/04-text-classification.ipynb) | Classification with representation and generative models |
| 05 | [Clustering and topic modeling](05-clustering-and-topic-modeling/05-clustering-and-topic-modeling.ipynb) | Document clustering and BERTopic |
| 06 | [Prompt engineering](06-prompt-engineering/06-prompt-engineering.ipynb) | Prompting techniques and output control |
| 07 | [Advanced text generation](07-advanced-text-generation/07-advanced-text-generation.ipynb) | Chains, memory and agents with LangChain |
| 08 | [Semantic search and RAG](08-semantic-search-and-rag/08-semantic-search-and-rag.ipynb) | Dense retrieval, reranking, retrieval-augmented generation |
| 09 | [Multimodal LLMs](09-multimodal-llms/09-multimodal-llms.ipynb) | Vision-language models |
| 10 | [Training embedding models](10-training-embedding-models/10-training-embedding-models.ipynb) | Creating and fine-tuning text embedding models |
| 11 | [Fine-tuning BERT](11-finetuning-bert/11-finetuning-bert.ipynb) | Fine-tuning representation models for classification |
| 12 | [Fine-tuning generation models](12-finetuning-generation-models/12-finetuning-generation-models.ipynb) | Parameter-efficient fine-tuning of generative LLMs |

## Running them

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
python -m venv .venv && source .venv/bin/activate
pip install jupyterlab
jupyter lab
```

Each notebook begins with a commented-out `pip install` cell with the exact package versions I used. I uncomment it for whichever notebook I'm working on instead of installing everything at once.

## Hardware

I run most of these on a free Colab T4 GPU. Notebooks 10 to 12 (training and fine-tuning) are the heaviest.

## API keys

A few notebooks call hosted APIs (OpenAI in 04 to 07, Cohere in 08). I keep keys in environment variables and never in the notebooks or in git:

```bash
export OPENAI_API_KEY="..."
export COHERE_API_KEY="..."
```

`.env` files are in `.gitignore`.
