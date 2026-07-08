Objective

-The objective of this lab is to capture and analyze Address Resolution Protocol (ARP) traffic using Wireshark and 
 understand how devices resolve IP addresses to MAC addresses before communicating on a local area network (LAN).

Commands

-ip route

-sudo  ip neigh flush all

-ping -c 4 10.0.2.2

Findings

-Wireshark captured ARP request and reply packets generated when the local machine attempted to 
 communicate with the default gateway. The ARP request asked for the MAC address associated with the gateway's IP address,
 and the ARP reply provided the corresponding MAC address. This demonstrated how IP addresses are translated into MAC addresses
 before communication occurs on a local network.

Analysis

-The packet capture demonstrated the role of ARP in local network communication. Before transmitting Ethernet frames,
 the sender must determine the destination device's MAC address. The ARP request was broadcast to all devices on the network, 
 while the ARP reply was sent directly back to the requesting host with the required MAC address.

Lesson Learned

-ARP maps IP addresses to MAC addresses.

-ARP Requests are broadcast on the local network.

-ARP Replies provide the requested MAC address.

-Ethernet communication depends on successful ARP resolution

Screenshots

-ARP filter

![Arp filter](images/ARP-Filter.png)

-Expanded Ethernet

![Expanded Ethernet](images/expanded-ethernet.png)

-Expanded ARP

![Expanded ARP](images/expanded-arp.png)
