# Disaster Response Pipeline Project

### File Description:
    .
    ├── app     
    │   ├── run.py                        # Flask file that runs app
    │   └── templates   
    │       ├── go.html                   # Classification result page of web app
    │       └── master.html               # Main page of web app
    |
    ├── data                   
    │   ├── disaster_categories.csv       # Categories Dataset
    │   ├── disaster_messages.csv         # Messages Dataset
    │   ├── process_data.py                 
    │   └── DisasterResponse.db           # database to save clean data to
    |
    ├── models
    │   ├── train_classifier.py            
    │   └── process_data.py               # saved model
    |
    └── README.md


### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`
    - Run `run.py` directly if **DisasterResponse.db** and **claasifier.pkl** already exist.

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
