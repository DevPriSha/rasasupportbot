# rasasupportbot

### Create a virtual environment
Make sure python is python 3.8
`python3 -m venv venv`
`source venv/bin/activate` (Linux/UNIX)
`venv\Scripts\activate` (Windows)
`pip install rasa=3.0`

**Note:** M1 Mac users install Rasa by following this guide - https://forum.rasa.com/t/an-unofficial-guide-to-installing-rasa-on-an-m1-macbook/51342

### Train model
`rasa train`

### Run rasa in terminal
`rasa shell`

### Run RASA on web (tested only on M1 mac chrome)
`rasa run --enable-api --cors="*"`
Open `index.html` in your browser.

## TODO
- [x] Add frontend
- [ ] Add voice support (speech synthesis and speech recognition)
- [ ] Increase dataset (and add buttons and slots/entities)
- [x] Add a fallback intent.

## Known bugs/Issues
- [ ] Does not work on Safari (M1 Mac)

