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
#SERVER
```
import socket

HOST = '127.0.0.1'  
PORT = 65432       

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print('Connected by', addr)
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
## OUPUT
#SERVER
![Screenshot 2024-03-13 150749](https://github.com/Pradeepkumar-2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147474038/716264e7-af1e-4aa5-9a21-1495f4b66c1d)

#CLIENT
![Screenshot 2024-03-13 150805](https://github.com/Pradeepkumar-2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147474038/d3002f41-b1f4-48ad-b52f-62d8db0a4f85)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
