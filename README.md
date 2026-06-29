# Enterprise Systems Administration & Help Desk Ticketing Portfolio Lab

## 📌 Project Overview
This portfolio project demonstrates a production-grade integration of enterprise identity management, systems administration, and technical support infrastructure. The lab simulates a live corporate environment by pairing a **Windows Server 2022 instance hosted on Google Cloud Platform (GCP)** with a cloud-managed **Spiceworks Help Desk tracking system**. 

Throughout this project, I acted as the sole Tier 1/2 IT Support Specialist and Systems Administrator for **Ramsey Tech Labs**, resolving a 12-ticket queue spanning identity lifecycles, automated governance, access control security, and network protocol diagnostics.

---

## 🛠️ Technology Stack & Competencies
* **Directory Services:** Active Directory Domain Services (AD DS)
* **Automation & Governance:** Group Policy Objects (GPO), Group Policy Preferences (GPP)
* **Cloud Infrastructure:** Google Cloud Platform (GCP) Compute Engine
* **Ticketing & ITSM:** Spiceworks Help Desk
* **Security & Storage:** Role-Based Access Control (RBAC), SMB File Sharing, Share/NTFS Permissions
* **OS & Networking Utilities:** PowerShell 7, Command Line (ICMP, DNS, DHCP audits), System File Checker (SFC)

---

## 📊 The Central Dashboard: Spiceworks ITSM Environment
All support interactions were captured, prioritized, and tracked through to successful remediation within Spiceworks.

## Spiceworks Closed Ticket Queue

<img width="1149" height="759" alt="Screenshot 2026-06-29 at 11 14 23 AM" src="https://github.com/user-attachments/assets/1e55a4c1-1aa7-47b5-92d0-fd790ab6c44a" />
*Figure 1: Complete audit history of the 13 resolved support lines.*

---

## 📂 Detailed Ticket Breakdown & Implementations

### 👤 1. Identity & Access Management (IAM)

#### Ticket 10: Staff Name Change (Linda Martinez)
* **Incident:** User requested a directory name adjustment to comply with newly modified internal payroll data formatting.
* **Resolution:** Modified the account object string variables directly inside the active directory directory tree. Aligned display traits and adjusted the primary User Logon Name prefix to `lmartinez` to adhere to corporate conventions.
* **Evidence:**

  <img width="868" height="533" alt="Screenshot 2026-06-25 at 7 37 27 PM" src="https://github.com/user-attachments/assets/6670e293-fdaf-45de-9e37-8d454238fdbd" />


#### Ticket 12: Temporary Staff Onboarding & Account Expiration Lifecycle
* **Incident:** HR submitted an incoming request to provision a temporary profile (`Sub Teacher`) for a short-term contractor requiring environment access.
* **Resolution:** 
  1. Provisioned a constrained user object container (`steacher@school.local`) within the target `Staff` Organizational Unit (OU). Enforced a mandatory password reset phase upon initial environment entry.
  2. Applied an explicit identity termination flag directly inside the object's properties window, scheduling an immutable expiration constraint for Friday, August 21, 2026, to neutralize dormant account threats.
* **Evidence:**

<img width="844" height="534" alt="Screenshot 2026-06-25 at 7 38 40 PM" src="https://github.com/user-attachments/assets/de513dcb-514e-4c42-b673-93dfd0d8b5e1" />

<img width="755" height="536" alt="Screenshot 2026-06-25 at 7 47 46 PM" src="https://github.com/user-attachments/assets/e4e4e8d1-2f3b-471b-9411-42a8512b6cad" />

---

### 🛠️ 2. Endpoint Configuration & Group Policy Automation

#### Ticket 6: Centralized Desktop Standardization via GPO
* **Incident:** Management requested a uniform desktop workspace environment applied across all connected endpoints within the domain scope.
* **Resolution:** Created and deployed an Active Directory Group Policy Object named `Mandatory School Wallpaper`. Managed the policy layout to force a path to a locked local asset resource and linked the policy definition directly to the `School-Root` domain node to enforce absolute downward inheritance compliance.
* **Evidence:**

<img width="791" height="637" alt="Screenshot 2026-06-25 at 7 45 00 PM" src="https://github.com/user-attachments/assets/828c1cf7-e849-4276-a9e5-ac67020cdbc8" />

<img width="750" height="527" alt="Screenshot 2026-06-25 at 7 46 19 PM" src="https://github.com/user-attachments/assets/0dc2ed89-8f49-4bdc-ae7e-50b5ef96b154" />

#### Ticket 13: Automated Drive Mapping via Group Policy Preferences (GPP)
* **Incident:** Library staff requested persistent, automated client-side access to shared organizational document collections without needing manual file path entries.
* **Resolution:** Leveraged Group Policy Preferences (GPP) inside the management console to configure a server-side drive mapping deployment action. Instructed endpoints to automatically map the corporate resource path `\\school-dc-2022\Library-S...` to local client drive letter `L:`.
* **Evidence:**

