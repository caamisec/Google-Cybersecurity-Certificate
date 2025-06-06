This project presents a network traffic analysis conducted as part of the **Google Cybersecurity Professional Certificate**. The objective was to analyze DNS and ICMP traffic using network protocol analyzer data to identify which network protocol was affected during a cybersecurity incident.

## 🎯 Scenario

You are a cybersecurity analyst working at a company that provides IT services for clients. Several customers reported they could not access the client website **[www.yummyrecipesforme.com](http://www.yummyrecipesforme.com)** and received "destination port unreachable" errors. The analyst was tasked with investigating the network connectivity issue and determining the root cause.

## 🔍 Applied Methodology

- **Tool**: tcpdump (network protocol analyzer)
- **Approach**: Packet capture and analysis during website access attempts
- **Protocols Analyzed**: UDP (DNS requests) and ICMP (error responses)
- **Focus**: Network layer communication in the TCP/IP model

## 📊 Key Findings

### **Issue Identified: DNS Service Unavailable**

**Technical Details:**

- DNS server IP: 203.0.113.2
- Affected port: Port 53 (DNS service)
- Error message: "udp port 53 unreachable"
- Time of incident: 13:24 - 13:28 (1:24 PM - 1:28 PM)

**Traffic Pattern:**

- UDP packets sent from client (192.51.100.15) to DNS server
- ICMP error responses received indicating port unreachable
- Multiple attempts resulted in the same error

## 🎯 Analysis Results

The investigation revealed that the DNS service on the server was not responding to requests on port 53, preventing domain name resolution and causing website access failures for all clients.

## 📁 Documentation

- **Incident Report**: Complete analysis with problem summary and root cause assessment
- **tcpdump Logs**: Raw packet capture data showing UDP requests and ICMP error responses
- **Timeline**: Detailed timestamp analysis of the incident progression

## 💼 Skills Demonstrated

- Network protocol analysis (UDP, ICMP, DNS)
- Packet capture interpretation using tcpdump
- Incident investigation and documentation
- Root cause analysis for network connectivity issues
- Understanding of TCP/IP model and network troubleshooting