# From Semantic Similarity to Generative Curation: LLM-Based Music Recommendation

## Project Overview
This repository hosts the code for **"From Semantic Similarity to Generative Curation,"** a project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a **Generative Retrieval** framework where an LLM directly generates the identifiers of recommended songs. project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a Generative Retrieval framework where an LLM directly generates the identifiers of recommended songs.

## File: `NLP-SFT_DPO.ipynb`
This notebook implements a generative recommendation pipeline that fine-tunes a Llama-3 model to predict discrete "Semantic IDs" derived from audio features. It contains the workflow from data processing to evaluation, utilizing Supervised Fine-Tuning (SFT) followed by Direct Preference Optimization (DPO) to align recommendations with implicit user feedback mined from listening history logs.
