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

OUTPUT:




RESULT:

