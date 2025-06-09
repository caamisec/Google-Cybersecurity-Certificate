This project presents a network attack analysis conducted as part of the **Google Cybersecurity Professional Certificate**. The objective was to identify and analyze a security incident affecting a company's website, determine the type of network attack, and assess its impact on business operations.

## 🎯 Scenario

You work as a security analyst for a travel agency that advertises sales and promotions on the company's website. Employees regularly access the sales webpage to search for vacation packages. One afternoon, an automated alert indicated a problem with the web server, and attempts to visit the website resulted in connection timeout errors. Investigation revealed suspicious network traffic patterns requiring immediate analysis and response.

## 🔍 Applied Methodology

- **Tool**: Packet sniffer and Wireshark log analysis
- **Approach**: Network traffic pattern analysis and attack identification
- **Focus**: TCP SYN request monitoring and server response analysis
- **Response**: Immediate server protection and firewall configuration

## 📊 Key Findings

### **Attack Identified: SYN Flood Attack (DoS)**

**Technical Details:**

- Large volume of TCP SYN requests from unfamiliar IP address
- Web server overwhelmed by abnormal traffic volume
- Server unable to respond to legitimate requests
- Connection timeout errors for all users

**Attack Characteristics:**

- TCP three-way handshake exploitation
- Server resources exhausted by incomplete connections
- Website inaccessibility for employees and customers
- Automated monitoring system triggered alerts

## 🎯 Analysis Results

The investigation revealed a SYN flood attack targeting the company's web server. The attacker sent numerous TCP SYN requests without completing the handshake, consuming server resources and preventing legitimate users from accessing the website. This attack disrupted business operations and customer access to travel packages.

## 📁 Documentation

- **Incident Report**: Complete analysis with attack identification and impact assessment
- **Wireshark Logs**: Network traffic data showing abnormal SYN request patterns
- **Response Actions**: Server recovery procedures and firewall configuration changes
- **Prevention Recommendations**: Security measures to prevent future attacks

## 💼 Skills Demonstrated

- Network attack identification and classification
- Packet analysis and traffic pattern recognition
- Incident response and mitigation strategies
- Security monitoring and alert investigation
- Firewall configuration and IP blocking implementation
- Business impact assessment and communication