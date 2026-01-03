# Intro
The Open Systems Interconnection (OSI) model is a powerful framework for understanding what is required for data to flow across the internet and for troubleshooting network and device connectivity issues, allowing technicians and engineers to systematically narrow down problems.

The model breaks network communication into a series of distinct layers, each representing responsibilities that must work together for two devices to successfully communicate. 

# Do You Like [Onions](https://www.youtube.com/watch?v=Lt1u6N7lueM)?
This part was confusing to me until I learned the onion analogy. The OSI model is typically visualized as a layered stack, with Layer 7 at the top and Layer 1 at the bottom. The numbering itself is less important than what each layer represents. Higher-numbered layers are closer to the user experience and deal with application-level behavior, while lower-numbered layers are further removed from the user and focus on the physical transmission of data. The onion analogy helps clarify this idea. The outer layers of an onion are closest to you and are encountered first, much like the higher OSI layers that represent the user-facing parts of a network. As you peel inward, you move away from what the user sees and toward the core, just as lower OSI layers handle the physical and electrical details required to transmit data.

# Mnemonic
The mnemonic I used to help memorize the layers is: "(P)lease (D)o (N)ot (T)hrow (S)ausage (P)izza (A)way" --> (P)hysical, (D)ata Link, (N)etwork, (T)ransport, (S)ession, (P)resentation, (A)pplication.

# The Layers
### Layer 7 - Application

### Layer 6 - Presentation

### Layer 5 - Session

### Layer 4 - Transport
- This layer is responsible for service-to-service delivery of data, ensuring that data is delivered to the correct application on a host.
- It uses port numbers to distinguish between applications, allowing multiple services to communicate simultaneously over the network.
- ex) UDP, TCP

### Layer 3 - Network
- This layer is responsible for logical addressing and routing, enabling end-to-end communication across multiple networks.
- It forwards packets based on IP addresses but does not guarantee delivery.
- ex) Routers, IP-configured Hosts, IP Addresses, Packets

### Layer 2 - Data Link
- This layer is responsible for hop-to-hop delivery between adjacent network interfaces.
- It packages raw bits into frames and delivers them using Media Access Control (MAC) addresses to identify the source and destination.
- ex) Network Interface Card (NIC), Switches, Ethernet and Wi-Fi Frames, MAC Addresses

### Layer 1 - Physical
- The technology in this layer transports bits (1's and 0's) of computer data over a physical or wireless medium.
- ex) Copper Wires, Ethernet Cables, Fiber Optics, Wi-Fi Radio Signals, Repeaters, Hubs

# Acknowledgements
- ChatGPT
- [Practical Networking](https://www.youtube.com/watch?v=LkolbURrtTs&pp=2AYk0gcJCU0KAYcqIYzv)
