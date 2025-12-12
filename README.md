# From Semantic Similarity to Generative Curation: LLM-Based Music Recommendation

Aadhi Aravind, Aidan Sakuma, Irene Nguyen

## Project Overview
This repository hosts the code for **"From Semantic Similarity to Generative Curation,"** a project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a **Generative Retrieval** framework where an LLM directly generates the identifiers of recommended songs. project exploring the use of Large Language Models (LLMs) for next-generation music recommendation. Unlike traditional matrix factorization or embedding-based retrieval, we implement a Generative Retrieval framework where an LLM directly generates the identifiers of recommended songs.

## File: `final.ipynb` 
This notebook is our main code that works and shows all of our results.

## File : `spotifyplaylist.csv`
Full csv file with all of our playlists.

## EVERYTHING BELOW ARE ITERATIONS IN OUR PROCESS AND NOT FINAL CODE, WE WANTED TO INCLUDE THEM SO THE EFFORTS DONT GO TO WASTE.

## File: `llamasmallercsvworkingversion.ipynb`
This notebook runs LLama on a smaller version of the .csv file, and was an iteration in our process.

## File: `NLP-SFT_DPO.ipynb`
This notebook implements a generative recommendation pipeline that fine-tunes Llama-3 to predict discrete "Semantic IDs" aligned with implicit user feedback mined from listening history logs.

