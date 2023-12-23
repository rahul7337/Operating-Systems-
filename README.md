# Operating-Systems-
Client-Server Communication System
Overview
This code implements a simple client-server communication system using shared memory and pthreads in C. The system allows clients to register with the server, perform various mathematical operations, and then unregister when done.

Features
Client-Server Interaction: Clients communicate with the server using shared memory segments, allowing them to send requests and receive responses.

Registration and Unregistration: Clients can register and unregister with the server, creating and destroying shared memory segments as needed.

Mathematical Operations: Clients can request the server to perform arithmetic operations (addition, subtraction, multiplication, division), check if a number is even or odd, check if a number is prime, and check if a number is negative.

Usage
Compilation:

Compile the server code using: gcc server.c -o server -lpthread
Compile the client code using: gcc client.c -o client
Execution:

Run the server in one terminal: ./server
Run one or more clients in separate terminals: ./client
Client Registration:

Clients are prompted to enter a unique name when they start. The client sends a registration request to the server, and if successful, it receives a key for further communication.
Client Menu:

Clients are presented with a menu to choose from various mathematical operations or unregister and exit.
Mathematical Operations:

Clients can perform arithmetic operations on two numbers, check if a number is even or odd, check if a number is prime, and check if a number is negative.
Unregistration:

Clients can unregister and exit, sending an unregister request to the server. The server cleans up the resources associated with the client.
Communication Mechanism
Shared Memory Segments:

Clients and the server communicate through shared memory segments for exchanging messages.
Mutex Locking:

Mutex locks are used to ensure synchronized access to shared resources, preventing race conditions.
Client Threads:

Each client runs in its own thread, allowing concurrent communication with the server.
Notes
Error Handling:

The system handles errors such as non-unique client names, invalid keys, and invalid input during arithmetic operations.
Sleep Duration:

A brief sleep duration is included to avoid busy-waiting and reduce CPU usage.
