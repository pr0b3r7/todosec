---
description: TCP Server script from Python section of PTSv4 (eLearnSecurity)
---

# TcpServer.py

```python
# Goal 
# Bind to specific IPv4 address and TCP port (client) and 
# listen for incoming TCP communications (server)

# import socket module (low level network interface)

import socket

# Takes input from the user and saves it in variables SRV_ADDR and SRV_PORT

SRV_ADDR = input("Type the server IP address: ")
SRV_PORT = int(input("Type the server port: "))

# Create a new socket using the default family socket (AF_INET) that uses TCP and 
# the default socket type connection-oriented (SOCK_STREAM)

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# bind function binds the socket to the provided address and port, while
# the listen function instructs the socket to listen for an incoming connection. 

s.bind((SRV_ADDR, SRV_PORT))

# the argument 1 specifies the maximum number of queued connections.

s.listen(1)
print("Server started! Waiting for connections...")

# connection is the socket object we will use to send and receive data
# address contains the client address bound to the socket
connection, address = s.accept()

# Print address of connected client and 

print('Client connected with address:', address)

# start an infinite loop 

while 1:
    data = connection.recv(1024)
    if not data: break
    connection.sendall(b'-- Message Received --\n')

# print all messages received from it

    print(data.decode('utf-8'))
connection.close()
```

