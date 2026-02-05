# SOC Incident Report: Multi-Stage Attack Detection
**Analyst:** [Arivazhagan] | **Date:** February 5, 2026 | **Status:** RESOLVED

---

## 1. Executive Summary
Between 07:00 and 14:00, the monitored environment was subjected to a coordinated attack lifecycle. I identified the entry point as a "low-and-slow" SSH brute force attack, followed by an unauthorized user creation for persistence.

---

## 2. Attack Phase: Brute Force (SSH)
**Summary:** Identified 69 failed authentication events from IP `10.48.156.247`. The attacker utilized a throttled cadence (1 attempt every 10 minutes) to evade standard rate-limiting.

<div style="display: flex; overflow-x: auto; gap: 20px; padding-bottom: 25px; border: 1px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9;">

  <div style="flex: 0 0 450px; text-align: center;">
    <p style="font-weight: bold; color: #2c3e50; margin-bottom: 2px;">1. Dashboard Overview</p>
    <p style="font-size: 0.8em; color: #666; margin-bottom: 10px;">(Click to view full size)</p>
    <a href="BF_1.png" target="_blank">
      <img src="BF_1.png" width="450" style="border-radius: 5px; border: 1px solid #ccc; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    </a>
  </div>

  <div style="flex: 0 0 450px; text-align: center;">
    <p style="font-weight: bold; color: #2c3e50; margin-bottom: 2px;">2. Alert Distribution</p>
    <p style="font-size: 0.8em; color: #666; margin-bottom: 10px;">(Click to view full size)</p>
    <a href="BF_2.png" target="_blank">
      <img src="BF_2.png" width="450" style="border-radius: 5px; border: 1px solid #ccc; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    </a>
  </div>

  <div style="flex: 0 0 450px; text-align: center;">
    <p style="font-weight: bold; color: #2c3e50; margin-bottom: 2px;">3. Detailed Event Logs</p>
    <p style="font-size: 0.8em; color: #666; margin-bottom: 10px;">(Click to view full size)</p>
    <a href="BF_3.png" target="_blank">
      <img src="BF_3.png" width="450" style="border-radius: 5px; border: 1px solid #ccc; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    </a>
  </div>

  <div style="flex: 0 0 450px; text-align: center;">
    <p style="font-weight: bold; color: #2c3e50; margin-bottom: 2px;">4. Rule 5712 Frequency</p>
    <p style="font-size: 0.8em; color: #666; margin-bottom: 10px;">(Click to view full size)</p>
    <a href="BF_4.png" target="_blank">
      <img src="BF_4.png" width="450" style="border-radius: 5px; border: 1px solid #ccc; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    </a>
  </div>

  <div style="flex: 0 0 450px; text-align: center;">
    <p style="font-weight: bold; color: #2c3e50; margin-bottom: 2px;">5. Rule 5712 Analysis</p>
    <p style="font-size: 0.8em; color: #666; margin-bottom: 10px;">(Click to view full size)</p>
    <a href="BF_5.png" target="_blank">
      <img src="BF_5.png" width="450" style="border-radius: 5px; border: 1px solid #ccc; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    </a>
  </div>

  <div style="flex: 0 0 450px; text-align: center;">
    <p style="font-weight: bold; color: #2c3e50; margin-bottom: 2px;">6. Source/Destination Details</p>
    <p style="font-size: 0.8em; color: #666; margin-bottom: 10px;">(Click to view full size)</p>
    <a href="BF_6.png" target="_blank">
      <img src="BF_6.png" width="450" style="border-radius: 5px; border: 1px solid #ccc; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    </a>
  </div>

  <div style="flex: 0 0 450px; text-align: center;">
    <p style="font-weight: bold; color: #2c3e50; margin-bottom: 2px;">7. Attacker IP Filter</p>
    <p style="font-size: 0.8em; color: #666; margin-bottom: 10px;">(Click to view full size)</p>
    <a href="BF_7.png" target="_blank">
      <img src="BF_7.png" width="450" style="border-radius: 5px; border: 1px solid #ccc; box-shadow: 2px 2px 5px rgba(0,0,0,0.1);">
    </a>
  </div>

</div>
---

## 3. Attack Phase: Lateral Movement (Upcoming)
*Investigation in progress. Screenshots and analysis for Lateral Movement will be added here using the same interactive slider format.*

---

## 4. Remediation & Hardening
1. **Account Deletion:** Executed `sudo userdel -r persistence_user` to remove the backdoor.
2. **SSH Hardening:** Modified `/etc/ssh/sshd_config` to set `PermitRootLogin no`.
3. **Detection Improvement:** Recommended adjusting account lockout thresholds to monitor sustained failures over a 24-hour window.
