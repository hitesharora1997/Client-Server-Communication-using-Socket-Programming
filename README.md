# Client-Server Communication using Socket Programming

## Overview
This project demonstrates client-server communication using socket programming in both UNIX and Internet domains. Sockets facilitate inter-process communication within a single system or across a network. Essentially, sockets are two endpoints that enable this communication. While a socket represents a single connection between exactly two pieces of software, communication between multiple pieces of software is possible using multiple sockets.

## Socket Types
### AF_UNIX (UNIX Domain Sockets)
- Handles requests from clients by creating file system sockets.
- Establishes connections between clients and server in a multi-threaded environment.

### AF_INET (Internet Domain Sockets)
- Creates AF_INET sockets to connect clients and server.
- Supports connections via loopback address on the same machine.
- Facilitates communication using IP addresses over the same network on different systems.
- Utilizes threads and mutexes to manage multiple client connections.

## Features
- Multi-threaded server capable of handling multiple client requests simultaneously.
- Supports both UNIX domain and Internet domain sockets.
- Demonstrates basic principles of socket programming for both intra-system and network communication.

## Getting Started

### Prerequisites
- C/C++ compiler
- Basic understanding of socket programming

### Compilation
```sh
gcc -o server server.c -lpthread
gcc -o client client.c
