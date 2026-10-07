# VPN Fundamentals – Day 18

**Internship:** Veda Technology | **Domain:** Cyber Security | **Task:** 18 (Level 1)
**Tools:** Browser, Google Docs

## 1. Objective
Understand secure remote connectivity by studying VPN architecture and how VPNs protect traffic over untrusted networks.

## 2. What is a VPN?
A **Virtual Private Network (VPN)** creates an encrypted tunnel between a user's device and a VPN server. Traffic passes through this tunnel, so anyone between the two points (public Wi-Fi owner, ISP, attacker on the network) sees only unreadable data.

## 3. How a VPN Works
1. The user's device (VPN client) connects to a VPN server.
2. Both sides authenticate (password, certificate, or key).
3. They negotiate encryption keys.
4. Each data packet is encrypted and wrapped inside another packet (**tunneling / encapsulation**).
5. The VPN server decrypts the packet and forwards it to the destination, using the server's IP address.
6. Responses return to the server, are re-encrypted, and sent back to the user.

Without VPN:  Device -> Wi-Fi/ISP -> Website  (traffic and IP visible)
With VPN:     Device ==encrypted tunnel==> VPN Server -> Website

## 4. Why VPNs Are Used
- Securing data on public Wi-Fi (cafes, airports)
- Secure remote access to company networks
- Connecting branch offices (site-to-site)
- Hiding the real IP address from websites
- Preventing ISP-level snooping
- Accessing geo-restricted content

## 5. Types of VPN
| Type | Purpose |
|------|---------|
| Remote-access VPN | One user connects securely to a private network |
| Site-to-site VPN | Connects two or more office networks |
| SSL/TLS VPN | Works through a web browser or TLS client |
| IPsec VPN | Network-layer encryption, common in enterprises |

## 6. Common VPN Protocols
| Protocol | Notes |
|----------|-------|
| OpenVPN | Open source, secure, widely used |
| WireGuard | Modern, fast, simple code |
| IPsec/IKEv2 | Stable, good for mobile |
| L2TP/IPsec | Older, moderate security |
| PPTP | Outdated and insecure, avoid |

## 7. VPN Encryption vs Anonymity
A VPN provides **encryption in transit** between the device and the VPN server. It does **not** provide complete anonymity.

**What a VPN does:**
- Encrypts traffic on untrusted networks
- Hides your real IP address from websites
- Hides browsing content from the local network and ISP

**What a VPN does NOT do:**
- The VPN provider can still see traffic metadata, so you must trust it
- Websites can still identify you via logins, cookies, and browser fingerprinting
- It does not protect against malware or phishing
- DNS or WebRTC leaks can expose real activity
- Traffic beyond the VPN server is protected only if the site uses HTTPS

## 8. Limitations
- Slight speed reduction from encryption overhead
- Trust is shifted from the ISP to the VPN provider
- Free VPNs may log or sell user data
- Misconfiguration can leak traffic

## 9. Best Practices
- Use trusted providers with a clear no-logs policy
- Prefer WireGuard or OpenVPN
- Enable the kill switch
- Test for DNS leaks
- Combine with HTTPS, MFA, and updated software

## 10. Interview Questions
**Q1. What is a VPN?**
A technology that creates an encrypted tunnel over an untrusted network to secure data and mask the user's IP address.

**Q2. Why are VPNs used?**
For privacy on public networks, secure remote work access, connecting office networks, and avoiding location restrictions.

**Q3. Does a VPN provide complete anonymity?**
No. It encrypts traffic and hides the IP, but the provider, cookies, accounts, and fingerprinting can still identify a user.

## 11. Conclusion
VPNs are a key tool for secure remote connectivity. They protect data in transit, but they work best as one layer of a wider security approach, not as a guarantee of anonymity.
