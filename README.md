# niksms-python
<p>Niksms API Client Writen In python</p>

## Installation
<p>You can install 'request' package from pypi using  below command:</p>

```python
pip install requests
```

<p>You need to have an active account in <a href='https://niksms.com'>NikSmsWebsite</a></p>

## Usage
<p>You can Send Single Sms using below Code</p>

```python
import requests 

URL = "http://niksms.com/api/SingleSms"

apiKey = "Your ApiKey"
message = "Yout Text Message To Send"
senderNumber = "" # Your private line to send SMS Or Niksms public Line

PARAMS = {'apiKey': apiKey, 'message': message, 'senderNumber': senderNumber,} 

r = requests.get(url = URL, params = PARAMS) 
data = r.json() 



```
