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

CLIENT :
~~~

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

~~~
SERVER :
~~~

import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())

~~~

## OUPUT

CLIENT :

![image](https://github.com/user-attachments/assets/ed152ab5-4ed8-4b72-bdaf-8fa28c4ae8e8)

SERVER :

![image](https://github.com/user-attachments/assets/524a7454-265f-4899-8067-699fab2b3c74)

## RESULT

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
