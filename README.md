# SOC Incident Report: Brute Force Attack Detection
**Analyst:** [Arivazhagan] | **Target System:** Windows/Linux Lab | **Status:** RESOLVED

---

## Attack Analysis: SSH Brute Force (Rule 5712)
**Summary:** This phase documents the detection of 69 failed authentication events. The attacker (IP: `10.48.156.247`) utilized a "low-and-slow" cadence, attempting access every 8–10 minutes to bypass automated lockout thresholds.

<div style="display: flex; overflow-x: auto; gap: 20px; padding-bottom: 20px; border: 1px solid #ddd; padding: 15px; border-radius: 8px;">

  <div style="flex: 0 0 400px;">
    <p style="font-weight: bold; color: #2c3e50;">1. Dashboard Overview</p>
    <p style="font-size: 0.9em;">Total alerts over 24 hours showing initial spikes.</p>
    <img src="BF_1.png" width="400" style="border-radius: 4px;">
  </div>

  <div style="flex: 0 0 400px;">
    <p style="font-weight: bold; color: #2c3e50;">2. Alert Distribution</p>
    <p style="font-size: 0.9em;">Pie chart showing the volume of SSHD alerts vs others.</p>
    <img src="BF_2.png" width="400" style="border-radius: 4px;">
  </div>

  <div style="flex: 0 0 400px;">
    <p style="font-weight: bold; color: #2c3e50;">3. Event Detail List</p>
    <p style="font-size: 0.9em;">Timestamped list of failed login attempts.</p>
    <img src="BF_3.png" width="400" style="border-radius: 4px;">
  </div>

  <div style="flex: 0 0 400px;">
    <p style="font-weight: bold; color: #2c3e50;">4. Rule 5712 Statistics</p>
    <p style="font-size: 0.9em;">Detailed breakdown of Rule 5712 occurrences.</p>
    <img src="BF_4.png" width="400" style="border-radius: 4px;">
  </div>

  <div style="flex: 0 0 400px;">
    <p style="font-weight: bold; color: #2c3e50;">5. Rule 5712 Pie Chart</p>
    <p style="font-size: 0.9em;">Visualizing Rule 5712 as a specific threat vector.</p>
    <img src="BF_5.png" width="400" style="border-radius: 4px;">
  </div>

  <div style="flex: 0 0 400px;">
    <p style="font-weight: bold; color: #2c3e50;">6. Src/Dest IP Analysis</p>
    <p style="font-size: 0.9em;">Verification of Attacker IP and Target destination.</p>
    <img src="BF_6.png" width="400" style="border-radius: 4px;">
  </div>

  <div style="flex: 0 0 400px;">
    <p style="font-weight: bold; color: #2c3e50;">7. Attacker IP Filter</p>
    <p style="font-size: 0.9em;">Isolated view of all activity from 10.48.156.247.</p>
    <img src="BF_7.png" width="400" style="border-radius: 4px;">
  </div>

</div>

---

## Remediation & Analyst Notes
- **Action:** Blocked Source IP `10.48.156.247` at the firewall level.
- **Hardening:** Updated SSH config to `PermitRootLogin no`.
