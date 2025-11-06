# Automashup_Mashup_Eval

## Project summary

This repository explores automated mashup creation and ways to measure the "proximity" between a vocal and an instrumental track so we can pick compatible pairs for mashups. The original work experimented with CoCoLa (a contrastive audio model). To reduce resource needs we experimented with lighter alternatives — notably CLAP and MERT embeddings with cosine similarity — and documented that workflow here.

This README summarizes the goal, what was tried (CLAP + MERT + cosine similarity), where to find code/notebooks, quick usage notes, and suggested next steps for evaluation and automation.

## What we tried (current state)

- CoCoLa: powerful contrastive scores used in earlier experiments (see `Code/cocola.ipynb` and `Code/cocola_scores_calculation.py`). Heavy to run (GPU + checkpoint).
- CLAP/MERT + cosine similarity: lighter alternative tried in this project. Extract embeddings (CLAP or MERT) per track, optionally average or pool over time/segments, then compute cosine similarity between vocal and instrumental embeddings. 

## Files and notebooks

- `Code/AutoMashup_Notebook.ipynb` — high-level mashup pipeline and utilities.
- `Code/cocola.ipynb` and `Code/cocola_scores_calculation.py` — CoCoLa extraction and scoring (heavy workflow).
- `Code/Embeddings_generation_CLAP_MERT.ipynb` — notebooks and notes for extracting CLAP and MERT embeddings (where the lightweight experiments live).
- `Code/Mashups_creation.ipynb`, `Code/songs_selection.ipynb` — mashup-building and selection helper notebooks.

If you want to reproduce the CLAP/MERT + cosine workflow, check `Code/Embeddings_generation_CLAP_MERT.ipynb` for extraction steps and where embeddings are written.


