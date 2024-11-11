# Requests, JSON, and basic NLP with spaCy

# virtual environment
python -m venv Mod4venv
Mod4venv\Scripts\activate

# git commit
git add .
git commit -m ""
git push origin master (main did not work)

# Spacy import error
1. Go to the `pyvenv.cfg` file in the Virtual environment folder
2. Set the `include-system-site-packages` to `true` and save the change
3. Reactivate the virtual environment.

# imports
python -m pip install requests
python -m pip install spacy
python -m pip install spacytextblob

# Generate access token
https://genius.com/api-clients
# in the terminal
set GENIUS_ACCESS_TOKEN=gsjIgmpSiTLvwgKM-466TRtbJ-PTjYy8JXLGpilayE4XzdW-8gC8O3B24nnPdxeb

# import lyrics
pip install lyricsgenius
import lyrics genius
genius = lyricsgenius.Genius("gsjIgmpSiTLvwgKM-466TRtbJ-PTjYy8JXLGpilayE4XzdW-8gC8O3B24nnPdxeb")
artist = genius.search_artist("Vincent Lima", max_songs=3, sort="title")
print(artist.songs)

    # search for a single song
    song = artist.song("To You")
    song = genius.search_song("To You", artist.name)
    #save the artist's songs to aJSON file
    artist.save_lyrics()
# search and save lyrics to a specific song or an album
python3 -m lyricsgenius song "Orpheus" "Vincent Lima" --save
python3 -m lyricsgenius album "The Party" "Andy Shauf" --save


Complete the tasks in the Python Notebook in this repository.
To be submitted for credit, all changes must be committed and pushed to this repository (do not create your own repository unless instructed to on the course website).

## Rubric

* (Question 1) Lyrics printed: 1 pt

* (Question 1) File created and submitted with notebook: 1 pt


* (Question 2) Correct polarity reported: 1 pt


* (Question 2) Question answered thoughtfully: 1 pt





* (Question 3) Function defined as specified: 1 pt
def get_lyrics_and_save(artist_name, song_title, filename):
    """
    Fetches the lyrics of a song by an artist using the Genius API and saves them to a specified file.
    
    Parameters:
    artist_name (str): The name of the artist.
    song_title (str): The title of the song.
    filename (str): The name of the file to save the lyrics.
    """

* (Question 3) Song lyrics retrieved and stored in separate files (0.5 pts/song): 2 pts



* (Question 4) Polarity scores printed (with appropriate label containing song title, .25 pts/song): 1 pt

import spacy
from spacytextblob.spacytextblob import SpacyTextBlob

# Load spaCy and add the spaCyTextBlob pipeline
nlp = spacy.load("en_core_web_sm")
nlp.add_pipe("spacytextblob")

def analyze_sentiment(filename):
    """
    Reads song lyrics from a file, performs sentiment analysis, and returns the polarity score.
    
    Parameters:
    filename (str): The name of the file containing the song lyrics.
    
    Returns:
    tuple: The polarity score and the filename (for identification).
    
    """
* (Question 4) Questions answered thoughtfully: 2 pts
