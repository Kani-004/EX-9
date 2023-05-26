# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

DATE : 04-05-2023

# AIM :

To write a python program for creating Chat using TCP Sockets Links

# ALGORITHM :

Start the program.
Get the frame size from the user.
To create the frame based on the user request.
To send frames to server from the client side.
If your frames reach the server, it will send ACK signal to client otherwise it will sendNACK signal to client.
Stop the program

# PROGRAM :

## CLIENT:
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
~~~

## SERVER:
~~~
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
~~~

# OUTPUT :

![image](https://github.com/Kani-004/EX-9/assets/129577149/42d19d49-0f81-4b53-9642-c52d93cfba2d)

# RESULT :
~~~

Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
~~~
