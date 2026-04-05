# Validating-GRC-Policies-with-Technical-Simulations

### **Objective**
To bridge the gap between high-level policy and technical enforcement by simulating real-world threats. This project demonstrates that Governance, Risk, and Compliance (GRC) isn't just a paperwork exercise, but a measurable state of security validated through continuous testing.

### **Core Goal**
To technically validate **NIST 800-53 Control AC-7 (Unsuccessful Logon Attempts)** by executing a brute-force attack simulation and verifying that detection controls, telemetry, and incident response workflows trigger as intended.



### **Skills Learned**
* **Offensive Scripting:** Developing PowerShell-based attack vectors for credential testing.
* **EDR Management:** Analyzing telemetry and alerts within **Microsoft Defender for Endpoint**.
* **Process Analysis:** Identifying process hollowing and suspicious behavior in `notepad.exe`.
* **Mapping Compliance:** Linking technical event IDs and alerts to specific GRC frameworks (NIST/ISO).
* **Incident Triage:** Utilizing Incident Graphs to map relationships between users, hosts, and malicious processes.



### **Steps**
1.  **Attack Execution (Offensive Phase):**
    Ran a custom PowerShell script (`AttackScript.ps1`) designed to simulate a brute-force credential attack. To bypass basic signature detection, the script utilized process hollowing techniques, masking its activity under a legitimate `notepad.exe` process.

3.  **Monitoring & Detection (Defensive Phase):**
    Observed the environment through the Microsoft Defender for Endpoint dashboard to see if the activity was captured in the telemetry stream.

5.  **Analysis & Validation:**
    Triaged the resulting alert: **"Unexpected behavior observed by a process"** (Medium Severity). 
6.  **Evidence Mapping:**
    Used the **Incident Graph** to visualize the attack path, confirming the connection between the target user account, the host machine, and the manipulated process.

 
### **Security Takeaway**
**Policies are hypotheses; simulations are the proof.** A policy like AC-7 is only effective if the underlying technology (EDR/SIEM) is tuned to see the violation. By conducting this simulation, we move from "assuming" compliance to "proving" operational resilience. This ensures that when an actual audit or incident occurs, the Incident Response Plan (IRP) is a functional reality rather than a theoretical document.

### Screenhorts showing the process

 ![Azure_Brute Force_PowerShell](https://github.com/user-attachments/assets/dcc5612e-4c68-403e-b448-a5db408b10a9)

 ![Azure_Brute Force_PowerShell_2](https://github.com/user-attachments/assets/9c61a7a7-d46a-4fcf-b697-b0588b86a34c)
