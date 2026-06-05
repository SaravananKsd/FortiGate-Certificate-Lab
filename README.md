# FortiGate-Certificate-Lab
Lab setup and certificate installation workflow for FortiGate firewall
# 🔐 FortiGate Certificate Lab Setup

## 📘 Overview
This repository documents my learning journey on **certificate installation and HTTPS error resolution** in FortiGate Firewall.  
It covers the complete flow from generating keys and CSRs to importing certificates and achieving a secure HTTPS connection.

---

## 🧩 Certificate Workflow
1. **Private Key** → Generated locally for secure identity.  
2. **CSR (Certificate Signing Request)** → Created using the private key and submitted to CA.  
3. **Root CA Certificate** → Imported into PC’s *Trusted Root Certification Authorities* store.  
4. **Intermediate Certificate** → Bridges trust between root and domain certificate.  
5. **Domain Certificate** → Installed on FortiGate for HTTPS/SSL‑VPN services.

---

## 🛡️ FortiGate Configuration Steps
- Imported **Domain Certificate** and **CA Chain** into FortiGate.  
- Bound the certificate to **HTTPS admin GUI** and **SSL‑VPN portal**.  
- Verified the certificate chain under *System → Certificates*.  
- Resolved browser warning (**NET::ERR_CERT_AUTHORITY_INVALID**) by trusting the **Root CA**.

---

## ⚠️ Common Issue
> Accessing FortiGate via **IP address** still shows HTTPS warnings.  
> Certificates validate **domain names**, not raw IPs.  
> Add IP to the **Subject Alternative Name (SAN)** or access via domain for full trust.

---

## 📊 Visuals
### Certificate Trust Chain
![Certificate Trust Chain](assets/trust_chain.png)

### FortiGate Certificate Success Thumbnail
![FortiGate Certificate Success](assets/thumbnail.png)

---

## 🧠 Key Takeaways
- Certificates establish **identity and trust** in secure communication.  
- The **Root CA** is the ultimate trust anchor.  
- Domain‑based access works seamlessly once the root CA is trusted.

---

## 🏷️ Tags & Topics
`fortigate` `certificate` `ssl` `tls` `network-security` `lab-practice`

---

## 📢 Author
**Saravanan** — Network Engineer | Lab Enthusiast | Knowledge Sharer  
Connect on [LinkedIn](www.linkedin.com/in/saravanan-a-b48754130) for more technical insights.

---

## 🔖 Hashtags
#FortiGate #FirewallSecurity #DigitalCertificates #SSL #TLS #CyberSecurity #NetworkSecurity #TechLearning #KnowledgeSharing
