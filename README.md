# rasasupportbot

### Create a virtual environment and install dependencies

`python3 -m venv venv`

`source venv/bin/activate` (Linux/UNIX)

`venv\Scripts\activate` (Windows)

`pip install -r requirements.txt`

### Train model
`python3 -m rasa train`

### Run rasa in terminal
`python3 -m rasa shell`

### Train rasa with examples while running it on terminal
`python3 -m rasa interactive`

### Run RASA on web (needs to be updated, use shell/interactive in the meantime)
`python3 -m rasa run --enable-api --cors="*"`
Clone bizdamn/priya and run the following command in the directory - 
`npm install`
`npm start`

## How to add data to dataset

### Add intent examples to `data/nlu.yml`
```yml
- intent: new_intent_name
  examples: |
    - some intent examples
    - make sure the examples help train the AI
    - and has all necessary keywords as well as variations of the keywords
    - minimum 5 examples are recommended
    - these examples all correspond to the same intent and will be mapped to a particular response so kindly do not club various examples together.
```
### Add intent name and response to `domain.yml`
```yml
intents:
  - existing_intent_name
  - new_intent_name
  .
  .
  .
responses:
  utter_new_intent_name:
  - text: "The response to new_intent_name"
  - image: "https://image.com/image.png" # optional
```

### Add rules to `data/rules.yml` to map the intent and response
```yml
- rule: Do action when asked about intent
  steps:
  - intent: new_intent_name
    action: utter_new_intent_name
  ```

## TODO
- [x] Add frontend
- [ ] Update Frontend for Pi
- [ ] Add voice support (speech synthesis and speech recognition)
- [ ] Increase dataset (and add buttons and slots/entities)
- [x] Add a fallback intent.
- [ ] Add university map.
- [ ] Look into better STT and TTS.
- [x] Connect Mic and Speakers
- [ ] Give the Pi a body
- [ ] Add the frontend code to this repository

### Optional/Future Work:

- [ ] Wake word
- [ ] Interface with mouth movements and face (refer something like UwU)
- [ ] Design 3d printed body


## Known bugs/Issues
- [ ] Does not work on Safari (M1 Mac)

