# SOC Incident Report: Multi-Stage Attack Detection
**Analyst:** [Arivazhagan] | **Date:** Feb 5, 2026 | **Status:** RESOLVED

---

## 1. Executive Summary
Between 07:00 and 14:00, the environment was subjected to a coordinated attack. I identified a "low-and-slow" brute force entry followed by an attempt at persistence. 

## 2. Phase I: Initial Detection (Dashboard View)
I utilized the Wazuh dashboard to identify anomalies in login behavior over a 24-hour period.

<div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
  <div style="text-align: center;">
    <img src="BF_1.png" width="350" alt="Total Alerts"><br>
    <sub><b>Total Alerts (24h)</b></sub>
  </div>
  <div style="text-align: center;">
    <img src="BF_2.png" width="350" alt="Pie Chart Distribution"><br>
    <sub><b>Alert Distribution</b></sub>
  </div>
</div>

---

## 3. Phase II: Brute Force Analysis (Rule 5712)
By drilling down into **Rule ID 5712**, I isolated the attacker's traffic. The pie chart and event list confirm a sustained brute force attempt against the SSH service.

<div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
  <div style="text-align: center;">
    <img src="BF_4.png" width="300" alt="Rule 5712 Pie"><br>
    <sub><b>Rule 5712 Ratio</b></sub>
  </div>
  <div style="text-align: center;">
    <img src="BF_5.png" width="300" alt="Rule 5712 Events"><br>
    <sub><b>Event Timeline</b></sub>
  </div>
  <div style="text-align: center;">
    <img src="BF_3.png" width="300" alt="Detailed Events"><br>
    <sub><b>Detailed Log List</b></sub>
  </div>
</div>

---

## 4. Phase III: Attacker Attribution (Source IP)
I identified the malicious Source IP and verified the specific system calls used during the exploit phase.

<div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
  <div style="text-align: center;">
    <img src="BF_6.png" width="450" alt="Event Description"><br>
    <sub><b>Technical Event Description</b></sub>
  </div>
  <div style="text-align: center;">
    <img src="BF_7.png" width="450" alt="IP Filtering"><br>
    <sub><b>Filtering Attacker IP: 10.48.156.247</b></sub>
  </div>
</div>

---

## 5. Challenges & CLI Forensics
- **SIEM Delay:** The dashboard lagged on User Creation (Rule 5902).
- **Resolution:** I pivoted to CLI forensics, using `grep` on `/var/log/auth.log` to confirm the creation of the `persistence_user`.

> **Analyst Note:** This attack successfully bypassed standard rate-limiting by using a 10-minute delay between attempts. Hardening recommendations include disabling Root SSH and implementing stricter account lockout policies.

---
*Next Step: Investigating Lateral Movement signatures (Work in Progress)*