<img width="1287" height="566" alt="Screenshot 2026-06-25 at 7 57 12 PM" src="https://github.com/user-attachments/assets/591e2359-65e6-4f5b-8eef-3728dc244768" />

---

### 🖨️ 3. Hardware Triage & System Maintenance

#### Ticket 7: Library Print Spooler Remediation
* **Incident:** Users reported that print jobs sent to the library hardware terminal were hanging indefinitely and failing to execute.
* **Resolution:** Isolated the breakdown to a local driver stall event within the printer control subsystem. Cleared the backlogged payload arrays and manually cycled the queue state away from a `Paused` state, returning the subsystem to a nominal, responsive state.
* **Evidence:**

<img width="1123" height="595" alt="Screenshot 2026-06-25 at 8 15 50 PM" src="https://github.com/user-attachments/assets/9bd94f58-c53c-498b-9b87-e4e641a8a8ae" />
#### Ticket 15: Local System Integrity Diagnostics
* **Incident:** End-user reported erratic device performance and software crashes during daily desktop operations.
* **Resolution:** Remotely executed the Windows System File Checker (`sfc /scannow`) utility through PowerShell 7 to audit core binary structures against baseline image maps. Verified that the operating system root storage tree was clear of corrupted code blocks.
* **Evidence:**

<img width="977" height="515" alt="Screenshot 2026-06-28 at 12 44 42 PM" src="https://github.com/user-attachments/assets/63e942e7-8425-4d75-a8a9-41d21c55278d" />
---

### 🔒 4. Secure Network Storage & Role-Based Access Control (RBAC)

#### Ticket 11: Shared Folder Problems & Departmental Containment
* **Incident:** HR required a secure, isolated network storage share path restricted strictly to authenticated personnel handling sensitive employee files.
* **Resolution:** 
  1. Provisioned a server-side SMB share container endpoint named `HR-Private` directly on the local domain controller volume path (`C:\HR-Private`).
  2. Maintained tight data control boundaries by auditing user object security attributes. Verified that personnel access rights (such as user Tamron Williams) were strictly derived through explicit security group inheritance nested inside the `HR Staff` directory container.
* **Evidence:**

<img width="1213" height="656" alt="Screenshot 2026-06-28 at 12 55 12 PM" src="https://github.com/user-attachments/assets/57ca848e-33c1-47ca-a8a4-c60013e0eb10" />

<img width="852" height="539" alt="Screenshot 2026-06-28 at 1 00 24 PM" src="https://github.com/user-attachments/assets/8ee357f2-4cfb-4c93-a6cc-3b5566d896ef" />

---

### 🌐 5. Advanced Network Protocol Triage

#### Ticket 14: Computer Lab Local Network and Gateway Outage
* **Incident:** Endpoint stations across the computing lab space reported a total loss of external web platform connectivity.
* **Resolution:** Deployed a structured, 3-tier OSI network model triage sequence using PowerShell 7:
  1. **Layer 1-3 Verification:** Executed `ipconfig /all` to query local physical interface traits. Verified accurate DHCP lease conditions, proper local IP structural bounds (`10.128.0.5`), and correct gateway pointers (`10.128.0.1`).
  2. **WAN Routing Verification:** Issued an ICMP echo payload tracking command (`ping 8.8.8.8`) out past internal gateway switches to confirm zero routing loss metrics over external transit nodes.
  3. **Layer 7 Translation Verification:** Ran an application translation probe (`nslookup google.com`) to evaluate structural health across forward lookup tables. Confirmed the local loop targets were successfully translating target strings into usable public IP maps.
* **Evidence:**
  ![Local Network Adapter Diagnostic Check](images/Screenshot%202026-06-28%20at%201.02.09%20PM.jpg)
  ![ICMP Gateway Echo Routing Verification Passes](images/Screenshot%202026-06-28%20at%201.02.44%20PM.jpg)
  ![DNS Name Resolution Testing Via Nslookup](images/Screenshot%202026-06-28%20at%201.03.11%20PM.jpg)

---

## 🎯 Key Takeaways & Operational Competency
Building this lab environment from the ground up provided actionable experience in managing enterprise infrastructure:
* Designing, organizing, and maintaining clean Active Directory **Organizational Units (OUs)** and managing security group memberships.
* Scaling configuration management via **Group Policy Objects** to systematically eliminate manual endpoint adjustments.
* Standardizing data security policies using proper share level and NTFS permission layers following **least privilege principles**.
* Developing a structured, logical methodology for **diagnosing and troubleshooting network and operating system issues** under tight service-level deadlines.
