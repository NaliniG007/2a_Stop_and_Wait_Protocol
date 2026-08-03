# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
Client.py
```
import socket
s = socket.socket()
s.connect(("localhost", 8000))
while True:
    # Receive data from server
    data = s.recv(1024).decode()
    print("Server:", data)
    s.send("Acknowledgement Received".encode())
s.close()
```
server.py
```
import socket
s = socket.socket()
s.bind(("localhost", 8000))
s.listen(5)
print("Server is waiting for connection...")
c, addr = s.accept()
print("Connected to:", addr)
while True:
    data = input("Enter Data: ")
    c.send(data.encode())
    ack = c.recv(1024).decode()
    if ack:
        print("Client:", ack)
    else:
        break
c.close()
s.close()
```
## OUTPUT
<img width="673" height="252" alt="image" src="https://github.com/user-attachments/assets/deb9c515-ce55-4099-84fa-716313d0ded7" />
<img width="793" height="205" alt="image" src="https://github.com/user-attachments/assets/aa7afbe6-8d29-4782-aca3-a3690735ac16" />



## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
