# 🛡️ Azure Cloud Security & SOC Operations Portfolio

Welcome to my technical portfolio demonstrating hands-on experience in designing, implementing, and monitoring security controls within Microsoft Azure. This project showcases practical implementation of cloud security engineering and SOC analyst workflows, reflecting advanced skills in securing cloud environments and proactively hunting threats.

---

## 🔐 1. Identity & Access Management (IAM & PIM)

Securing the perimeter starts with robust identity controls. I implemented strict access policies utilizing Microsoft Entra ID.

*   **Role-Based Access Control (RBAC):** Applied least privilege principles by managing assignments at the Resource Group level.
    ![RBAC Configuration](Screenshot%201448-04-05%20at%208.16.33%E2%80%AFAM.jpg)
*   **Privileged Identity Management (PIM):** Configured time-bound role assignments to minimize the attack surface for highly privileged accounts.
    ![PIM Configuration](Screenshot%201448-04-05%20at%208.19.22%E2%80%AFAM.png)
*   **Microsoft Graph API Security:** Explicitly granted Admin Consent for necessary, scoped permissions.
    ![Graph API Admin Consent](Screenshot%201448-04-07%20at%207.12.47%E2%80%AFAM.png)

---

## 🗄️ 2. Storage Security & Incident Response

Protecting data at rest and demonstrating active incident response capabilities during a simulated breach scenario.

*   **Access Control:** Configured Stored Access Policies for Blob Containers to regulate access.
    ![Stored Access Policy](policy%20changes%20incase%20of%20breach%20(%20get%20rid%20if%20read%20and%20list%20and%20then%20refresh%20it%20back%20to%20normal)%20..jpg)
*   **Breach Simulation & Containment:** Successfully simulated a breach response by dynamically revoking read access, immediately resulting in authentication failures for unauthorized entities.
    ![Access Revoked](policy%20changes%20incase%20of%20breach%20(%20get%20rid%20if%20read%20and%20list%20and%20then%20refresh%20it%20back%20to%20normal)%20...jpg)

---

## 🌐 3. Network & Application Security (WAF)

Implementing network segmentation and protecting public-facing applications from common threats.

*   **Network Security Groups (NSG):** Deployed VMs with tightly configured NSGs to restrict inbound/outbound traffic.
    ![NSG Configuration](privite%20servoce.jpg)
*   **Secure Remote Access:** Established secure administrative connections utilizing Azure Bastion, eliminating the need for public IPs.
    ![Bastion Connection](bass%20succcc.png)
*   **Web Application Firewall (WAF):** Deployed and managed WAF policies. Tested traffic in **Detection Mode** and subsequently switched to **Prevention Mode** to actively block malicious requests.
    ![WAF Detection Mode](detection%20mode.png)
    ![WAF Switch to Prevention](switch%20to%20pre.jpg)

---

## 🔑 4. Secrets Management & API Security

Ensuring sensitive credentials are never hardcoded and APIs are protected from unauthorized access.

*   **Azure Key Vault:** Retrieved secrets programmatically via Python scripts executed through the Serial Console. Handled authorization errors effectively.
    ![Key Vault Access](Screenshot%201448-04-06%20at%206.21.19%E2%80%AFAM.jpg)
    ![Key Vault Error Handling](Screenshot%201448-04-06%20at%205.19.03%E2%80%AFAM.jpg)
*   **API Management (APIM):** Enforced IP filtering policies to restrict API access, verifying successful blocking (403 Forbidden) for unauthorized IPs.
    ![API IP Filter Policy](api%20policies.png)
    ![API Access Denied](api%20denied.jpg)

---

## 🐳 5. Container & Serverless Security

Securing modern deployment models including Containers and Serverless functions.

*   **Azure Kubernetes Service (AKS):** Managed cluster access by explicitly assigning Kubernetes permissions utilizing Microsoft Entra ID.
*   **Container Registry:** Pushed and deployed images securely via Azure Container Registry (ACR) to Azure Container Instances.
*   **Azure Functions:** Deployed secure serverless code environments via Azure Cloud Shell.
    ![Function Deployment](function.zip%20display.jpg)

---

## 👁️ 6. Monitoring, Logging & SOC Operations (Microsoft Sentinel)

The core of security operations: ensuring complete visibility and automated threat detection.

*   **Log Analytics Workspace:** Configured custom log tables to ingest specific application data.
    ![Custom Log Table](Custome%20table%20.png)
*   **Data Connectors (AMA):** Integrated both Windows and Linux security events into Microsoft Sentinel using the Azure Monitor Agent (AMA).
    ![Windows AMA Connector](rl-windows%20event%20via%20ama%20.jpg)
    ![Linux AMA Connector](rl-linux.jpg)
*   **Threat Detection (KQL):** Created and scheduled custom analytics rules in Microsoft Sentinel to proactively hunt for threats.
    ![Sentinel Analytics Rule](shceduled%20quere%20rule%20created.png)
    ![Sentinel Logs Query](windows%20logs%20events.jpg)
