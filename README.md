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
## PROGRAMimport socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
        import socket
s=socket.socket()
s.connect(('localhost',8000))
while True 
:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
## OUTPUT

<img width="721" height="214" alt="Screenshot 2025-09-03 111841" src="https://github.com/user-attachments/assets/e957fa60-c567-454c-9101-b5db46d68933" />
<img width="937" height="158" alt="Screenshot 2025-09-03 112218" src="https://github.com/user-attachments/assets/5b57135e-8066-4ab3-b83b-1439fd66e565" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
