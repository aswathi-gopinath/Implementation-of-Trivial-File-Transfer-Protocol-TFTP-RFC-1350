# TFTP Client–Server Implementation (RFC 1350)

This project implements the Trivial File Transfer Protocol (TFTP) based on RFC 1350 using C programming and UDP socket communication on Linux systems. The project demonstrates client–server communication and reliable file transfer over an unreliable transport protocol (UDP).

The system consists of two applications: a TFTP Client and a TFTP Server. The client requests file transfer operations while the server responds to read and write requests and manages data transmission.

The implementation focuses on low-level networking concepts, socket programming, protocol design, packet handling, timeout management, and retransmission mechanisms.

Project Features:
- Implementation of TFTP protocol using UDP sockets
- Client–Server architecture
- Read Request (RRQ) handling
- Write Request (WRQ) handling
- DATA packet transmission
- ACK packet acknowledgement mechanism
- Block number sequencing
- Timeout detection and retransmission
- Error packet handling
- File transfer over Local Area Network (LAN)

TFTP Packet Types Implemented:
Opcode 1 – RRQ (Read Request)  
Opcode 2 – WRQ (Write Request)  
Opcode 3 – DATA  
Opcode 4 – ACK  
Opcode 5 – ERROR  

Technologies Used:
- C Programming Language
- Linux System Programming
- UDP Socket Programming
- Networking Protocols
- POSIX System Calls
- GCC Compiler

Project Folder Structure:
tftp/
client/ → contains client source files  
server/ → contains server source files  
README.md

Compilation Steps:

Compile Server:
gcc server.c -o server

Compile Client:
gcc client.c -o client

Execution Steps:

1. Start the server:
./server

2. Run the client:
./client

3. Follow terminal prompts to upload or download files between client and server.

Working Principle:
The client initiates communication by sending either a Read Request (RRQ) or Write Request (WRQ). The server responds with DATA packets containing file blocks. Each block is acknowledged using ACK packets. If an acknowledgement is not received within a timeout period, the packet is retransmitted to ensure reliable transfer. The transfer completes when the final data block size is less than 512 bytes as defined in RFC 1350.

Learning Outcomes:
- Understanding of application layer networking protocols
- Hands-on experience with UDP socket programming
- Implementation of reliable communication over unreliable transport
- Client–Server software design
- Linux system call usage
- Network debugging and protocol analysis

Author:
Aswathi E P  
Embedded Systems Engineer  
Email: aswathigopinath20@gmail.com  
LinkedIn: https://www.linkedin.com/in/aswathi-ep-by0256  
GitHub: https://github.com/aswathi-gopinath

License:
This project is developed for educational and learning purposes.

