# Pre-Security - Packets & Frames

## 🧠 What I learned

### Task 1 - What are Packets and Frames
- small pieces of data when formed together make a larger piece of information/message
- 2 different things in OSI model
  - packets - Layer 3
    - piece of data from network layer
    - contains IP [header](#ip-header) and [payload](#payload)     
    - packets are efficient way of communicating data across network
    - data is exchanged in small pieces so less chance of bottleneck as opposed to large messages sent at once
    - e.g. images are sent as small pieces and re-assembled when it reaches destination (Transport layer 4 re-assembles this image)
    - some headers:
      - Time to Live > packet will expire after certain time
      - Checksum > provides checking, otherwise data is corrupt
      - Source address > IP address of data sender
      - Destination address > IP address of data receiver
  - frames - Layer 2
    - encapsulates packet and adds additional information such as MAC Address (adds source and destination MAC address)


### Task 2 - TCP/IP (The Three-Way Handshake)
- Transmission Control Protocol
- Only 4 layers
  1. Application
  2. Transport
  3. Internet
  4. Network Interface
- TCP is connetion-based > will need to establish connection first between 2 devices before data is sent
- will guarantee that any data will be received by destination
- Pros
  - data integrity
  - device synchronization to avoid being flooded with data in wrong order
  - reliability (but more processes)
- Cons
  - requires reliable connection
  - if small chunk is not received, entire chunk of data cannot be used and must be re-sent
  - slow connection can bottleneck another device as connection is reserved on the other device the whole time
  - slower than UDP since more work has to be done

- Three-Way Handshake
  1. SYN - initial packet sent by source during handshake
  2. SYN/ACK - sent by receiving device to acknowledge synchronization
  3. ACK - sent by sender to acknowledge that a series of messages/packet have been successfully received
  4. DATA - information being sent
  5. FIN - packet used to cleanly close the connection
  6. RST - abruptly end all communication e.g. problem during process

- Example: Alice wants to send some info to Bob
  1. Alice sends SYN to Bob
  2. Bob sends SYN/ACK to acknowledge communication
  3. Alice send ACK to confirm communication

- TCP Closing a connection
  1. Alice send FIN to inform connection will be closed
  2. Bob sends ACK agreeing to this
  3. Bob send FIN to acknowledge closure
  4. Alice sends ACK to confirm closure

### Task 3 - Practical - Handshake
- Alice asks if Bob can hear her (SYN)
- Bob replies that he can hear her (SYN/ACK)
- Alice responds "Okay Great" (ACK)
- Then, Alice sends a message (DATA)
- Bob acknowledges Alice's message (ACK)
- Alice responds she's done sending her message (FIN/ACK)
- Bob responds he's done as well (FIN/ACK)
- Alice responds "goodbye" (ACK)

### Task 4 - UDP/IP
- User Datagram Protocol
- stateless protocol
- doesn't require constant connection between 2 devices for data to be sent
- Three-way handshake doesn't occur

- Pros:
  - much faster than TCP
  - leaves apps to decide if there is any control how quickly packets are sent
  - does not reserve a continuous connection

- Cons:
  - doesn't care if data is received or not
  - flexible to software deves
  - unstable connections result in terrible experience for user

- fewer packets and fewer headers
- some headers:
  - Time to Live
  - Source address
  - Destination Address
  - Source port
  - Destination port
  - Data

- UDP Connection
  1. Bob requests information from Alice
  2. Alice sends information
  3. Alice sends information
  4. Alice sends information
- Unlike TCP, there is no syn/ack and data just gets sent anyways

### Task 5 - Ports (101)
- ports are numerical value between 0 and 65535
- ports identify which software (or process) should handle incoming or outgoing data on a device
- define where the data goes so correct program can handle it


## 📚 KEYWORDS

### IP Header
- is a segment of data placed at the beginner of a network packet or frame
<a name="ip-header"></a>

### Payload
- payload refers to part of transmitted message or data that carries the actual intended information
- payload is data portion of a message that a user or app intends to send
<a name="payload"></a>