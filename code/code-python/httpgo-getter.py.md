---
description: >-
  HTTP resource enumeration script via GET method from Python section of PTSv4
  (eLearnSecurity)
---

# HttpGo-Getter.py

```python
import http.client

print('** Check resources in WWW server and output HTTP status code via GET/HTTP **\n')

host = input('Insert the host/DST IP: ')
port = input('Insert the DST PORT:(default:80) ')
url = input('Insert the URL of the resource you want to check for ')

if(port == ''):
    port = 80

try:
    connection = http.client.HTTPConnection(host, port)
    connection.request('GET', url)
    response = connection.getresponse()
    print('Status Code Returned: ', response.status)
    connection.close()
except ConnectionRefusedError:
    print('Connection Failed')
```

