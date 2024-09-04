---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">Incident Report: Unreachable DNS Port</h1>

[Project reference](https://www.coursera.org/learn/networks-and-network-security?specialization=google-cybersecurity)

## Case Study Scenario
You are a cybersecurity analyst working at a company that specializes in providing IT services for clients. Several customers of clients reported that they were not able to access the client company website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you attempt to visit the website and you also receive the error “destination port unreachable.” To troubleshoot the issue, you load your network analyzer tool, tcpdump, and attempt to load the webpage again. To load the webpage, your browser sends a query to a DNS server via the UDP protocol to retrieve the IP address for the website's domain name; this is part of the DNS protocol. Your browser then uses this IP address as the destination IP for sending an HTTPS request to the web server to display the webpage  The analyzer shows that when you send UDP packets to the DNS server, you receive ICMP packets containing the error message: “udp port 53 unreachable.” 
![LKXsnNIhT0e1mAz5AEvxog_d363c94e0a4f4a8b90b0be403f6ee1f1_mMBaLWLyXG2omYBcSdjuR8y5_S59zow1ZEPYdjNyJzA1B0r55nI9KmDosI8QHXcEwE51NxM3N5gNtMgSOyVDHyJVLZvZA7_jJtkzUKfxuqFUJPHs57vVVES-LbG5teR8eir4idaqsxFaYJhhVJZn-a_S-txb](https://github.com/marufrahmangit/cybersecurity-portfolio/assets/25085219/a240d107-b471-4780-bab3-20d3da43d581)

In the DNS and ICMP log, you find the following information:

1. In the first two lines of the log file, you see the initial outgoing request from your computer to the DNS server requesting the IP address of yummyrecipesforme.com. This request is sent in a UDP packet.

2. Next you find timestamps that indicate when the event happened. In the log, this is the first sequence of numbers displayed. For example: 13:24:32.192571. This displays the time 1:24 p.m., 32.192571 seconds.

3. The source and destination IP address is next. In the error log, this information is displayed as: 192.51.100.15.52444 > 203.0.113.2.domain. The IP address to the left of the greater than (>) symbol is the source address. In this example, the source is your computer’s IP address. The IP address to the right of the greater than (>) symbol is the destination IP address. In this case, it is the IP address for the DNS server: 203.0.113.2.domain.

4. The second and third lines of the log show the response to your initial ICMP request packet. In this case, the ICMP 203.0.113.2 line is the start of the error message indicating that the ICMP packet was undeliverable to the port of the DNS server.

5. Next are the protocol and port number, which displays which protocol was used to handle communications and which port it was delivered to. In the error log, this appears as: udp port 53 unreachable. This means that the UDP protocol was used to request a domain name resolution using the address of the DNS server over port 53. Port 53, which aligns to the .domain extension in 203.0.113.2.domain, is a well-known port for DNS service. The word “unreachable” in the message indicates the message did not go through to the DNS server. Your browser was not able to obtain the IP address for yummyrecipesforme.com, which it needs to access the website because no service was listening on the receiving DNS port as indicated by the ICMP error message “udp port 53 unreachable.”

The remaining lines in the log indicate that ICMP packets were sent two more times, but the same delivery error was received both times.

Now that you have captured data packets using a network analyzer tool, it is your job to identify which network protocol and service were impacted by this incident. Then, you will need to write a follow-up report. 

As an analyst, you can inspect network traffic and network data to determine what is causing network-related issues during cybersecurity incidents. Later in this course, you will demonstrate how to manage and resolve incidents. For now, you only need to analyze the situation. 

This event, in the meantime, is being handled by security engineers after you and other analysts have reported the issue to your direct supervisor. 

## Provide a summary of the problem found in the DNS and ICMP traffic log.
The UDP protocol reveals that port 53 is unreachable. This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message `UDP port 53 is unreachable`. The port noted in the error message is used for the DNS server. Since port 53 is associated with DNS protocol traffic, we know this is an issue with the DNS server. Due to the ICMP error response message about port 53, it is highly likely that the DNS server is not responding. This assumption is further supported by the flags associated with the outgoing UDP message and domain name retrieval.

## Explain your analysis of the data and provide at least one cause of the incident.
The incident occurred at 1:24 p.m. Customers notified that they received the message “destination port unreachable” when they attempted to visit the website yummyrecipesforme.com. The cybersecurity team providing IT services to the client is investigating the issue so customers can access the website again. In our investigation, we conducted packet sniffing tests using `tcpdump`. In the resulting log file, we found that DNS port 53 was unreachable. The next step is to identify whether the DNS server is down or traffic to port 53 is blocked by the firewall. The DNS server might be down due to a successful Denial of Service (DoS) attack or a misconfiguration. 
