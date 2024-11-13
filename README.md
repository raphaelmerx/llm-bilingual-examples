# Generating bilingual example sentences with large language models as lexicography assistants

Paper: https://arxiv.org/abs/2410.03182

## Getting started

- Create a Python (3.12) venv, then `pip install -r requirements.txt`
- Get API keys in .env: `cp .env.example .env` and populate your `.env` file (with `OPENAI_API_KEY` and `REPLICATE_API_KEY`)
- Run the notebooks


## Notebooks

### 1. `generate_dict_examples.ipynb`

From a list of candidate words, generate example sentneces using GPT-4o and Llama-3.1-405B.

### 2. `rate_examples.ipynb`

Interpret annotation ratings: inter-annotator agreement, performance per model and per language.

### 3. `pretrained_metrics_corel.ipynb`

Calculate correlations between example GDEX ratings and pre-trained metrics (perplexity, mask probability, entropy).

### 4. `llm_rate_example.ipynb`

Rate an example using an LLM, using 10 previous ratings for in-context learning (ICL), to align the LLM with a specific annotator.


## Data

Annotated examples are in `select_examples_[gpt4,llama]_[fra,ind,tdt]_eng_rated_A[1,2].tsv`