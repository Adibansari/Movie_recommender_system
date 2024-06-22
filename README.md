# Movie Recommendation System

## Overview
This repository contains code for a movie recommendation system based on content filtering using natural language processing techniques. It preprocesses movie data, extracts features, and uses cosine similarity to recommend movies similar to a given input movie.

## Project Structure
The project structure is as follows:
.

├── preprocessing.ipynb

├── movie_dict.pkl

├── Procfile

├── setup.sh

├── requirements.txt

├── app.py

└── README.md

- `preprocessing.ipynb`: Jupyter notebook containing code for preprocessing movie data and building the recommendation system.
- `movie_dict.pkl`: Pickled file containing movie data in dictionary format.
- `Procfile`: File specifying the commands that are executed by the app on startup.
- `setup.sh`: Shell script to configure Streamlit for deployment.
- `requirements.txt`: File listing required Python packages.
- `app.py`: Streamlit application code for the recommendation system.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Adibansari/Movie_recommender_system
   cd your_project
2. Install the required Python packages:
pip install -r requirements.txt
## Usage

1. **Run the Jupyter notebook `preprocessing.ipynb` to preprocess the movie data and build the recommendation system.**

2. **Execute the cells in the notebook to:**
   - Load and merge movie data (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`).
   - Clean and preprocess the data.
   - Generate tags for each movie based on its overview, genres, keywords, cast, and crew.
   - Implement stemming and vectorization of tags using CountVectorizer.
   - Calculate cosine similarity between movies.
   - Build a function to recommend movies similar to a given input movie.

3. **Save the processed data and models as pickled files:**
   - `movie_dict.pkl`: Movie data in dictionary format.
   - `similarity.pkl`: Cosine similarity matrix.

## Deploying with Streamlit

1. **Create a `Procfile` in the root directory with the following content:**
   ```bash
    web: sh setup.sh && streamlit run app.py

2. **Create or update `setup.sh` with the following content to configure Streamlit:**

   ```bash
    mkdir -p ~/.streamlit/
    echo "\
   [server]\n\
   port = $PORT\n\
   enableCORS = false\n\
   headless = true\n\
   " > ~/.streamlit/config.toml

3. **Update app.py with your Streamlit application code.**
4. **Deploy your app to a platform that supports Streamlit apps, such as Heroku.**
## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Streamlit
- Requests (for fetching movie data from API)

## Contributing
Contributions to the project are welcome! Here's how you can contribute: 
- Fork the repository.
- Create a new branch (git checkout -b feature-branch).
- Make your changes.
- Commit your changes (git commit -am 'Add new feature').
- Push to the branch (git push origin feature-branch).
- Create a new Pull Request.

