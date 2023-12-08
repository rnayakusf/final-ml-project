# Song recommendations from facial recognition (TuneQuest)

## Dataset sources
* [Smaller Spotify set with moods](https://www.kaggle.com/datasets/musicblogger/spotify-music-data-to-identify-the-moods)
* [Larger spotify set without moods](https://www.kaggle.com/datasets/vatsalmavani/spotify-dataset/data)
* [Image set](https://www.kaggle.com/datasets/jonathanoheix/face-expression-recognition-dataset)

The datasets are already in the repository.

## Model training instructions
For dependencies, run `pip install -r requirements.txt`

Running the `emotionrecognitiontrainer.ipynb` notebook will generate the model. This can take some time on a CPU.

## Song moods
Running the `songmoods.ipynb` notebook will use XGBoost to find the moods of the larger Spotify dataset.

## Running the facial recognition software
Before running `emotionrecognition.py`, you need to generate a Spotify API key from developers.spotify.com. For the redirect URI, use `http://localhost`.

Next, run:
```
EXPORT SPOTIPY_CLIENT_ID=<client-id>
EXPORT SPOTIPY_SECRET_ID=<secret-id>
EXPORT SPOTIPY_REDIRECT_URI=http://localhost
```
in the terminal.

Then you can run `python emotionrecognition.py` and generate your playlist (you will be prompted to link your Spotify account). To register your face, press the ESC key.