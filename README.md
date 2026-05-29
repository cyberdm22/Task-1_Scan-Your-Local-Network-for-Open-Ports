# Elevate-Labs_Task-1
Task 1: Scan Your Local Network for Open Ports (Nmap/Wireshark)
# Elevate Labs Task 1: Network Reconnaissance

## Objective
Discovered open ports on devices within the local network to understand network exposure using Nmap.

## Interview Questions & Answers

**1. What is an open port?** An open port is a network endpoint where an application or service is actively listening for incoming connections and data packets.

**2. How does Nmap perform a TCP SYN scan?** It performs a "half-open" scan. Nmap sends a SYN packet to the target. If the port is open, the target replies with a SYN-ACK. Nmap then immediately sends an RST (Reset) packet to drop the connection before the TCP handshake completes, which makes the scan faster and stealthier.

**3. What risks are associated with open ports?** Open ports are the gateways to your infrastructure. If a service running on an open port is misconfigured or outdated, it acts as a direct vector for exploitation. For instance, an open port hosting a web application can expose the underlying server to critical application-layer vulnerabilities, such as Cross-Site Scripting (XSS), SQL injection (SQLi), or Server-Side Request Forgery (SSRF).

**4. Explain the difference between TCP and UDP scanning.** TCP scanning relies on the connection-oriented TCP handshake (ensuring packet delivery and clear responses), whereas UDP scanning sends connectionless packets. UDP scans are often slower because open UDP ports rarely send a response back, forcing the scanner to rely on ICMP timeout errors to infer the port's status.

**5. How can open ports be secured?** By implementing the principle of least privilege: disabling all unnecessary services, deploying robust firewalls to filter unauthorized traffic, and ensuring all actively listening services are authenticated and patched.

**6. What is a firewall's role regarding ports?** A firewall acts as a network gatekeeper, inspecting incoming and outgoing traffic against a set of predefined rules to either permit, drop, or reject connections to specific ports.

**7. What is a port scan and why do attackers perform it?** A port scan is a systematic method of probing a server or network for open ports. Attackers perform it during the initial reconnaissance phase to map the attack surface and identify running services that can be leveraged for initial access.

**8. How does Wireshark complement port scanning?** While Nmap acts as the active probe generating the traffic, Wireshark acts as the passive analyzer. It captures the raw packet exchange, allowing an analyst to verify the actual TCP flags being sent and troubleshoot firewall interference.
