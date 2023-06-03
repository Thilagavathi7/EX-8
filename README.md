### EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

DATE :27-04-2023

### AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

### ALGORITHM :

 1.Start the program.
 
 2.Get the frame size from the user
 
 3.To create the frame based on the user request.
 
 4.To send frames to server from the client side.
 
 5.If your frames reach the server, it will send ACK signal to client otherwise it will send NACKsignal to client.
 
 6.Stop the program


### PROGRAM :

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
### OUTPUT :

CLIENT: 
![image](https://github.com/Thilagavathi7/EX-8/assets/119407159/818cba62-2b73-4b67-9ee7-33a9493fe123)

SERVER:
![image](https://github.com/Thilagavathi7/EX-8/assets/119407159/e1e2f85b-ee02-43f4-ad69-0b427366aac1)




### RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
