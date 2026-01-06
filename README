inat2ebird
==========

Convert iNaturalist bird observations into an eBird Record Format CSV for upload.

Setup
-----
1) Install dependencies:
   `python3 -m pip install -r requirements.txt`
2) Set your eBird API key (used to infer country/region from coordinates):
   `export EBIRD_API_KEY=your_key_here` (get one at https://ebird.org/api/keygen)

Choose a path (no required order)
---------------------------------
Single observation -> `observation2ebird.py`
- Input: iNaturalist observation ID
- Output: `items.csv` (one row in eBird Record Format)
- Run: `python observation2ebird.py 123456`

User life list -> `user2ebird.py`
- Input: iNaturalist user ID
- Input file: `ebird_world_life_list.csv` downloaded from https://ebird.org/lifelist?time=life&r=world
- Output: `all_bird_entries_<user_id>.csv`
- Run: `python user2ebird.py 12345`

Web form -> `app.py`
- Input: user ID + eBird life list CSV upload
- Output: CSV saved in `uploads/` with a download link
- Run: `python app.py` and open http://127.0.0.1:5000

Notes
-----
- eBird checklists must be a single date and a single location. These scripts create one row per observation in Record Format.
- `user2ebird.py` currently fetches only the first page (200) of research-grade bird observations from iNaturalist.
- `ebird_record_format_template.csv` is included as a reference for the required columns.

Upload
------
Upload your CSV at https://ebird.org/import/upload.form?theme=ebird
