# Task 5 — Capture and Analyze Network Traffic Using Wireshark

**Date:** 27-10-2025 
**Environment:** Kali Linux VM ([Kali version]) — Interface captured: `[interface name]` (e.g., eth0, wlan0)

---

## 1. Objective
Capture live network packets and identify basic protocols and traffic types using Wireshark.

## 2. Tools & Setup
- Wireshark version: `[wireshark --version output or install version]`
- tshark / tcpdump (optional)
- System user: `[your username]`
- Capture file: `capture_task5.pcap`

## 3. Capture Details
- Capture start time: `[YYYY-MM-DD HH:MM:SS]`
- Capture end time: `[YYYY-MM-DD HH:MM:SS]`
- Duration: `[seconds]`
- Total packets captured: `[N]`
- Capture file size: `[e.g., 1.2 MB]`
- Interface used: `[interface]`
- Capture method: `[Wireshark GUI / tshark / tcpdump]`
- Capture filename: `capture_task5.pcap` (attached)

## 4. Steps performed
1. Installed Wireshark and configured non-root capture.
2. Selected interface `[interface]` and started capture.
3. Generated traffic:
   - `ping -c 5 8.8.8.8`
   - `curl -I http://example.com`
   - `dig google.com`
   - Visited `[site1]`, `[site2]`
4. Stopped capture after ~[60] seconds and saved as `capture_task5.pcap`.
5. Analyzed capture using Wireshark Statistics and filters.

## 5. Protocols identified (at least 3)
| Protocol | Filter used | Packet count (approx.) | Notes / Evidence (frame numbers) |
|---|---:|---:|---|
| DNS | `dns` | `[e.g., 15]` | Example: Frame 12 — DNS query for `google.com`. |
| ICMP | `icmp` | `[e.g., 6]` | Example: Frame 3 — Echo (ping) request to 8.8.8.8. |
| HTTP / TLS | `http` / `tls` | `[e.g., 20 / 40]` | Example: Frame 45 — HTTP GET / Frame 66 — TLS Client Hello to `server:443`. |
*(Add other protocols you observed: ARP, TCP, DHCP, SSDP, etc.)*

## 6. Notable packets/findings
- **Frame [#]** — `[protocol]` — Summary: `[e.g., HTTP GET /index.html to example.com — 200 OK]`
- **Frame [#]** — `[protocol]` — Summary: `[e.g., TLS Client Hello — server certificate exchange]`
- Any suspicious or unexpected traffic: `[none / describe if present]`

## 7. Analysis procedure (how to reproduce)
- Capture:
