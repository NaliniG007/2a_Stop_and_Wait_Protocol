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
## PROGRAM
## NAME: ADITHYA V
## REGISTER NO: 212223110001
## Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter the data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close
        break
```
## Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Received".encode())
```

## OUTPUT

### client
![image](https://github.com/karthik-2106/2a_Stop_and_Wait_Protocol/assets/150319557/3443a3e9-af83-4ac4-a4be-ecca970bb24b)
### server
![image](https://github.com/karthik-2106/2a_Stop_and_Wait_Protocol/assets/150319557/81299281-e802-4c14-a925-580897c7b6dc)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
