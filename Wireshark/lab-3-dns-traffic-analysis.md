Objective

-The objective of this lab is to analyze DNS traffic and understand how a computer 
translates a domain name into an IP address before communicating with a website or service.

Command used

-dig google.com

Findings

-Wireshark captured DNS traffic generated when resolving the domain name google.com. 
 The packet capture showed a DNS Standard Query sent from the Ubuntu virtual machine to the configured DNS server, 
 followed by a DNS Standard Query Response containing the IPv4 address associated with the requested domain.
 Applying the dns display filter isolated the DNS packets, making it easy to examine the name resolution process.

Analysis

-The packet capture demonstrated that domain names must be translated into IP addresses before network communication can begin.
 The DNS query requested an IPv4 address (A record) for google.com, and the DNS server responded with the corresponding address.
 This exchange enabled the operating system to establish subsequent connections using the returned IP address.

Lessons Learned

-DNS translates domain names into IP addresses.

-DNS queries occur before communication with most websites.

-Wireshark can capture both DNS queries and DNS responses.

-The dns display filter isolates DNS traffic for analysis.

-DNS traffic is valuable during network troubleshooting and security investigations.

Screenshots

-dns display filter in use

![dns filter](images/dns-display-filter)

-The expanded DNS section showing the returned IP address.

![expanded DNS section](images/expanded-dns-section)


