# SOC Incident Report: Multi-Stage Attack Detection

## 1. Initial Detection & Dashboard Overview
I began the investigation by reviewing the Wazuh dashboard for the last 24 hours. The initial surge in alerts indicated a potential brute-force attempt.

**[Image 1: Total Alerts Dashboard]**
![Dashboard Overview](BF_1.png)

**[Image 2: Alert Distribution]**
The Pie Chart reveals that Rule 5712 (SSHD Brute Force) accounts for a significant portion of the telemetry.
![Pie Chart Overview](BF_2.png)

---

## 2. Deep Dive: Brute Force Analysis (Rule 5712)
By filtering specifically for **Rule ID: 5712**, I isolated the malicious traffic from the background noise.

**[Images 4 & 5: Rule 5712 Analysis]**
The data shows a "Low-and-Slow" attack pattern designed to bypass simple threshold alerts.
![Rule 5712 Pie Chart](BF_4.png)
![Rule 5712 Events List](BF_5.png)

---

## 3. Threat Actor Attribution & Technical Details
I pivoted to the event details to identify the Source IP and the targeted destination.

**[Image 6 & 7: Attacker Identification]**
* **Attacker IP:** `10.48.156.247`
* **Target:** SSH Service
* **Method:** Automated credential stuffing

![Event Description Details](BF_6.png)
![Source IP Filtering](BF_7.png)

---

## 4. Forensic Evidence (CLI Pivot)
Because SIEM dashboards can sometimes lag, I verified the activity directly on the host using the `auth.log`. This confirmed the creation of the `persistence_user` backdoor.

**[Image 3: Detailed Event Logs]**
![Raw Log Evidence](BF_3.png)

