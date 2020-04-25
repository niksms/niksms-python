# niksms-python
<p>Niksms API Client Writen In python</p>

## Installation
<p>Install Below code : </p>

```
pip install requests
```

## Usage
<p>You can Send Sms using below Code</p>

```
import requests 

URL = "http://maps.googleapis.com/maps/api/geocode/json"

location = "delhi technological university"
PARAMS = {'address':location} 

r = requests.get(url = URL, params = PARAMS) 
data = r.json() 
# Comment
latitude = data['results'][0]['geometry']['location']['lat'] 
longitude = data['results'][0]['geometry']['location']['lng'] 
formatted_address = data['results'][0]['formatted_address']

```
