# Billboard to Spotify Playlist

This Python script allows you to travel back in time and create a Spotify playlist of the Billboard Hot 100 songs for any specified date.

## Features
- Scrapes the **Billboard Hot 100** songs list for a given date.
- Searches for these songs on **Spotify**.
- Creates a **private Spotify playlist** and adds the songs to it automatically.

## Requirements
To run this project, you'll need the following:

1. **Python 3.x**
2. Spotify Developer account and a registered app for API access
3. Environment variables configured for Spotify API credentials

## Setup Instructions

### 1. Clone the repository
```bash
 git clone https://github.com/MostafaHima/Billboard-Hot-100-to-Spotify-Playlist.git
 cd Billboard-Hot-100-to-Spotify-Playlist
```

### 2. Install dependencies
Ensure you have the required Python libraries by running:
```bash
pip install -r requirements.txt
```
**Dependencies**:
- `spotipy`
- `beautifulsoup4`
- `requests`
- `python-dotenv`

### 3. Set up Spotify API Credentials
- Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard).
- Create an app to obtain your **Client ID** and **Client Secret**.
- Add `http://example.com` as the Redirect URI.

Create a `.env` file in your project directory and add the credentials:
```env
CLIENT_ID=your_spotify_client_id
CLIENT_SECRET=your_spotify_client_secret
```

### 4. Run the Script
Run the script in your terminal:
```bash
python main.py
```
When prompted, enter the date in the format `YYYY-MM-DD`:
```
Which year do you want to travel to? Type the date in this format YYYY-MM-DD: 2000-08-12
```

### 5. Spotify Authentication
When running for the first time, a browser window will open asking you to log in to Spotify and authorize access.

## How It Works
1. The script scrapes the Billboard Hot 100 list for the specified date.
2. It searches for each song on Spotify.
3. A private playlist is created with the retrieved songs.
4. Songs are added to the playlist.

## Output
- **Terminal**: Displays the song names and any songs that couldn't be found.
- **Spotify**: A new private playlist with the title `Billboard Hot 100 - YYYY-MM-DD`.

## Example
### Input
```
Which year do you want to travel to? Type the date in this format YYYY-MM-DD: 2000-08-12
```

### Output
```
['Song 1', 'Song 2', 'Song 3', ...]
Song 4 doesn't exist in Spotify. Skipped.
Playlist created: Billboard Hot 100 - 2000-08-12
```

## Notes
- The script only fetches songs available on Spotify.
- Ensure your Spotify app has the required permissions to create playlists (`playlist-modify-private`).

