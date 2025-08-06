# Pre-Security - Intro to Lan

## 🧠 What I learned

### Task 1 - Introducing LAN Topologies
- Star Topology
  - devices are connected via central device e.g. switch or hub
  - most common
  - more cabling and requires dedicated networking equipment
  - much more scalable
  - information from a device is sent via the central device, then is sent to the destination

- Bus Topology
  - relies upon a single connection aka "backbone cable"
  - similar to leaf where the central line is the backbone and the smaller lines/stems are lines connected to the device
  - easier and more cost-efficient
  - little to no redundancy in case of failures
  - if the cable breaks, devices will no longer be able to send/receive data along the bus
  - prone to bottleneck and becoming slow

- Ring Topology
  - aka "Token Topology"
  - devices are connected so that they form a loop
  - data is sent across the loop until it reaches the destine device
  - uses the other devices along the loop to pass data
  - if the receiving device has a data to sent, it will send its own data first
  - otherwise, it will forward the received data
  - easy to setup and troubleshoot but data does not efficiently travel across the network

- Switch
  - dedicated device within a network designed to connect multiple devices such as computers, printers, or other network capablet device
  - can have ports 8, 16, 24, 32, and 64 to plug into
  - More efficient than hubs/repeaters
  - It keeps track of what device is connected to which port. Thus, data is sent directly to the destination device

- Router
  - connect networks and pass data between them. hence the name - "router"
  - "routing" is the process of data travelling across networks
  - involves creating a path between networks so data is sucessfully delivered


### Task 2 - A Primer on Subnetting
- splitting up a network into a smaller networks within itself
- e.g. divide a network to 
  1. Accounting
  2. Finance
  3. Human Resources

- subnets use IP Address in 3 different ways:
  1. identify the network address
    - identifies the start of the actual network and is used to identify a network's existence
    - e.g. 192.168.1.0
  2. identify the host address
    - used to identify a device on the subnet
    - e.g. 192.16.1.100
  3. identify the default gateway
    - is a special address assigned to a device on the network that is capable of send information to another network
    - e.g. 192.168.1.254

- benefits:
  - efficiency
  - security
  - full control


### Task 3 - ARP
- Address Resolution Protocol
- allows a device to associate its MAC address with an IP address on the network
- each device will keep a log (local table/list aka "cache") of the MAC addresses associated with other devices
- to map IP Address and Mac Address, ARP sends 2 types of messages:
  1. ARP Request
    - a message is broadcasted on the network to other devices asking "What is the MAC address that owns this IP Address"
  2. ARP Reply
    - devices who receive this will ONLY reply if they own that IP address and will send an ARP Reply with its MAC address
- then the requesting device will remember this mapping into its ARP cache for future reference

### Task 4 - DHCP
- Dynamic Host Configuration Protocol
- Automatically assign an available IP Address to the requesting device if it doesn't already have its own
- Process:
  1. Requesting device sends a "DHCP Discover"
  2. DHCP Server will offer an IP Address > "DHCP Offer"
  3. Requesting device will agree and will request for the available IP Address > "DHCP Request"
  4. DHCP Assigns the IP address to the requesting device > "DHCP Ack"