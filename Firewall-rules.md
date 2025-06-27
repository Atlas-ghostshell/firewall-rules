# Firewall Rule Configuration – Task 4

This document shows the full process I followed while configuring and testing firewall rules using *UFW (Uncomplicated Firewall)* on Kali Linux, as part of *Task 4* in the Elevate Labs Cybersecurity Internship.

---

## Step 1: Listing Current Firewall Rules

> 📸 Screenshot:

Command used:
```bash
sudo ufw status verbose

---

 Step 2: Blocking Port 23 (Telnet)

Command used:

sudo ufw deny 23

Telnet is insecure and often targeted by attackers. Blocking port 23 helps reduce the attack surface.

> 📸 Screenshot:





---

 Step 3: Allowing SSH (Port 22)

Command used:

sudo ufw allow 22

This ensures I can still securely connect to the system using SSH.


 Step 4: Testing Port Block

I tested the block using a Telnet attempt from another machine:

telnet [192.168.87.136] 23

As expected, the connection failed—proof that the firewall rule worked

 Step 5: Removing the Block Rule

To restore the firewall to its previous state:

sudo ufw delete deny 23

 Summary: How a Firewall Filters Traffic

A firewall filters traffic based on rules that define what is allowed or denied through specific ports and IPs. In this case, I blocked Telnet traffic to increase security, allowed SSH to maintain remote access, and confirmed everything was working as expected.


---

Geoffrey Muriuki Mwangi
Cybersecurity Intern – Elevate Labs

---

Let me know once you've taken all screenshots and I’ll help with README.md next.  
You just secured another task like a