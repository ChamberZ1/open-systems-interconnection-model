# Intro
The Open Systems Interconnection (OSI) model is a conceptual framework for understanding what is required for data to flow across the internet. While real-world networks do not strictly implement the OSI model, it remains a valuable tool for reasoning about how network communication works and for troubleshooting network and device connectivity issues. By organizing communication into distinct layers, the model allows technicians and engineers to systematically isolate and narrow down problems.

The OSI model breaks network communication into a series of layers, each representing a specific set of responsibilities that must work together for two devices to successfully communicate.
 
# Do You Like [Onions](https://www.youtube.com/watch?v=Lt1u6N7lueM)?
This part was confusing to me until I learned the onion analogy. The OSI model is typically visualized as a layered stack, with Layer 7 at the top and Layer 1 at the bottom. The numbering itself is less important than what each layer represents. Higher-numbered layers are closer to the user experience and deal with application-level behavior, while lower-numbered layers are further removed from the user and focus on the physical transmission of data. The onion analogy helps clarify this idea. The outer layers of an onion are closest to you and are encountered first, much like the higher OSI layers that represent the user-facing parts of a network. As you peel inward, you move away from what the user sees and toward the core, just as lower OSI layers handle the physical and electrical details required to transmit data.

# Mnemonic
The mnemonic I used to help memorize the layers is: "(P)lease (D)o (N)ot (T)hrow (S)ausage (P)izza (A)way" --> (P)hysical, (D)ata Link, (N)etwork, (T)ransport, (S)ession, (P)resentation, (A)pplication.

# The Layers
In the OSI model, Layers 5 (Session), 6 (Presentation), and 7 (Application) were defined as separate layers to isolate session management, data representation, and application logic. In practice, modern networking stacks do not implement these layers independently. Instead, their responsibilities are tightly coupled and are typically handled together within application protocols.

As a result, most real-world protocols combine session handling, data formatting, encryption, and application logic into a single application layer, as reflected in the TCP/IP model.

### Layer 7 - Application
- Provides network services directly to user applications
- ex) HTTP, HTTPS, DNS

### Layer 6 - Presentation
- Handles how data is represented and protected during transmission.
- Responsible for encoding, serialization, compression, and encryption.
- Typically implemented within application protocols.
- ex) TLS/SSL, UTF-8 Encoding.

### Layer 5 - Session
- Manages application-level sessions and communication state.
- In modern networking, session management is usually handled within
  application logic rather than a separate protocol.

### Layer 4 - Transport
- This layer is responsible for process-to-process delivery of data, ensuring that data is delivered to the correct application on a host.
- It uses port numbers to distinguish between applications, allowing multiple services to communicate simultaneously over the network.
- ex) UDP, TCP

### Layer 3 - Network
- This layer is responsible for logical addressing and routing, enabling end-to-end communication across multiple networks.
- It forwards packets based on IP addresses but does not guarantee delivery.
- ex) Routers, IP-configured Hosts, IP Addresses, Packets

### Layer 2 - Data Link
- This layer is responsible for hop-to-hop delivery between adjacent network interfaces.
- It packages raw bits into frames and delivers them using Media Access Control (MAC) addresses to identify the source and destination.
- ex) Network Interface Cards (NICs), Switches, Ethernet and Wi-Fi Frames, MAC Addresses

### Layer 1 - Physical
- The technology in this layer transports bits (1's and 0's) of computer data over a physical or wireless medium.
- ex) Copper Wires, Ethernet Cables, Fiber Optics, Wi-Fi Radio Signals, Repeaters, Hubs

# Acknowledgements
- ChatGPT
- [Practical Networking](https://www.youtube.com/watch?v=LkolbURrtTs&pp=2AYk0gcJCU0KAYcqIYzv)
- [Cloudflare](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
