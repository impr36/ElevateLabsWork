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
- Capture start time: `2025-10-27 18:28:14`
- Capture end time: `2025-10-27 18:29:01`
- Duration: `47`
- Total packets captured: `[100]`
- Interface used: `[interface]`
- Capture method: `[Wireshark GUI]`
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

- Open in Wireshark and view:
- `Statistics → Protocol Hierarchy`
- `Statistics → Conversations`
- Useful display filters:
- `dns`, `http`, `tls`, `tcp`, `icmp`, `arp`

## 8. Conclusion & recommendations
- Summary: `[short summary of what you found — e.g., "DNS, ICMP, HTTP and TLS traffic seen; no suspicious traffic observed"]`
- Recommendations:
- Use `tcpdump`/`tshark` for automated captures.
- Capture longer traffic if investigating intermittent issues.
- If suspicious traffic is found, correlate with logs (firewall, IDS).

## 9. Appendix
- Filters used:
- `dns`, `http`, `icmp`, `tcp`, `tls`, `arp`
- Capture file: `capture_task5.pcap` (attached in repo)
- Screenshots:
- `protocol_hierarchy.png`
- `tcp_stream_example.png`

## 10. Key Concepts

```
Packet capture, protocol analysis, TCP/IP, network troubleshooting, filtering
```


**© 2025 Pratyush Raj — ElevateLabs Pvt. Ltd. Cyber Security Internship**
