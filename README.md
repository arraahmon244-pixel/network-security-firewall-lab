#  Network Security Tools – Firewall Configuration Lab

##  Objective
The objective of this lab is to configure a basic firewall rule on a local server and test its effectiveness in blocking network traffic.

---

##  Tools Used
- UFW (Uncomplicated Firewall)
- Apache2 Web Server
- Nmap (Network Scanning Tool)
- Linux (Kali)

---

##  Firewall Configuration

The following steps were performed:

1. Enabled the firewall
2. Set default rules:
   - Deny all incoming traffic
   - Allow all outgoing traffic
3. Blocked port 80 (HTTP)
4. Allowed SSH access to maintain remote connectivity

---

##  Testing Procedure

### Before Applying Firewall Rule
- Apache server was started
- Accessed via system IP address using curl
- Result: Web page loaded successfully

Note: Testing was performed using the system’s IP address instead of localhost because firewall rules do not apply to loopback traffic.

....
### After Applying Firewall Rule
- Port 80 was blocked using UFW
- Attempted access again using curl
- Result: Connection failed

### Verification with Nmap
- Scanned port 80
- Result: Port state changed to "filtered"

---

## 📊 Results

| Test Phase        | Result        |
|------------------|--------------|
| Before Firewall  | Port 80 Open |
| After Firewall   | Port 80 Blocked |
| Nmap Scan        | Filtered     |

---

## 📸 Screenshots

All screenshots are available in the `/screenshots` folder, showing:
- Firewall setup
- Rule configuration
- Successful and failed connection tests
- Nmap verification

##  Security Insight

This experiment demonstrates that firewalls control external traffic but do not typically block internal loopback communication. Proper testing must therefore simulate external access using a real IP address.

---

##  Conclusion

The firewall configuration was successful. The system initially allowed access to the web server, but after applying the firewall rule, access to port 80 was blocked. This demonstrates how firewalls can be used to control and secure network traffic effectively.

---

## 👨‍💻 Author
Abdurrahmon
