# Pre-Security - Extending Your Network

## 🧠 What I learned

### Task 1 - Introduction to Port Forwarding
- without port forwarding, apps and services such as web servers are only available to device within the same direct network
- To explain further:
  - e.g. a router with an IP Address of 192.168.1.10 runs a webserver on port 80 (public IP is 82.62.51.70)
  - only the 2 other computers on this network will be able to access it AKA Intranet
  - to have it available to devices outside the network (through the internet), port forwarding is a must
  - once setup, the outside network (public IP is 172.68.43.21) can access the webserver using its public IP (82.62.51.70)
- port forwarding opens specific ports
- router is used to configure port forwarding

### Task 2 - Firewalls 101
- is a device within the network responsible for allowing/denying traffic to enter and exit
- AKA border security for a network
- can configure firewall to permit or deny traffic from entering or exiting a network based on:
  - where traffic is coming from
  - where traffic needs to go
  - what port is traffic for (such as 80)
  - what protocol (tcp, udp)

2 primary categories:
  1. Stateful
    - uses the entire information from a connection rather than inspecting individual packet
    - determine the behaviour of a device based upon the entire connection
    - decision making is dynamic

  2. Stateless
    - uses static set of rules to determine whether or not individual packets are acceptable or not
    - will not block a device if a bad packet enters
    - if a rule is not exactly matched, it is effectively useless
    - great against DDoS

### Task 3 - Practical - Firewall
- In this activity, I created a simple rule to prevent malicious traffic:
  - Source IP is set to the machine's IP sending red dots (malicious traffic)
  - Destination IP is set to the receiving device (web server)
  - Port is 80
  - Action is set to DROP

### Task 4 - VPN Basics
- Virtual Private Network
- allows devices on separate networks to communicate securely
  - e.g. home computers, laptops connecting to work/company network
- creates a dedicated path between home device and work network other internet known as tunnel
- devices connected to the tunnel form their own private network
- Benefits:
  - allows networks from other parts of the world to connect
  - privacy > even when using public wifi, using a VPN protects your traffic against other people
  - offers anonymity

- some existing VPN technologies:
  - PPP
    - allow for authentication and provide encryption
    - VPNs use private key and public certificate and both must match for you to connect
    unable to leave a network by itself
  - PPTP
    - Point-to-Point Tunneling Protocol
    - allows data from PPP to travel and leave a network
- IPSec
  - Internet Protocol Security
  - encrypts data using IP framework
  - boasts strong encryption and is also supported on many devices

### Task 5 - Lan Networking Devices
- Router
  - connect networks and pass data between them
  - through "routing"
    - process of data traveling across networks
    - creating a path between networks so data can be delivered
  - operates at Layer 3 of the OSI model
  - Different protocols decide what path should be taken
    - What is shortest
    - What is most reliable
    - Which has faster medium (copper or fiber)
- Switch
  - providing means of connecting devices
  - uses ethernet cables
  - operate at Layer 2 and Layer 3 of the OSI model (but layer 2 switches cannot operate at layer 3)
  - switches forward frames onto the connected devices using their MAC address
  - Layer 3 switches can perform SOME functinos of router
    - send frames to devices (as layer 2 does) and route packets to other devices using IP protocol

- VLAN (Virtual Local Area Network)
  - allows splitting of network virtually
  - e.g. Sales Department, Accounting Department, Tech Department
  
### Task 6 - Practial - Network Simulator
- In this activity, I sent a TCP packet from computer 1 to computer 3 where they are both on a separate switches but connected to the same router
- When TCP packet is sent from computer 1, it failed to find computer 3 in the same network, thus, the router sent an ARP request to find computer 3's IP address
- After computer 3 answers the ARP request by sending ARP response, SYN was sent to computer 3 and computer 3 sent SYN/ACK to computer 1
- Then, computer 1 sent ACK to computer 3
- Next, data was sent to computer
- Finally, computer 3 sent ACK to computer 1