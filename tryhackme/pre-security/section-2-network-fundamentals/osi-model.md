# Pre-Security - OSI Model

## 🧠 What I learned

### Task 1 - What is the OSI Model?
- Open Systems Interconnection Model
- provides a framework dictating how all networked devices will send, receive, and interpret data
- 7 layers:
  1. Layer 1 - Physical
  2. Layer 2 - Data Link
  3. Layer 3 - Network
  4. Layer 4 - Transport
  5. Layer 5 - Session
  6. Layer 6 - Presentation
  7. Layer 7 - Application

- When pieces of information are added to data > encapsulation
- When pieces of information are 'removed' > decapsulation

### Task 2 - Layer 1 - Physical
- references the physical components
- hardware used in networking
- transfer data between each other in binary (0s and 1s)
- e.g. ethernet cables

### Task 3 - Layer 2 - Data Link
- focues on the physical addressing of the transmission
- receives a packet from the network layer (layer 3) and adds in the physical MAC address of the receiving endpoint
- data link layer also present the data in a format suitable for transmission

### Task 4 - Layer 3 - Network
- routing & re-assembly of data takes place
  - routing > determines the most optimal path in which these chunks of data should be sent

- OSPF > Open Shortest Path Firsrt
- RIP > Routing Information Protocol

- factors:
  - Shortest path?
  - Most reliable path?
  - Has faster physical connection?

- everything is dealth with via IP Address
- routers are layer 3 devices

### Task 5 - Layer 4 - Transport
- transmit data across network and follows 2 different protocols:
  1. TCP - Transmission Control Protocol
    - designed with reliability and guarantee in mind
    - reserves a constant connection between 2 devices
    - incorporates error checking to guarantee data sent from small chunks in session layer has been received and reassembled in the same order
    - guarantees accuracy of data
    - synchronize 2 devices
    - performs a lot more processes for reliability
    - mostly used for emails, downloading files, anything that needs a complete data
  2. UDP - User Datagram Protocol
    - data gets sent to the computer whether it gets there or not
    - no synchronization between 2 devices
    - mostly used in real time communication such as voicecall, video call, videos, music
    - much faster than TCP since it doesn't care if data is received
    - lets application layer (user software) to decide it there is any control how quickly packets are sent
    - does not reserve a continuous connection on a device as TCP does

### Task 6 - Layer 5 - Session
- this layer creates and maintain a connection to other computer for which data is destined
- when connection is established, session is created
- responsible for closing connection if idle or lost
- can contain checkpoints where if data is lost, only neweset pieces of data are needed to be sent to save bandwidth

### Task 7 - Layer 6 - Presentation
- standardisation
- even with different programs, data still need to be handled the same way
- translator for data to and from application layer
- e.g. 2 different computers have different email clients such as outlook and apple mail, but data (contents) will display the same
- security features such as data encryption e.g. HTTPS occurs here
- "Translator"

### Task 8 - Layer 7 - Application
- protocols and rules are in place to determine how users will interact with sent/received data
- email clients, browsers, GUI, DNS