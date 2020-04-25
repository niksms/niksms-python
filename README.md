# niksms-python
<p>Niksms API Client Writen In python</p>

## Installation
<p>Install Below code : </p>

```python
pip install requests
```

## Usage
<p>You can Send Sms using below Code</p>

```python
import requests 

URL = "http://niksms.com/api/SingleSms"

apiKey = "Your ApiKey"
message = "Yout Text Message To Send"
PARAMS = {'apiKey': apiKey, 'message': message} 

r = requests.get(url = URL, params = PARAMS) 
data = r.json() 

latitude = data['results'][0]['geometry']['location']['lat'] 
longitude = data['results'][0]['geometry']['location']['lng'] 
formatted_address = data['results'][0]['formatted_address']

```
