# esg-frontier

## jupyter notebooks
1. `get_tweets/get_tweets.ipynb`: uses twitter api v2 to retrieve tweets data and save them in `get_tweets/` and `get_tweets/tweets_data/` as `.json` files
    - requires twitter api keys
2. `get_tweets/merge_tweets.ipynb`: cleans up and merge tweets data from relevant companies and save it to `data/tweets_dow.csv`
3. `train.ipynb`: uses labeled data to train the nlp model via spacy, trained models are saved to `output/`
4. `tweets.ipynb`: loads trained model to calculate climate-related score for each tweets, then aggregate into monthly scores for each stock

## configuration files
- `conda-env.yml`: create conda environment by `conda env create -f conda-env.yml`
- `config.cfg`: for spacy training pipeline
- `keywords.txt`: climate topic keywords, used to construct non-climate related labels
- `get_tweets/search_*.yaml`: search queries for retrieving tweets in `get_tweets.ipynb`


## csv files
- `data/tickers_dow.csv`, `data/tickers_sp_100.csv`: stocks information
- `climate_score.csv`: constructed monthly score for each stock