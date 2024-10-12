# Spotify Music Recommender System

This project implements a content-based music recommendation system using Spotify data. It utilizes various techniques to provide personalized song recommendations based on user preferences and listening history. Note that the notebook needs to be restructured and organized; the notebook usage is meant to ease experimentation. In the future, this code will be transferred to a better structured coding project.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Algorithms](#algorithms)

## Features

- Content-based filtering for song recommendations
- Time-aware recommendations with recency bias
- Integration with Spotify API for playlist creation
- Support for various audio features and metadata
- Customizable recommendation parameters

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/spotify-recommender.git
   cd spotify-recommender
   ```

2. Create a virtual environment:
   ```
   python -m venv recommenderVar
   source recommenderVar/bin/activate  # On Windows, use `recommenderVar\Scripts\activate`
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Set up your Spotify API credentials:
   - Create a `.env` file in the project root
   - Add your Spotify API credentials:
     ```
     SPOTIPY_CLIENT_ID=your_client_id
     SPOTIPY_CLIENT_SECRET=your_client_secret
     SPOTIPY_REDIRECT_URI=your_redirect_uri
     ```

## Usage

1. Prepare your dataset:
   - Ensure you have the Spotify dataset CSV file in the `data/` directory.

2. Run the Jupyter notebook:
   ```
   jupyter notebook recommender.ipynb
   ```

3. Follow the notebook cells to:
   - Load and preprocess the data
   - Create feature sets
   - Generate recommendations
   - Create playlists based on recommendations

## Project Structure

- `recommender.ipynb`: Main Jupyter notebook containing the recommendation system code
- `requirements.txt`: List of Python package dependencies
- `data/`: Directory for storing the Spotify dataset (not included in the repository)
- `.env`: File for storing Spotify API credentials (not included in the repository)
- `.gitignore`: Specifies intentionally untracked files to ignore

## Algorithms

The project uses the following main algorithms and techniques:

1. Content-Based Filtering: Recommends songs based on their similarity to items the user has interacted with in the past.
2. Time-Aware Recommendations: Incorporates recency bias using an exponential decay function.
3. Cosine Similarity: Measures the similarity between user playlists and potential recommendations.
4. TF-IDF (Term Frequency-Inverse Document Frequency): Used for processing genre information.

For more details on the algorithms, refer to the relevant sections in the `recommender.ipynb` notebook.