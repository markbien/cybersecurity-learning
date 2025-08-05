# Pre-Security - What is Networking?

## 🧠 What I learned

### Task 1 - What is Networking?
- Networks in computing is simply connection of multiple devices be it mobile device, tablet, computers, printers, etc.
- This allows multiple devices send and receive data

### Task 2 - What is the Internet?
- Internet is a one giant network that consists of many small networks within itself
- First iteration of the Internet was within ARPANET project in the late 1960s
- Funded by US Defence Department
- Tim Berners-Lee invented WWW (World Wide Web)
- These small networks can be private or public network

### Task 3 - Identifying Devices on a Network
- To communicate and maintain order, devices must be both identifying and identifiable
- Similar to humans that we have
  - Our Name
  - Our Fingerprints

- For devices, they have:
  - An IP Address
  - A Media Access Control ([MAC](#mac)) Address

- IP Addresses (Internet Protocol Address)
  - can be used to identify a host on a network
  - e.g. 192.168.1.1
  - set of numbers divided into 4 octets
  - can change from device to device but cannot be used simultaneously within the same network
  - Public address is used to identify device on the internet
  - Private address is used to identify a device amongst other device (can be in the same network)
  - 2 devices with different private address sent a data within the same network, they will still be identified with the same public address
  - Public address are given by ISP (Internet Service Provider)
  - IPv4 is dominant but the new version is IPv6

- MAC Addresses
  - devices connecting to network will always have physical network interface (e.g. microchip board)
  - A unique address is set to it
  - 12 character hexadecimal number split into 2s separated by a colon (e.g. a4:c3:f0:85:ac:2d)

### Task 4 - Ping (ICMP)
- one of most fundamental netework tools available to us
- ICMP > Internet Control Message Protocol
  - determine the performance of a connection between devices
  - check if connection exists or is reliable
- Running ping 192.168.1.1 will perform a teste


## 📚 KEYWORDS
### MAC (Media Access Control) Address
- Is the address embedded into the network cards of a device
- Similar to serial number
- a4 : c3 : f0 : 85 : ac : 2d
- [ a4 : c3 : f0 ] - vendor who buil the network interface, in this case, Intel
- [ 85 : ac : 2d ] - Unique address of the network interface