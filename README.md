# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

# DATE :03-05-2023

# AIM :
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM :
# Client:
Import the necessary modules in python Create a socket connection to using the socket module. 
Send message to the client and receive the message from the client using the Socket module in server
Send and receive the message using the send function in socket.


# PROGRAM :
# CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```

# SERVER:
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
 
 # CLIENT OUTPUT :
 ![243920544-a7d08960-c2e0-429e-a0e7-e8ab3f9d4cbb](https://github.com/Hemaprasad-N/EX-9/assets/135933397/623ca172-902a-4723-a33d-1bab779e6a8b)

 # SERVER OUTPUT :
 ![243920664-08808603-9a18-4736-a3f8-a3003543843d](https://github.com/Hemaprasad-N/EX-9/assets/135933397/ffa0cec2-5341-4932-a251-deab36cb992c)

 # RESULT :
 
 Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed
