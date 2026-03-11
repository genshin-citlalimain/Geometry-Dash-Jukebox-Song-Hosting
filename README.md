# Geometry Dash Jukebox Song Library

Welcome! This repository hosts MP3s ready to use with the Jukebox mod in Geometry Dash. All songs are streamed directly from GitHub via jsDelivr, so you don’t need to download anything—just point Jukebox to this library.

## Table of Contents

- [Using the Library](#using-the-library)
- [Adding Your Own Songs](#adding-your-own-songs)
- [Folder Structure](#folder-structure)
- [JSON Example](#json-example)
- [Tips & Notes](#tips--notes)

## Using the Library

1. Install the **Jukebox mod** in Geometry Dash.
2. Open Jukebox and find the option to **add a hosted song library**.
3. Paste the following link:

https://cdn.jsdelivr.net/gh/genshin-citlalimain/Geometry-Dash-Jukebox-Song-Hosting/index.json

4. All the songs in this repository will now appear in Jukebox, ready to play.
> ✅ Tip: These songs stream from the internet. Make sure you have a stable connection.

## Adding Your Own Songs

If you want to add your own MP3s, you’ll need to update the `index.json` file manually. Here’s how:

1. **Add your MP3**
   - Put the MP3 in the `songs/` folder of the repository.
   - Make sure the filename uses only letters, numbers, underscores `_`, or hyphens `-`. No spaces.

2. **Add a new JSON entry**
   - Open `index.json` in a text editor (VS Code, Notepad++, or GitHub web editor).
   - Copy one of the existing entries and modify it:
```
{
"name": "Song Name Here",
"artist": "Artist Name Here",
"songs": [10],
"source": "host",
"url": "https://cdn.jsdelivr.net/gh/yourusername/Geometry-Dash-Jukebox-Song-Hosting/songs/your_song_file.mp3
"
}
```

3. **Save and push**
   - Commit the changes and push them to GitHub.
   - Jukebox will now see your new song in the library.

> ⚠️ Important: Jukebox does **not** let you add hosted songs directly in-game. The JSON file is the only way to make new songs available.

## Folder Structure

```Geometry-Dash-Jukebox-Song-Hosting/
├─ songs/          # MP3 files go here
│   ├─ aa_kenran_no_yume.mp3
│   ├─ amazing_mirage.mp3
│   └─ ...etc
└─ index.json      # Lists all songs with URLs for Jukebox
```

- Make sure the paths in `index.json` match the `songs/` folder exactly.
- Filenames in the JSON must match the MP3 filenames.

## JSON Example

Here’s an example entry from `index.json`:
```
{
"name": "Amazing Mirage",
"artist": "lapix",
"songs": [2],
"source": "host",
"url": "https://cdn.jsdelivr.net/gh/genshin-citlalimain/Geometry-Dash-Jukebox-Song-Hosting/songs/amazing_mirage.mp3
"
}
```
- You can copy and edit this for your own songs.
- Keep the JSON format valid—every entry should be separated by a comma, and the last entry should **not** have a trailing comma.

## Tips & Notes

- Use descriptive filenames like `song_title.mp3` to avoid confusion.
- GitHub + jsDelivr handles the hosting, so you don’t need to upload files anywhere else.
- For large libraries, keep track of the `songs` numbers to avoid duplicates.
- Test your new songs in a browser first by pasting the URL—if it plays there, Jukebox can stream it.
