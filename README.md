# 🧪 Networking & Cloud Security Lab – Day 1

## 📅 Overview
Today’s lab focused on understanding core networking concepts in Linux and mapping them to Cloud Security principles.  
The goal was to observe how real network traffic, services, and security controls work at a low level.

---

# 🌐 1. Network Fundamentals

## 🔹 IP Configuration
- IP: `192.168.1.217/24`
- Network range: `192.168.1.0 – 192.168.1.255`
- Local network (LAN)

## 🔹 Default Gateway
- Gateway: `192.168.1.1`
- Acts as router between LAN and internet

## 🔹 Routing Table
- `ip route show`
- Shows:
  - local network routes
  - default route → gateway

---

# 📡 2. DNS (Name Resolution)

- Domain tested: `google.com`
- DNS resolved domain → IP addresses (IPv4 + IPv6)

👉 DNS translates human-readable names into machine IPs.

---

# 🔌 3. Connectivity Tests

## Ping
- Checked latency
- Verified packet delivery

## Traceroute
- Showed network path (hops)
- Demonstrated routing across multiple routers

---

# 🔗 4. TCP Fundamentals

Observed TCP 3-way handshake in Wireshark:

- SYN
- SYN-ACK
- ACK

👉 This is the foundation of reliable network communication.

---

# 🔐 5. TLS / HTTPS

Observed TLS 1.3 handshake:
- Client Hello
- Server Hello
- Encrypted Application Data

👉 After handshake, all traffic is encrypted.

---

# 🖥️ 6. Application Layer

- Web server: Apache Tomcat
- Port: `8080`
- Response: HTTP 200 OK
- Default web page served

---

# 🚪 7. Ports & Services

Active services observed:

- 22 → SSH
- 53 → DNS
- 3306 → MySQL
- 8080 → Tomcat

### LISTEN state
- `*:8080 LISTEN`

👉 Service is actively waiting for connections.

---

# 🌐 8. Network Exposure

| Interface | Meaning |
|----------|--------|
| 127.0.0.1:8080 | Local machine only |
| *:8080 | Accessible from network (LAN) |

---

# 🔥 9. Firewall (UFW)

- Rule observed: `8080/tcp DENY IN`

👉 Important concept:
> Service running ≠ Service accessible

Firewall controls inbound/outbound traffic regardless of running services.

---

# ☁️ 10. Cloud Security Mapping

| Linux Concept | AWS Equivalent |
|--------------|----------------|
| UFW Firewall | Security Groups |
| LAN Network | VPC Internal Network |
| Open Ports | Inbound Rules |
| Localhost Access | Private Instance Access |

---

# 🧠 11. Key Takeaways

- IP + subnet define network boundaries
- DNS resolves domains to IPs
- TCP establishes connections
- TLS encrypts traffic
- Ports define services
- Firewalls control access
- Cloud security is built on network control

---

# 🚀 Conclusion

This lab simulated a real cloud-like environment using a local Linux machine:

**Services + Network Traffic + Security Controls = Real-world cloud networking model**

This forms the foundation of cloud security and DevSecOps understanding.
