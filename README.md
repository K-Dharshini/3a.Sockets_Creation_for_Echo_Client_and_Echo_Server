## Ex.No:3a. ECHO AND CLIENT SERVER USING TCP SOCKETS

## AIM:
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python.
   
2. Create a socket connection to using the socket module.
   
3. Send message to the client and receive the message from the client using the Socket module in server.
   
4. Send and receive the message using the send function in socket.
   
## PROGRAM:
# Client
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("Server>",s.recv(1024).decode())
~~~

# Server
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

## OUTPUT:
# Client
![image](https://github.com/K-Dharshini/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139334830/1d04f8be-a202-492b-bf18-a3ba7595d327)

# Server
![image](https://github.com/K-Dharshini/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139334830/71fa2826-4f01-49d6-8df3-f871c9c2b2c4)

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
