

This project presents a malware investigation conducted as part of the **Google Cybersecurity Professional Certificate**. The objective was to investigate a security incident involving a compromised website, identify the network protocols used during the attack, and document the malicious activity that redirected users to a fake website containing malware.

## 🎯 Scenario

You are a cybersecurity analyst for **yummyrecipesforme.com**, a website that sells recipes and cookbooks. A former employee executed a brute force attack to gain admin access and embedded malicious JavaScript code in the website. When customers visit the site, they are prompted to download a file that redirects them to a fake website (**greatrecipesforme.com**) containing malware. Multiple customers reported slow computer performance after downloading the file.

## 🔍 Applied Methodology

- **Tool**: tcpdump (network protocol analyzer) in sandbox environment
- **Approach**: Network traffic capture during malicious website interaction
- **Protocols Analyzed**: DNS requests and HTTP traffic patterns
- **Focus**: Website redirection analysis and malware delivery investigation

## 📊 Key Findings

### **Attack Identified: Website Compromise with Malware Distribution**

**Technical Details:**

- Original website: yummyrecipesforme.com (IP: 203.0.113.22)
- Malicious redirect to: greatrecipesforme.com (IP: 192.0.2.17)
- Attack vector: Brute force on admin account using default passwords
- Malware delivery: JavaScript-prompted executable file download

**Traffic Pattern:**

- DNS resolution for yummyrecipesforme.com
- HTTP GET requests to legitimate website
- Malicious file download execution
- DNS resolution and redirect to greatrecipesforme.com
- HTTP traffic to fake malicious website

## 🎯 Analysis Results

The investigation revealed that a former employee compromised the website through a brute force attack on the admin account. The attacker embedded malicious JavaScript that prompted users to download malware disguised as a browser update, which then redirected victims to a fake website hosting additional malicious content.

## 📁 Documentation

- **Incident Report**: Complete analysis with protocol identification and attack documentation
- **tcpdump Logs**: Network traffic showing DNS requests and HTTP redirections between legitimate and malicious websites
- **Attack Timeline**: Detailed sequence of events from initial compromise to malware distribution
- **Security Recommendations**: Brute force attack prevention measures

## 💼 Skills Demonstrated

- Malware investigation and analysis
- Network protocol identification (DNS, HTTP)
- Sandbox environment security testing
- Attack vector analysis and documentation
- Brute force attack understanding and prevention
- Incident response and security recommendations