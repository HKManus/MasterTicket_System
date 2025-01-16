# MasterTicket System

![Screenshot](/READMEFILE/header_image.png)

The MasterTicket System is a part of the [MasterTicket Project](https://github.com/HKManus/MasterTicket_Project)


## Getting Started
1. create a [Firebase](https://firebase.google.com/) Realtime Database

2. enable firebase update
   - go to realtime database > rule
   - set the rule as following
    ```json
    {
      "rules": {
        ".read": true,
        ".write": true
      }
    }
    ```
3. get a service account key, rename it as `serviceAccountKey.json`, and put it in the same directory of `app.py`

> To generate a service account key:
> 
> 1. In the Firebase console, open Settings > Service Accounts.
> 2. Click Generate New Private Key, then confirm by clicking Generate Key.
> 3. Securely store the JSON file containing the key.
> 
> src: https://firebase.google.com/docs/admin/setup

4. Obtain the databaseURL of your Realtime Database, and add it into `edit_firebase.py` (replace `your_databaseURL`)


![Screenshot](/READMEFILE/databaseURL.jpg)

```python
def firebase_init():
    cred = credentials.Certificate("serviceAccountKey.json")
    fb.initialize_app(cred, {
        "databaseURL": "your_databaseURL" # replace me
    })
```

5. run app.py
6. connect to the url shown in th terminal
   example of terminal message: ` * Running on http://127.0.0.1:5000`


## Usage

![Screenshot](/READMEFILE/interface.jpg)

