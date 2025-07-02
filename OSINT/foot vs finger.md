#🔍 Footprinting (Information Gathering Phase)
Definition:
Footprinting is the first step in the process of ethical hacking or reconnaissance. It involves collecting as much information as possible about the target (an organization or system) to identify potential attack vectors.
---
##Purpose:

To build a complete profile of the target.

Understand the organization’s external and internal infrastructure.

Identify IP ranges, domain names, mail servers, and public-facing systems.

##Techniques:

Passive (without interacting with the target):

WHOIS lookup

DNS queries

Search engines (Google hacking)

Social engineering

Active (with minimal interaction):

Ping sweeps

Traceroute

Email harvesting

##Example:

Finding the target's IP address, domain registration info, employee emails, or technologies used on their website.

#🧬 Fingerprinting (Scanning Phase)
Fingerprinting is a more focused and technical process that follows footprinting. It identifies specific details about the systems, such as the operating system, software versions, services, and open ports.

##Purpose:

To identify system details and vulnerabilities.

Determine what software/services are running and how they might be exploited.

##Types:

###Active Fingerprinting:

Sending crafted packets to elicit responses (e.g., with Nmap).

###Passive Fingerprinting:

Observing network traffic without direct interaction (e.g., sniffing packets).

##Tools:

Nmap

Netcat

Xprobe

Wireshark

##Example:

Detecting that a web server is running Apache 2.4.57 on Ubuntu Linux.
---
