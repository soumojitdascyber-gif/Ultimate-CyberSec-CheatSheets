# 🔍 The Ultimate Nmap Command Vault

An exhaustive, professional guide to Network Mapping (Nmap). This cheat sheet covers everything from basic host discovery to advanced firewall evasion, idle scanning, and lethal red-team combinations. Maintained for Penetration Testers, Ethical Hackers, and SOC Analysts.

---

## 🟢 1. Target Specification & Host Discovery
*Methods to find live hosts on a network before launching loud port scans.*

```bash
nmap <TARGET-IP>                 # Single Target: Scans a single IP address.
nmap <START-IP>-<END-IP>         # Range Scan: Scans a range of IP addresses (e.g., 192.168.1.1-50).
nmap <TARGET-SUBNET>/24          # CIDR Subnet Scan: Scans an entire subnet (256 hosts).
nmap -iL <TARGET-LIST.txt>       # Input List: Scans a list of target IPs provided in a text file.
nmap -sn <TARGET-SUBNET>/24      # Ping Sweep (No Port Scan): Discovers live hosts purely via ICMP/ARP without scanning ports.
nmap -Pn <TARGET-IP>             # Skip Host Discovery (No Ping): Treats the host as online. Crucial for bypassing firewalls that block ICMP pings.
