# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### NAME : DODLA SUSMITHA
### REGISTER NO : 212224110016
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM

### SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8080))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
### CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```


## OUPUT
<img width="1919" height="1103" alt="Screenshot 2025-10-15 110700" src="https://github.com/user-attachments/assets/51ec84b2-9191-4d2d-bce4-92971b8b4feb" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
