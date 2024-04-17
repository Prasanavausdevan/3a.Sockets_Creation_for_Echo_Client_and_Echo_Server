# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server.
4. Send and receive the message using the send function in socket.
## PROGRAM:
## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUTPUT:
## Client:
![3aclient](https://github.com/Prasanavausdevan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870579/4d0d2b95-f6ff-4ed5-983b-c96f01dc8c5a)

## Servera
![3aserver](https://github.com/Prasanavausdevan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870579/5385c415-e071-4911-970e-94784abfe157)


## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
