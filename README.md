# Client-Server Communication System
Client-Server Communication System
Overview
This C code implements a basic client-server communication system using shared memory and pthreads. The system enables clients to register with the server, perform mathematical operations, and unregister when done.

Features
Client-Server Interaction: Clients communicate with the server using shared memory segments for requests and responses.

Registration and Unregistration: Clients can register and unregister with the server, creating and destroying shared memory segments as needed.

Mathematical Operations: Clients can request the server to perform arithmetic operations and check if a number is even, odd, prime, or negative.

Usage
Compilation:

Server: gcc server.c -o server -lpthread
Client: gcc client.c -o client
Execution:

Run server: ./server
Run clients: ./client
Client Operations:

Clients interact with the server through a menu, choosing mathematical operations or unregistering.
Communication Mechanism:

Shared memory segments and mutex locks ensure synchronized communication.
Notes
Error Handling:

Handles non-unique client names, invalid keys, and input errors during arithmetic operations.
Sleep Duration:

Includes a brief sleep to avoid busy-waiting and reduce CPU usage.
