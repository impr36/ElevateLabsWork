# Task 1 — Local Network Open Ports Scan

**Author:** Pratyush Raj  
**Date:** 20-10-2025  
**Network scanned:** 192.168.1.0/24  

---

## 1. Summary

Scanned 256 IPs, found 4 live hosts. High-risk findings: None detected in this host-discovery run (no port/service enumeration performed). This run was a host discovery (ping) scan only. Perform TCP SYN (-sS) and -sV scans next to enumerate open ports and services.

---  

## Structure

Task1-Port_Scan/  
│  
├── 📂 Captures/  
│   ├── IP_addr.png  
│   ├── NMap.png  
│   ├── Wireshark01.png  
│   ├── Wireshark02.png  
│   ├── ifconfig.png  
│   └── port192.168.1.4.pcapng  
│  
├── 📂 Others/  
│   ├── Common_mapping.txt  
│   ├── Interview-Questions.txt  
│   └── Nmap_Cheat-Sheet.txt  
│  
├── 📂 Reports/  
│   └── Task 1.pdf  
│  
├── 📂 Scans/  
│   ├── UDP-Scan.txt  
│   ├── host-192.168.1.1-sv.txt  
│   ├── host-192.168.1.3-sv.txt  
│   ├── host-192.168.1.4-sv.txt  
│   ├── host-192.168.1.5-sv.txt  
│   ├── network_scan.gnmap  
│   ├── network_scan.nmap  
│   ├── network_scan.xml  
│   └── port_scan.txt  
│  
├── Task1_ReadME.md  
  
---  

## 2. Commands used

* `nmap -sn 192.168.1.0/24 -oN port_scan.txt`

(Recommended next steps — run after you confirm hosts)

* `sudo nmap -sS -T4 --open 192.168.1.0/24 -oA ElevateLabsWork/Task1-Port-Scan/scans/network_scan`
* `sudo nmap -sS -sV -p- 192.168.1.1 -oN ElevateLabsWork/Task1-Port-Scan/scans/host-192.168.1.1-sv.txt`
* (optional) `sudo nmap -sU -p 53,161 192.168.1.4 -oN ElevateLabsWork/Task1-Port-Scan/scans/udp-192.168.1.4.txt`

---

## 3. Top hosts (from this host discovery scan)

> Note: these entries record what `nmap -sn` reported (IP, MAC if shown). No ports/services were discovered in this scan.

### 192.168.1.1 — Vendor: ZTE (MAC: F4:F6:47:71:03:E0)

* Observed: Host is up. MAC vendor string shown as ZTE.
* Likely device: Router / ISP gateway (ZTE device).
* Next step: `sudo nmap -sS -sV -p- 192.168.1.1` to check for management ports (HTTP, HTTPS, SSH, etc.).
* Recommendation (preliminary): Do not expose admin interfaces to WAN; ensure strong admin credentials and up-to-date firmware.

### 192.168.1.5 — Vendor: Unknown (MAC: 52:04:2C:68:80:C1)

* Observed: Host is up; MAC vendor reported as Unknown.
* Likely device: Could be an IoT device, mobile, or other.
* Next step: perform a service scan to identify open ports and services, then map to a device owner.

### 192.168.1.4 — Vendor: Intel Corporate (MAC: 2C:7B:A0:8D:E6:63)

* Observed: Host is up; MAC vendor Intel Corporate (commonly a laptop/desktop NIC).
* Likely device: PC or laptop.
* Next step: check for SSH, file sharing, or remote desktop ports (e.g., 22, 445, 3389).

### 192.168.1.3 — Vendor: (not shown)

* Observed: Host is up (no MAC/vendor printed in this output).
* Likely device: Could be a smartphone, printer, or another host that suppressed MAC display.
* Next step: run a targeted port scan to identify services.

---

## 4. Risk summary & remediation

* **Current risk:** Unknown for services — host discovery only. No open ports were enumerated in this run.

**Recommended actions:**

* Run TCP SYN (`-sS`) scans with `--open` and `-sV` service detection on the discovered hosts to enumerate ports and versions.
* For each discovered service, evaluate necessity and exposure (close or restrict unused services).
* Apply firewall rules to limit access to management ports (allow only trusted IPs).
* Patch firmware/software for router and endpoints. Change default credentials on network devices.

---

## 5. Artifacts

* Host discovery output: `port_scan.txt` (contains `nmap -sn` results).
* After service scans (to be generated): `ElevateLabsWork/Task1-Port-Scan/scans/network_scan.nmap`, `.xml`, `.gnmap`.
* Per-host service output (example): `ElevateLabsWork/Task1-Port-Scan/scans/host-192.168.1.1-sv.txt`.
* Optional packet capture (if performed): `captures/scan.pcapng`.

---

## 6. Next immediate commands to run (copy-paste)

Run these one-by-one after you confirm you have permission and are ready to enumerate services:

**Fast SYN scan across subnet (shows only hosts with open ports):**

```
sudo nmap -sS -T4 --open 192.168.1.0/24 -oA ElevateLabsWork/Task1-Port_Scan/scans/network_scan
```

**Service/version detection on a specific host (replace <IP>):**

```
sudo nmap -sS -sV -p- -oN ElevateLabsWork/Task1-Port-Scan/scans/host-<IP>-sv.txt <IP>
```

**(Optional) Selective UDP check for DNS/SNMP on a single host:**

```
sudo nmap -sU -p 53,161 192.168.1.4 -oN ElevateLabsWork/Task1-Port_Scan/scans/udp-192.168.1.4.txt
```

---

**Outcome reflection**
Developed basic network reconnaissance skills; gained practical experience discovering live hosts on a subnet and preparing for deeper port/service scans to analyze service exposure.
