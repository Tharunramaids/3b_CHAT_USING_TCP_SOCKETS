# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM:
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## Server:
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
## OUTPUT:
## Server:

<img width="811" height="793" alt="image" src="https://github.com/user-attachments/assets/dba08663-93f5-45f0-8385-f80e71b2c79b" />

## Client:

<img width="799" height="797" alt="image" src="https://github.com/user-attachments/assets/19cdf323-d7ce-4c5a-8fcf-91db7c30a5ba" />

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
