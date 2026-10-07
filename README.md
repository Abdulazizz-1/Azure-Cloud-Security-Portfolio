#  Azure Cloud Security & SOC Operations Portfolio

Welcome to my technical portfolio demonstrating hands-on experience in designing, implementing, and monitoring security controls within Microsoft Azure. This project showcases practical implementation of cloud security engineering and SOC analyst workflows, reflecting advanced skills in securing cloud environments and proactively hunting threats.

---

## 1. Identity & Access Management (IAM & PIM)

Securing the perimeter starts with robust identity controls. I implemented strict access policies utilizing Microsoft Entra ID.

*   **Role-Based Access Control (RBAC):** Applied least privilege principles by managing assignments at the Resource Group level.
    ![RBAC Configuration](https://github.com/user-attachments/assets/bee1e988-22c3-4842-91ed-d8d1236b1659)
*   **Privileged Identity Management (PIM):** Configured time-bound role assignments to minimize the attack surface for highly privileged accounts.
    ![PIM Configuration](https://github.com/user-attachments/assets/207e7757-7579-4ddd-9ea4-f0426679e582)
*   **Microsoft Graph API Security:** Explicitly granted Admin Consent for necessary, scoped permissions.
    ![Graph API Admin Consent](https://github.com/user-attachments/assets/c910cafb-78da-4be8-b994-358bc89bed5e)

---

## 2. Storage Security & Incident Response

Protecting data at rest and demonstrating active incident response capabilities during a simulated breach scenario.

*   **Access Control:** Configured Stored Access Policies for Blob Containers to regulate access.
    ![Stored Access Policy](https://github.com/user-attachments/assets/dc2176b0-49ea-4ceb-9dcf-88f3d60673fd)
*   **Breach Simulation & Containment:** Successfully simulated a breach response by dynamically revoking read access, immediately resulting in authentication failures for unauthorized entities.
    ![Access Revoked](https://github.com/user-attachments/assets/c3980b29-f267-489e-856c-1dc89258beee)

---

## 3. Network & Application Security (WAF)

Implementing network segmentation and protecting public-facing applications from common threats.

*   **Network Security Groups (NSG):** Deployed VMs with tightly configured NSGs to restrict inbound/outbound traffic.
    ![NSG Configuration](https://github.com/user-attachments/assets/126db66d-30e3-47ee-8278-e3f0ac8b6e8d)
*   **Secure Remote Access:** Established secure administrative connections utilizing Azure Bastion, eliminating the need for public IPs.
    ![Bastion Connection](https://github.com/user-attachments/assets/902a1abe-0da5-4ecb-a30a-fbb7a534e0fe)
    ![Windows Remote Screen](https://github.com/user-attachments/assets/7c8e886a-e117-47bb-88a4-ec79eb6fbd05)
*   **Web Application Firewall (WAF):** Deployed and managed WAF policies. Tested traffic in **Detection Mode** and subsequently switched to **Prevention Mode** to actively block malicious requests.
    ![WAF Detection Mode](https://github.com/user-attachments/assets/7b1bd49a-e7d9-41a8-a790-600f27a3cb89)
    ![WAF Switch to Prevention](https://github.com/user-attachments/assets/7f41f448-c172-4b76-ac51-3fedc3dfa929)

---

## 4. Secrets Management & API Security

Ensuring sensitive credentials are never hardcoded and APIs are protected from unauthorized access.

*   **Azure Key Vault:** Retrieved secrets programmatically via Python scripts executed through the Serial Console. Handled authorization errors effectively.
    ![Key Vault Access](https://github.com/user-attachments/assets/de299cc2-ebd5-47f0-a65d-84f4102edf96)
    ![Key Vault Error Handling](https://github.com/user-attachments/assets/be401cc5-85c5-4987-9afa-f0f829053996)
*   **API Management (APIM):** Enforced IP filtering policies to restrict API access, verifying successful blocking (403 Forbidden) for unauthorized IPs.
    ![API IP Filter Policy](https://github.com/user-attachments/assets/f9b10957-0bcf-46fb-89ce-2a0af70e51e9)
    ![API Access Denied](https://github.com/user-attachments/assets/c6b8e837-924f-4832-a4d0-068d72e3b615)

---

## 5. Container & Serverless Security

Securing modern deployment models including Containers and Serverless functions.

*   **Azure Kubernetes Service (AKS):** Managed cluster access by explicitly assigning Kubernetes permissions utilizing Microsoft Entra ID.
*   **Container Instances & Logging:** Deployed containerized applications and validated runtime execution and application logs.
    ![Container Instance Logs](https://github.com/user-attachments/assets/2d9a251c-db21-42ee-a19b-7c75d475d668)
*   **Azure Functions:** Deployed secure serverless code environments via Azure Cloud Shell.
    ![Function Deployment](https://github.com/user-attachments/assets/cd7e9262-0ceb-4071-bb8c-37efd0a5c26b)

---

## 6. Monitoring, Logging & SOC Operations (Microsoft Sentinel)

The core of security operations: ensuring complete visibility and automated threat detection.

*   **Log Analytics Workspace:** Configured custom log tables to ingest specific application data.
    ![Custom Log Table](https://github.com/user-attachments/assets/2a440203-3d7e-4d24-a39e-95aaa9c3714e)
*   **Data Connectors (AMA):** Integrated both Windows and Linux security events into Microsoft Sentinel using the Azure Monitor Agent (AMA).
    ![Windows AMA Connector](https://github.com/user-attachments/assets/fbab4857-dcd8-4480-b4d7-64f8faf6ebba)
    ![Linux AMA Connector](https://github.com/user-attachments/assets/c543636b-2ee8-4c26-9128-03f7ca3385c3)
*   **Threat Detection (KQL):** Created and scheduled custom analytics rules in Microsoft Sentinel to proactively hunt for threats.
    ![Sentinel Analytics Rule](https://github.com/user-attachments/assets/09de465c-00fd-45ef-941a-b58d08841f71)
    ![Sentinel Logs Query](https://github.com/user-attachments/assets/69673df3-a4ea-499f-bc0d-5cf9b89a7ff4)
