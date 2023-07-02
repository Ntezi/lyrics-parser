# Hymnes et Cantiques Kinyarwanda Lyrics Parser

This Python script is designed to convert the lyrics of hymns and canticles from the Kinyarwanda version into a structured JSON format. The script reads the lyrics from a text file, extracts the information for each song, and then writes the information to a JSON file.

## Input

The input to the script is a text file (`lyrics.txt`) that contains the lyrics for the hymns and canticles. Each song is separated by two blank lines. The first line of each song contains the song number, title, and subtitle (in parentheses), separated by spaces. The subtitle can be "(Indimbo)" or a different category. Each verse of the song is separated by a blank line.

Example:
```
1. TURAGUSINGIZA DATA (N’icyubahiro)

Verse 1...

Verse 2...

2. DUTERE INDIRIMBO NZIZA (N’icyubahiro)

Verse 1...

Verse 2...
```

## Output

The output of the script is a JSON file (`songs.json`) that contains an array of song objects. Each song object has the following properties:
- `song_number`: the number of the song
- `title`: the title of the song
- `sub_title`: the subtitle of the song (empty if the subtitle is "(Indimbo)")
- `verses`: an array of verses for the song

Example:
```json
[
    {
        "song_number": 1,
        "title": "TURAGUSINGIZA DATA",
        "sub_title": "(N’icyubahiro)",
        "verses": ["Verse 1...", "Verse 2..."]
    },
    {
        "song_number": 2,
        "title": "DUTERE INDIRIMBO NZIZA",
        "sub_title": "(N’icyubahiro)",
        "verses": ["Verse 1...", "Verse 2..."]
    }
]
```