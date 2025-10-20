# Task 1 — Local Network Open Ports Scan
**Author:** <Your Name>  
**Date:** YYYY-MM-DD  
**Network scanned:** 192.168.1.0/24

---

## 1. Summary
Scanned X IPs, found Y hosts with open ports. High-risk findings: [list e.g., Telnet on 192.168.1.5, MySQL exposed on 192.168.1.12].

---

## 2. Commands used
- `nmap -sn 192.168.1.0/24 -oN scans/hosts-scan.txt`
- `sudo nmap -sS -T4 --open 192.168.1.0/24 -oA scans/network_scan`
- `sudo nmap -sS -sV -p- 192.168.1.10 -oN scans/host-192.168.1.10-sv.txt`
- (optional) `sudo nmap -sU -p 53,123,161 192.168.1.0/24 -oN scans/udp_scan.txt`

---

## 3. Top hosts (examples — replace with your findings)
### 192.168.1.10 — Router
- Open ports: 80/tcp (HTTP), 443/tcp (HTTPS)
- Risk: HTTP should redirect to HTTPS; ensure firmware is updated.
- Recommendation: disable admin on WAN, change default creds.

### 192.168.1.15 — Laptop
- Open ports: 22/tcp (SSH)
- Risk: low if key-based auth; check for password auth.
- Recommendation: enforce key auth, restrict IPs via firewall.

(Repeat for other hosts)

---

## 4. Risk summary & remediation
- Close unused services.
- Restrict admin ports to trusted IPs using firewall.
- Replace plaintext services (Telnet/FTP) with secure alternatives.
- Patch outdated software/firmware.

---

## 5. Artifacts
- `scans/network_scan.nmap`, `.xml`, `.gnmap`
- `scans/host-*.txt`
- `captures/scan.pcapng` (if captured)
