# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Name: NIRANJAN S
## Ref : 212224040221

## CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8080)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER:
```
 
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```

## OUTPUT:

## CLIENT

![323984271-2b2650cb-7e5d-46ad-b2b2-8fc4a1cc8d44](https://github.com/user-attachments/assets/5bd3985a-ebe9-45c9-98ce-56f171985a60)
## SERVER:

![323984174-74b5503f-6551-4c3b-9f20-2a6005f5a4a0](https://github.com/user-attachments/assets/7bb90d78-da4f-4d82-a633-57592fa75bb6)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
