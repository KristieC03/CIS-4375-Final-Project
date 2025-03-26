Need to create your own creds file in backend since we shouldn't push pwords and db links to public:
    1. create creds.py under backend
    2. paste in file(not sure what info is yet so left blank):
class Creds:
    host = ''
    user = ''
    passwd = ''
    dbname = ''

Backend setup:
    1. cd backend
    2. Mac:
        python3 -m venv venv
        source venv/bin/activate
    2. Windows:
        python -m venv venv
        venv\Scripts\activate
    3. pip install -r requirements.txt
    4. create file named .gitignore and paste, prevents cache/env folders and sensitive files from being pushed:
        venv/
        __pycache__/
        *.pyc
        creds.py

Push to backend branch:
    1. Switch to backend branch:
        git checkout backend
    2. add specific folders:
        git add backend/
       or all:
        git add .
    3. Commit:
        git commit -m "Comments"
    4. Push:
        git push origin backend


Run:
    1. python main.py or python3 main.py


