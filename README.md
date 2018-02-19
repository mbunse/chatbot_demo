# chatbot_demo

A chatbot demo based on [rasa-nlu](https://github.com/RasaHQ/rasa_nlu). 

Edit data.json (e.g. with [rasa-nlu-trainer](https://github.com/RasaHQ/rasa-nlu-trainer)).

```
cd ~/rasa-trainer
rasa-nlu-trainer -p 8080 -s ../chatbot/data.json
```
Train the bot:
```
cd ~/chatbot_demo
python -m rasa_nlu.train -c config_spacy.json
```

Run the bot's REST API:
```
cd ~/chatbot_demo
python -m rasa_nlu.server -c config_spacy.json
```

Start the webinterface:
```
cd ~/chatbot_demo
python -m http.server 80
```
