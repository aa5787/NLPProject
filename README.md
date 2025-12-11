# From Semantic Similarity to Generative Curation: LLM-Based Music Recommendation

## Project Overview
This repository hosts the code for **"From Semantic Similarity to Generative Curation,"** a project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a **Generative Retrieval** framework where an LLM directly generates the identifiers of recommended songs. project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a Generative Retrieval framework where an LLM directly generates the identifiers of recommended songs.

## File: `NLP-SFT_DPO.ipynb`
**Purpose:** This notebook contains the end-to-end experimental pipeline for the Llama-3 based generative recommender system. It handles the full lifecycle from raw audio feature processing to reinforcement learning alignment.

**Key Stages:**
1.  **Semantic Tokenization (RVQ):**
    * Loads the Spotify Tracks dataset.
    * Trains a Residual Vector Quantizer (RVQ) to compress 10 continuous audio features into a sequence of 3 discrete integers (Semantic IDs), effectively tokenizing the music catalog.

2.  **SFT Data Generation:**
    * Constructs synthetic instructions (e.g., *"I need music for a rock playlist"*) and maps them to the target Semantic IDs.
    * Fine-tunes the **Meta-Llama-3.2-1B** model using LoRA to learn this translation task.

3.  **Preference Dataset Construction (Mining Interaction Logs):**
    * Ingests the **Music4All** listening history dataset (20M+ logs).
    * Calculates "dwell time" to infer implicit user feedback. Tracks listened to for >90s are labeled **Chosen**, while those skipped in <30s are labeled **Rejected**.
    * Constructs over 89,000 preference pairs `(Instruction, Chosen_ID, Rejected_ID)` for alignment training.

4.  **Direct Preference Optimization (DPO):**
    * Loads the SFT-adapted weights.
    * Further fine-tunes the model using the DPO objective to maximize the margin between chosen and rejected songs, aligning the model with realistic user listening habits.

5.  **Evaluation:**
    * Implements ranking metrics (Hit Rate@K, NDCG@K) and hallucination checks to benchmark the generative model against traditional baselines.
