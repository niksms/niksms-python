# niksms-python
<p>Niksms API Client Writen In python</p>

<p>You need to have an active account in <a target='_blank' href='https://niksms.com'>NikSms Website</a></p>

## Installation
<p>You can install 'requests' package from pypi using  below command:</p>

```python
pip install requests
```
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
