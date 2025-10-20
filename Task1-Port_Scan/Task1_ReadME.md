Task 1 — Local Network Open Ports Scan

Author: Pratyush Raj

Date: 20-10-2025

Network scanned: 192.168.1.0/24

Outcome reflection

Developed basic network reconnaissance skills; gained practical experience discovering live hosts on a subnet and preparing for deeper port/service scans to analyze service exposure.

1\. Summary

Scan type: Host discovery (ping) scan only (nmap -sn). No port/service probing was performed in this run.

Total IPs scanned: 256.

Live hosts found: 4 (192.168.1.1, 192.168.1.3, 192.168.1.4, 192.168.1.5).

High-risk findings: None detected yet — this run only confirmed which hosts are online. Perform a TCP SYN (-sS) and -sV scan next to enumerate open ports and services.

2\. Commands used (as executed)

Host discovery (as in screenshot):

nmap -sn 192.168.1.0/24 -oN port\_scan.txt

(Recommended next steps — run after you confirm hosts)

sudo nmap -sS -T4 --open 192.168.1.0/24 -oA scans/network\_scan

sudo nmap -sS -sV -p- \-oN scans/host-\-sv.txt

3\. Top hosts (from this host discovery scan)

Note: these entries record what nmap -sn reported (IP, MAC if shown). No ports/services were discovered in this scan.

192.168.1.1 — vendor: ZTE (MAC: F4:F6:47:71:03:E0)

Observed: Host is up. MAC vendor string shown as zte.

Likely device: Router / ISP gateway or a ZTE device.

Next step: run sudo nmap -sS -sV -p- 192.168.1.1 to check for management ports (HTTP, HTTPS, SSH, etc.).

Recommendation (preliminary): Do not expose admin interfaces to WAN; ensure strong admin credentials and up-to-date firmware.

192.168.1.3 — vendor: Unknown (MAC: 52:04:2C:68:80:C1)

Observed: Host is up; MAC vendor reported as Unknown.

Likely device: Unknown (could be an IoT device, mobile, or other).

Next step: perform a service scan to identify open ports and services, then map to a device owner.

192.168.1.4 — vendor: Intel Corporate (MAC: 2C:7B:A0:8D:E6:63)

Observed: Host is up; MAC vendor Intel Corporate (commonly a laptop/desktop NIC).

Likely device: PC or laptop.

Next step: check for SSH, file sharing or remote desktop ports (e.g., 22, 445, 3389).

192.168.1.5 — vendor: (not shown)

Observed: Host is up (no MAC/vendor printed in this output).

Likely device: Could be smartphone, printer, or another host that suppressed MAC display (or scanned from different segment).

Next step: run targeted port scan to identify services.

4\. Risk summary & remediation (based on current scan)

Current risk: Unknown for services — host discovery only. No open ports were enumerated in this run.

Recommended actions:

Run TCP SYN (-sS) scans with --open and -sV service detection on the discovered hosts to enumerate ports and versions.

For each discovered service, evaluate necessity and exposure (close or restrict unused services).

Apply firewall rules to limit access to management ports (allow only trusted IPs).

Patch firmware/software for router and endpoints. Change default credentials on network devices.

5\. Artifacts (from this session)

Host discovery output (as shown): port\_scan.txt (contains nmap -sn results).

For further analysis (to create and include): scans/network\_scan.nmap, .xml, .gnmap (after running -sS), per-host scans/host-\-sv.txt, and optional captures/scan.pcapng if you capture traffic in Wireshark.

6\. Next immediate commands to run (copy-paste)

Run these one-by-one after you confirm you have permission and are ready to enumerate services:

Fast SYN scan across subnet (shows only hosts with open ports):

sudo nmap -sS -T4 --open 192.168.1.0/24 -oA MainRepo/Task1-Port-Scan/scans/network\_scan

Service/version detection on a specific host (replace ):

sudo nmap -sS -sV -p- \-oN MainRepo/Task1-Port-Scan/scans/host-\-sv.txt

(Optional) If a device appears to run UDP services (DNS, SNMP), run a selective UDP check:

sudo nmap -sU -p 53,161 192.168.1.3 -oN MainRepo/Task1-Port-Scan/scans/udp-192.168.1.3.txt
