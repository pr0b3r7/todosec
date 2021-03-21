---
description: TCP Client script from Python section of PTSv4 (eLearnSecurity)
---

# TcpClient.py

```python
# Goal 
# Client that starts a connection to the Python server
# and sends a message. Use function 'connect'

# Notes, to start listening on port 1234 in Linux,
# use "socat -v tcp-l:1234,fork exec:'/bin/cat'"

import socket

CLT_ADDR = input("Server's IP: ")
CLT_PORT = int(input("Type the TCP port you would like to connect to: "))

# Create new socket using the default family socket (AF_INET) that uses TCP
# the default socket type connection-oriented (SOCK_STREAM)

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# Connect to a remote socket at address

s.connect((CLT_ADDR, CLT_PORT))

# print Target IPv4 address and TCP port

print("Connected to:", CLT_ADDR, "on port:", CLT_PORT, "\n")

message = input("Enter message to send: ")

s.sendall(message.encode())
s.close()
```

