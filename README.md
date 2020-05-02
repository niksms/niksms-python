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
<p>You can Send Single Sms using below Code</p>

```python
import requests 

URL = "http://niksms.com/api/SingleSms"

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

URL = "http://niksms.com/api/GroupSms"

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

<hr/>

<div dir='rtl'>

# راهنمای زبان برنامه نویسی Python

## معرفی سرویس پیامکی نیک اس ام اس
<p>شما می توانید با استفاده از سرویس ارسال پیامک <a target='_blank' href='https://niksms.com'>نیک اس ام اس</a> به راحتی پیامک های خود را ارسال نمایید.</p>

## ساخت حساب کاربری
<p>برای استفاده از سرویس پیامکی باید یک حساب کاربری در سایت <a target='_blank' href='https://niksms.com/fa/main/register'>نیک اس ام اس</a> ساخته و آن را فعال نمایید.</p>

## مستندات
شما می توانید برای مشاهده کامل مستندات وب سرویس به <a target='_blank' href='https://niksms.com/fa/documentation'>بخش برنامه نویسان</a> سایت مراجعه فرمایید.

## اطلاعات بیشتر
برای کسب اطلاعات بیشتر به وب سایت <a target='_blank' href='https://niksms.com'>نیک اس ام اس</a> مراجعه فرمایید.
</div>


