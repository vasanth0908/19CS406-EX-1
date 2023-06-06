# 19CS406-EX-1 STUDY OF SOCKET PROGRAMMING WITH CLIENT-SERVER MODEL
DATE :08-03-2023
AIM :
To implement socket programming date and time display from client to server using TCPSockets

ALGORITHM :
Server:
Create a server socket and bind it to port.
Listen for new connection and when a connection arrives, accept it.
Send server‟s date and time to the client.
Read client‟s IP address sent by the client.
Display the client details.
Repeat steps 2-5 until the server is terminated.
Close all streams.
Close the server socket.
Stop.

Client:
Create a client socket and connect it to the server‟s port number.
Retrieve its own IP address using built-in function.
Send its address to the server.
Display the date & time sent by the server.
Close the input and output streams.
Close the client socket.
Stop.

PROGRAM:
CLIENT PROGRAM :
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
address={"165.165.80.80":"6A:08:AA:C2","165.165.79.1":"8A:BC:E3:FA"};
while True:
 ip=c.recv(1024).decode()
 try:
 c.send(address[ip].encode())
 except KeyError:
 c.send("Not Found".encode())
 
 
SERVER PROGRAM :
import socket
s=socket.socket()
s.connect(('localhost',8000))
print(s.getsockname())
print(s.recv(1024).decode())
s.send("acknowledgement recived from the server".encode())

OUTPUT:
![1](https://github.com/vasanth0908/19CS406-EX-1/assets/122000018/943bf759-d77b-49dc-b18a-75e76a1cc93a)

![2](https://github.com/vasanth0908/19CS406-EX-1/assets/122000018/de28b101-03ea-48e9-b8c5-c0c38eba9e3f)




RESULT:

