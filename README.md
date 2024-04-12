# 3b.CREATION FOR CHAT USING TCP SOCKETS

## Developed By : ADITAAYAN M
## Register No  : 212223040006

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:

## client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```

## server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
 ```
## OUTPUT:
## client:
![321572465-67ed1970-0a58-4566-b5b0-bb11ab5fe476](https://github.com/Aditaayan/3b_CHAT_USING_TCP_SOCKETS/assets/147473394/853918bb-751d-40d7-a920-5019538d2ed8)

## server:
![321572545-7fb967e6-9e36-4a79-b24b-930aeee1ee25](https://github.com/Aditaayan/3b_CHAT_USING_TCP_SOCKETS/assets/147473394/a93acd01-55a1-4f2c-a2e7-5610322011cf)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
