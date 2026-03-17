# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
server
```
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept()
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
client
```
import socket 
s=socket.socket() 
s.connect(('localhost',9000)) 
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
<img width="1858" height="318" alt="Screenshot 2026-03-17 090410" src="https://github.com/user-attachments/assets/d2291e3c-732b-499e-9abc-be0ad41b3126" />
<img width="1843" height="180" alt="Screenshot 2026-03-17 090514" src="https://github.com/user-attachments/assets/88c0004c-e4db-4f21-a6ca-c507415fa1be" />




## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
