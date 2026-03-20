# CSV to SQL Database automation using Python and SQLite

A Python project that **automates** the parsing of a CSV music library and loads it into a structured **SQLite relational database** with a normalised schema — eliminating manual data entry and making the dataset instantly queryable with SQL.

**Tools:** Python · SQLite · sqlite3

---

## What it does

- Automatically reads and parses track data from `tracks.csv`
- Automates the creation of a normalised database with four related tables: `Artist`, `Genre`, `Album`, and `Track`
- Automates record insertion using foreign key relationships — no duplicates, no manual work

## CSV Format

The `tracks.csv` file must follow this column order:

```
track_name, artist, album, play_count, rating, length_ms, genre
```

Example:
```
Another One Bites The Dust,Queen,Greatest Hits,55,100,217103,Rock
Black Dog,Led Zeppelin,IV,109,100,296620,Rock
```
## Schema

<img width="1200" height="780" alt="image" src="https://github.com/user-attachments/assets/338bbc34-3add-479c-a3c0-399b0f09a609" />

## How to Run

1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/DB_Tracks.git
cd DB_Tracks
```

2. Make sure `tracks.csv` is in the same folder as `DB_Tracks.py`

3. Run the script
```bash
python DB_Tracks.py
```

4. The script will create `DB_Tracks.sqlite` and print the first 10 tracks:
```
Another One Bites The Dust | Queen | Greatest Hits | Rock
Black Dog | Led Zeppelin | IV | Rock

```

## Project Structure

```
DB_Tracks/
├── DB_Tracks.py       # Main script
├── tracks.csv         # Source data
├── requirements.txt   # Dependencies
└── README.md
```

> `DB_Tracks.sqlite` is generated automatically when the script runs.

## Requirements

- Python 3.x
- No external libraries required — `sqlite3` is part of the Python standard library
