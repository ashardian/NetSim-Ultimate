# 🌐 RouterOS Ultimate: Network Simulator

![Project Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-MIT-blue)
![Technology](https://img.shields.io/badge/Tech-HTML5%20%7C%20JS%20%7C%20Canvas-orange)

**RouterOS Ultimate** is a high-fidelity, browser-based simulation of a consumer ISP router. It is designed to teach network concepts, port forwarding logic, and security awareness through an interactive, realistic interface.

Unlike static diagrams, this simulator features a **live traffic engine** where you can see packets travel, get blocked by firewalls, or successfully routed based on the rules you configure.

## 🚀 Key Features

### 🖥️ Realistic Interface
- **Authentic GUI:** Mimics modern router firmware (TP-Link/Asus/Ubiquiti style).
- **Persistent Memory:** Settings (SSID, Rules, IPs) are saved to your browser's LocalStorage.
- **System Simulation:** Includes realistic boot sequences, reboot delays, and login authentication.

### ⚙️ Advanced Networking Logic
- **Real-World Dependencies:** Changing the LAN IP subnet (e.g., from `192.168.0.1` to `10.0.0.1`) **breaks** existing Port Forwarding rules, simulating real configuration errors.
- **Stateful Packet Inspection:** Visual feedback on why packets are dropped (Subnet Mismatch, No Rule, Firewall Block).
- **Diagnostic Tools:** Functional Ping and Traceroute simulations that interact with the visualizer.

### 🛡️ Security Education
- **"Hacker's View":** A toggleable mode that explains the security risks of specific settings (e.g., exposing Port 3389).
- **Traffic Visualizer:** A built-in "Canvas" engine that renders HTTP, SSH, and ICMP traffic flows in real-time.
- **Attack Simulation:** Generate random "Attack Traffic" to test your firewall rules.

---

## 🎮 How to Use

### Installation
No installation required! This is a client-side application.
1. Download the `RouterOS-Ultimate.html` file from this repository.
2. Open it in any modern web browser (Chrome, Edge, Firefox).

### Default Credentials
To access the admin dashboard:
- **Username:** `admin`
- **Password:** `admin`

### Scenarios to Try
1.  **The Web Server:** Forward Port 80 to `192.168.0.100`. Use the "Test HTTP" button to see green packets flow.
2.  **The Broken Subnet:** Go to LAN settings, change the IP to `10.0.0.1`, and Reboot. Notice how your old Port 80 rule now fails because the subnet doesn't match.
3.  **The Firewall Test:** Delete all rules and click "Random Attack". Watch the firewall block unauthorized inbound traffic by default.

---

## 🛠️ Technical Details

- **Single-File Architecture:** The entire app (CSS, HTML, JS engine) is contained in one file for portability.
- **Canvas API:** Uses HTML5 Canvas for the physics-based packet animation.
- **LocalStorage API:** Simulates non-volatile memory (NVRAM).

## 🤝 Contributing

Pull requests are welcome! If you'd like to improve the packet physics, add IPv6 support, or design new skins:

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

---
*Created for educational purposes to demonstrate NAT, Port Forwarding, and Network Security concepts.*
