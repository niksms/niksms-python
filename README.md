# niksms-python
<p>Niksms API Client Writen In python</p>

<p>You need to have an active account in <a target='_blank' href='https://niksms.com'>NikSms Website</a></p>

## Installation
<p>You can install 'requests' package from pypi using  below command:</p>

```python
pip install requests
```
## Usage

### Send Single SMS
<p>You can Send Single SMS using below Code</p>

```python
import requests 

URL = "http://niksms.com/SingleSms"

apiKey = "Your ApiKey"
message = "Yout Text Message To Send"
senderNumber = "" # Your private line to send SMS Or Niksms public lines
mobile = "" # reciever phone number

PARAMS = {'apiKey': apiKey, 'message': message, 'senderNumber': senderNumber, 'mobile':mobile} 

r = requests.get(url = URL, params = PARAMS) 
data = r.json() 

if int(data) > 0
    print('SMS Successfully Sent')
else
    print('Can not send Sms')



```


### Send Bulk SMS
<p>You can Send Bulk Sms using below Code</p>

```python
import requests 

URL = "http://niksms.com/GroupSms"

apiKey = "Your ApiKey"
message = "Yout Text Message To Send"
senderNumber = "" # Your private line to send SMS Or Niksms public lines
mobiles = "" # Recievers phone number sepereated by , (comma)

PARAMS = {'apiKey': apiKey, 'message': message, 'senderNumber': senderNumber, 'mobiles': mobiles} 

r = requests.get(url = URL, params = PARAMS) 
data = r.json() 

if int(data) > 0
    print('SMS Successfully Sent')
else
    print('Can not send Sms')



```

### Send point to point SMS
<p>If you want to send different SMS messages to diffrerent numbers in one request you can use PTPsend method.</p>

```python
import requests 

URL = "http://niksms.com/PtpSms"

apiKey = "Your ApiKey"
senderNumber = "" # Your private line to send SMS Or Niksms public lines
mobiles = "" # Recievers phone number sepereated by , (comma)
messages = "" # Messages sepreated by | (vertical bar)

PARAMS = {'apiKey': apiKey, 'senderNumber': senderNumber,'mobiles': mobiles, 'messages': messages } 

r = requests.get(url = URL, params = PARAMS) 
data = r.json() 

if int(data) > 0
    print('SMS Successfully Sent')
else
    print('Can not send Sms')



```


### Get Sender Numbers
<p>If you want to get the list of your private numbers that you use for sending SMS, you can use GetSenderNumbers method.</p>

```python
import requests 

URL = "http://niksms.com/GetSenderNumbers"

apiKey = "Your ApiKey"

PARAMS = {'apiKey': apiKey } 

r = requests.get(url = URL, params = PARAMS) 
listOfNumbers = r.json() 



```

### Get Credit
<p>You can get you credit balance with below code.</p>

```python
import requests 

URL = "http://niksms.com/GetCredit"

apiKey = "Your ApiKey"

PARAMS = {'apiKey': apiKey } 

r = requests.get(url = URL, params = PARAMS) 
yourBalance = r.json() 



```

### Get Expire Date
<p>You can get your account expiration date with below code.</p>

```python
import requests 

URL = "http://niksms.com/GetExpireDate"

apiKey = "Your ApiKey"

PARAMS = {'apiKey': apiKey } 

r = requests.get(url = URL, params = PARAMS) 
expireDate = r.json() 



```


### Get Server time
<p>You can get nik SMS server time using below code.</p>

```python
import requests 

URL = "http://niksms.com/GetServertime"

apiKey = "Your ApiKey"

PARAMS = {'apiKey': apiKey } 

r = requests.get(url = URL, params = PARAMS) 
serverTime = r.json() 



```


### Get SMS Delivery
<p>You can get results of sent messages using below code.</p>

```python
import requests 

URL = "http://niksms.com/GetSmsDelivery"

apiKey = "Your ApiKey"
nikIds = [] # Array of ids related to each SMS that you sent. This Ids has been sent to you as response of sendSingle or group SMS

PARAMS = {'apiKey': apiKey , 'nikIds':nikIds } 

r = requests.get(url = URL, params = PARAMS) 
arrayOfResult = r.json() 

for result in arrayOfResult:
    if result == '3'
        print('sent successfully')
    else if result == '2' or result == '1'
        print('waiting to be sent')
    else
        print('message not sent')

```


### Get SMS Delivery With ClientId
<p>You can get results of sent messages with ids which you used before, using below code.</p>

```python
import requests 

URL = "http://niksms.com/GetSmsDeliveryWithClientId"

apiKey = "Your ApiKey"
yourId = [] # Array of ids related to each SMS that you sent. This Ids are numbers which you used in sending SMS.

PARAMS = {'apiKey': apiKey , 'yourId':yourId } 

r = requests.get(url = URL, params = PARAMS) 
arrayOfResult = r.json() 

for result in arrayOfResult:
    if result == '3'
        print('sent successfully')
    else if result == '2' or result == '1'
        print('waiting to be sent')
    else
        print('message not sent')


```


### Get Received Sms
<p>You can get received SMS to your private line using below code.</p>

```python
import requests 

URL = "http://niksms.com/GetReceivedSms"

apiKey = "Your ApiKey"

PARAMS = {'apiKey': apiKey } 

r = requests.get(url = URL, params = PARAMS) 
arrayOfResult = r.json() 

for result in arrayOfResult:
    print('sender number is: ' + result.SenderNumber)
    print('message is : ' + result.Message)
    print('receive time is ' + result.ReceiveDate)

```




<hr/>

<div dir='rtl'>

# راهنمای زبان برنامه نویسی Python

### معرفی سرویس پیامکی نیک اس ام اس
<p>شما می توانید با استفاده از سرویس ارسال پیامک <a target='_blank' href='https://niksms.com'>نیک اس ام اس</a> به راحتی پیامک های خود را ارسال نمایید.</p>

### ساخت حساب کاربری
<p>برای استفاده از سرویس پیامکی و API باید یک حساب کاربری در<a target='_blank' href='https://niksms.com/fa/main/register'>بخش ثبت نام نیک اس ام اس</a> ساخته و آن را فعال نمایید.</p>

### مستندات
شما می توانید برای مشاهده کامل مستندات وب سرویس به <a target='_blank' href='https://niksms.com/fa/documentation'>بخش برنامه نویسان</a> سایت مراجعه فرمایید.

### اطلاعات بیشتر
برای کسب اطلاعات بیشتر به وب سایت <a target='_blank' href='https://niksms.com'>نیک اس ام اس</a> مراجعه فرمایید.
</div>


