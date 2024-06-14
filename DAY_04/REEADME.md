# ♦ Day 04

## ◙ 1st Topic ***NMAP***
  : Nmap is short for Network Mapper. It is an open-source Linux command-line tool that is used to scan IP addresses and ports in a network and to detect installed applications. Nmap allows network admins to find which devices are running on their network, discover open ports and services, and detect vulnerabilities.

  ***SYNTAX*** : nmap [scan type] {target specification}
      Ex:- nmap fb.com/24
           nmap 192.168.204.10 {To scan a single ip address}
           nmap -iL ip.txt  {To scan a list of ip`s }

 ## ♦ NMAP --help

  ### • 1st Page
  ![Screenshot 2024-06-14 130335](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/96cc9ea9-b446-400b-ad3d-80bbb599f968)
  ### • 2 Page
  ![Screenshot 2024-06-14 130439](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/49d648b0-b96d-47e3-ba30-1e82687e28dc)
  ### • 3 Page
  ![Screenshot 2024-06-14 130458](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/011a4c85-f556-4ed3-994e-63dfec6c6bc5)
  ### • 4 Page
  ![Screenshot 2024-06-14 130514](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/8ecde326-8954-4362-ab7e-76f29d9747c9)

## TCP (Transmission Control Protocol) & UDP (User Datagram Protocol)

• **TCP** - Transmission Control Protocol is a connection-oriented protocol for communications that helps in the exchange of messages between different devices over a network. The Internet Protocol (IP), which establishes the technique for sending data packets between computers, works with TCP.***{ ERROR HADLING AND DEBUGGING IS POSSIBLE IN TCP}***

• **UDP** - The User Datagram Protocol, or UDP, is a communication protocol used across the Internet for especially time-sensitive transmissions such as video playback or DNS lookups. It speeds up communications by not formally establishing a connection before data is transferred. This allows data to be transferred very quickly, but it can also cause packets to become lost in transit — and create opportunities for exploitation in the form of DDoS attacks.***{ ITS TRANSMISSION RATE IS MORE IN UDP}***

### ◙ TCP vs. UDP

1. UDP is faster but less reliable than TCP, another common transport protocol. In a TCP communication, the two computers begin by establishing a connection via an automated process called a ‘handshake.’ Only once this handshake has been completed will one computer actually transfer data packets to the other.
2. UDP communications do not go through this process. Instead, one computer can simply begin sending data to the other
3. In addition, TCP communications indicate the order in which data packets should be received and confirm that packets arrive as intended. If a packet does not arrive — e.g. due to congestion in intermediary networks — TCP requires that it be re-sent. UDP communications do not include any of this functionality.
4. These differences create some advantages. Because UDP does not require a ‘handshake’ or check whether data arrives properly, it is able to transfer data much faster than TCP.
However, this speed creates tradeoffs. If a UDP datagram is lost in transit, it will not be re-sent. As a result, applications that use UDP must be able to tolerate errors, loss, and duplication.
(Technically, such packet loss is less a flaw in UDP than a consequence of how the Internet is built. Most network routers do not perform packet ordering and arrival confirmation by design, because doing so would require an unfeasible amount of additional memory. TCP is a way of filling this gap when an application requires it.)


# ♦ There are a Total of 64738 ports are available 
  • Port 443 - Used for HTTPS (HYPERTEXT TRANSFER PROTOCOL SECURE) 
  
  • Port 80 - Used for HTTP (HYPERTEXT TRANSFER PROTOCOL) 
  
  • Port 22 - Used for SSH (SECURE SHELL) 
  
  • Port 21 - Used for FTP (FILE TRANSFER PROTOCOL)
  
  • Port 53 - Used for DNS (DOMAIN NAME SERVER)

  • Port 143 - Used for IMAP (INTERNET MESSAGE ACCESS PROTOCOL)

  • Port 138 - Used for NetBIOS Datagram Service     ***ETC***
  
  #### • ABOUT ALL THE PORTS [HERE](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)

  ### • ABOUT SYN
   : A client sends a SYN (synchronize) message to a server, indicating a desire to establish a connection. The server acknowledges this request by sending a SYN-ACK message back to the client. The client responds with an ACK (acknowledgment), and the connection is officially established.
   ### 1.
![image](https://github.com/Izumi0XD/CYBER_SECURITY_NOTES/assets/141332753/7913b4ac-84ab-43f6-90d1-4f0bf5975c36)

## PORT SPECIFICATION 
  : one of the most impostant and useful feature in NMAP is that we can specify the port number and specifications we can also scan all ports using **-p-** but it takes a lot of time so we can reduceit using **-T4**

  
