# From Semantic Similarity to Generative Curation: LLM-Based Music Recommendation

## Project Overview
This repository hosts the code for **"From Semantic Similarity to Generative Curation,"** a project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a **Generative Retrieval** framework where an LLM directly generates the identifiers of recommended songs. project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a Generative Retrieval framework where an LLM directly generates the identifiers of recommended songs.

## File: `NLP-SFT_DPO.ipynb`
This notebook implements a generative recommendation pipeline that fine-tunes Llama-3 to predict discrete "Semantic IDs" aligned with implicit user feedback mined from listening history logs.
