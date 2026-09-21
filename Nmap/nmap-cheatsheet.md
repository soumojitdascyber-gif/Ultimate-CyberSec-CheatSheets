# 🔍 The Ultimate Nmap Command Vault (Pro Edition)

An exhaustive, professional guide to Network Mapping (Nmap). This cheat sheet covers basic host discovery, every specific port scanning technique, advanced firewall evasion, idle scanning, timing controls, and lethal red-team combinations. Maintained for Penetration Testers, Ethical Hackers, and SOC Analysts.

---

## 🟢 1. Target Specification & Host Discovery (Ping Sweep Variations)
*Different ways to find live hosts depending on how the network blocks ping requests.*

```bash
nmap <TARGET-IP>                 # Single Target: Scans a single IP address.
nmap <START-IP>-<END-IP>         # Range Scan: Scans a range of IP addresses.
nmap <TARGET-SUBNET>/24          # CIDR Subnet Scan: Scans an entire subnet (256 hosts).
nmap -iL <TARGET-LIST.txt>       # Input List: Scans a list of target IPs provided in a text file.
nmap --exclude <IP1,IP2>         # Exclude Hosts: Excludes specific IPs from the scan range.
nmap -sn <TARGET-SUBNET>         # Ping Sweep (No Port Scan): Discovers live hosts without scanning ports.
nmap -Pn <TARGET-IP>             # Skip Ping: Treats host as online. Crucial for bypassing firewalls blocking ICMP.
nmap -PR <TARGET-SUBNET>         # ARP Ping: Extremely fast and reliable for local network discovery.
nmap -PS22,80,443 <TARGET-IP>    # TCP SYN Ping: Sends SYN packets to specific ports to discover hosts.
nmap -PA80,443 <TARGET-IP>       # TCP ACK Ping: Sends ACK packets to bypass stateful firewalls blocking SYN.
nmap -PU53,161 <TARGET-IP>       # UDP Ping: Sends UDP packets to bypass TCP-only firewalls.
nmap -PE <TARGET-IP>             # ICMP Echo Ping: Standard ping request (often blocked).
