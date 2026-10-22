# Movie Recommendation System

A Streamlit recommendation application that suggests movies using precomputed similarity data and displays poster artwork from The Movie Database API.

## Recommendation flow

1. Load the serialized movie catalogue and similarity matrix.
2. Select a movie from the Streamlit dropdown.
3. Find the nearest items in the similarity space.
4. Display five recommendations and their poster images.

## Technology

Python · Pandas · Streamlit · Requests · pickle-based model artifacts · TMDB API

## Run locally

```bash
pip install streamlit pandas requests
streamlit run app.py
```

The app expects the serialized movie data and similarity artifacts referenced by `app.py`. Configure the TMDB API key through an environment variable before sharing or deploying the app; never commit API keys.

## Evaluation ideas

For a stronger production system, compare content-based and collaborative filtering baselines, measure ranking quality with precision@k/recall@k, handle cold-start users, and cache poster requests.
