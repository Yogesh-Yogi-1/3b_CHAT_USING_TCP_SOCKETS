# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME : V.YOGESH
## REG NO : 212223230250
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT 
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
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
## OUTPUT
## CLIENT
![Screenshot 2024-05-15 214914](https://github.com/Yogesh-Yogi-1/3b_CHAT_USING_TCP_SOCKETS/assets/148514598/c18727bb-6141-4192-a445-9478662642e9)
## SERVER
![Screenshot 2024-05-15 214931](https://github.com/Yogesh-Yogi-1/3b_CHAT_USING_TCP_SOCKETS/assets/148514598/094a5f16-5036-4091-b1f1-f5783a659278)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
