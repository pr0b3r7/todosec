---
description: TCP Port Scanner script from Python section of PTSv4 (eLearnSecurity)
---

# PortScanner.py

```python
# Goal - Port scanner
import socket

TARGET = input("Server's IP: ")
PRANGE = input("Enter port range i.e 1-100: ")

lowport = int(PRANGE.split('-')[0])
highport = int(PRANGE.split('-')[1])

# Output given range and target
print('Scanning host ', TARGET, 'from port ', lowport, 'to port ', highport)

# For loop iterates attempting connections on all ports in range
# 0 = port open; otherwise closed.
for port in range(lowport, highport):
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    status = s.connect_ex((TARGET, port))
    if(status == 0):
        print('*** Port', port, '- OPEN ***')
    else:
        print('*** Port', port, '- CLOSED ***')
    s.close()
```

