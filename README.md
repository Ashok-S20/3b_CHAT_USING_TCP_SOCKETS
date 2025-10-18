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
### CLIENT
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER
```py
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
### CLIENT
<img width="818" height="369" alt="image" src="https://github.com/user-attachments/assets/0c82cc12-f919-407c-b82f-b9829fa4c05f" />

### SERVER
<img width="741" height="384" alt="image" src="https://github.com/user-attachments/assets/37e471bb-ecdf-4b4b-b39f-4aaf787ae4eb" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
