# Awesome-Secure-File-Transfer-Distribution

# Awesome Secure File Transfer & Distribution

> A curated list of top Secure File Transfer and Distribution platforms — both SaaS/Hosted commercial solutions and open-source alternatives for exchanging large or sensitive files with encryption, audit trails, and compliance controls.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Axway SecureTransport](#axway-securetransport)
  - [Progress MOVEit](#progress-moveit)
  - [Kiteworks](#kiteworks)
  - [Titan MFT Server](#titan-mft-server)
  - [SendSafely](#sendsafely)
  - [Citrix ShareFile](#citrix-sharefile)
  - [WeTransfer Pro](#wetransfer-pro)
- [Open-Source Software](#-open-source-software)
  - [FileSender](#filesender)
  - [FiNo](#fino)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Secure File Transfer and Distribution platforms. These are not open-source but are included as reference points for feature comparison.

### Axway SecureTransport
**Type:** Enterprise MFT gateway with high availability  
Axway SecureTransport is built for some of the largest, most critical MFT deployments globally, offering enterprise clustering, zero-downtime upgrades, and guaranteed delivery with SLAs up to 99.99% [citation:7]. It provides end-to-end encryption, full audit trails, and real-time alerting for compliance with GDPR, HIPAA, SOX, and PCI DSS [citation:1][citation:7]. The platform supports on-premises, cloud, hybrid, and managed service deployments, with REST APIs for integration and an MCP server for AI assistant access to operational context [citation:7].  
**Best for:** Large enterprises and government agencies needing maximum scalability, resilience, and audit governance for high-volume file exchanges.

### Progress MOVEit
**Type:** Managed file transfer with cloud and on-premises options  
Progress MOVEit (2026.0) is used by 3,000+ organizations and 100,000+ users for secure file transfers [citation:8]. It offers cloud-based MFTaaS, on-premises Transfer server, and Automation modules with no/low-code workflow builders. Compliance support covers PCI-DSS, HIPAA, GDPR, SOC 2, and CCPA/CPRA, with tamper-evident audit trails and data governance enforcement [citation:8]. Listed as a Leader in the G2 Grid Report for Managed File Transfer [citation:8].  
**Best for:** Organizations wanting a mature, widely adopted MFT solution with flexible deployment and strong compliance coverage.

### Kiteworks
**Type:** Secure MFT with hardened appliance and granular controls  
Kiteworks provides vault-to-vault transfers, a library of 2,000 connectors, and visual workflow authoring without coding [citation:9]. Security is enforced through a hardened virtual appliance with firewalls around each server, intrusion detection, and one-button patching. It integrates with DLP, ATP, and CDR systems, supports NIST 800-53, PCI DSS, and ISO 27001/27017/27018, and provides a standardized audit log of all transactions for SIEM ingestion [citation:9].  
**Best for:** Security-conscious organizations needing hardened infrastructure, granular policy controls, and integration with existing DLP/ATP security stacks.

### Titan MFT Server
**Type:** Cost-effective cloud MFT server  
Titan MFT Server is a fully configured, cloud-optimized server running on a dedicated VM in Azure, AWS, or GCP, priced at approximately $65.70/month or $788.40/year for the software alone [citation:10]. It supports SFTP, FTP/S, WebDAV/S, and HTTP/S, with a web-based admin console, REST API, and 100+ automation event actions. Pre-configured and ready to use, with pay-as-you-go licensing [citation:10].  
**Best for:** Budget-conscious teams wanting a turnkey cloud MFT server with predictable per-VM pricing and no complex setup.

### SendSafely
**Type:** End-to-end encrypted file exchange with developer APIs  
SendSafely uses a split-key architecture where files are encrypted client-side before upload, meaning SendSafely never has access to file contents [citation:6]. It integrates natively with Zendesk, Salesforce, Intercom, Freshdesk, Gmail, and Jira for encrypted file collection within existing workflows. Compliance covers SOC 2 Type II, HIPAA, PCI DSS, and GDPR. Provides REST API, SDKs for Node.js, Python, Java, and .NET, plus an MCP server for AI agent access to encryption primitives [citation:6][citation:15].  
**Best for:** Teams needing end-to-end encrypted file exchange embedded directly into helpdesk, CRM, or email workflows, with strong developer tooling.

### Citrix ShareFile
**Type:** Enterprise file sync and share with encryption  
Citrix ShareFile provides secure file sharing with encryption in transit (SSL/TLS) and at rest (AES 256-bit), customer-managed storage zones (AWS S3, Azure Blob, GCP, on-premises), and access control policies [citation:13]. It integrates with Microsoft apps, offers web/mobile access, and includes reporting, auditing, and retention policies. Reviewers praise encryption quality and ease of encrypted email, though some note larger files take longer and there is a learning curve [citation:4].  
**Best for:** Enterprises wanting a well-integrated file sharing platform with customer-managed storage options and strong Microsoft ecosystem support.

### WeTransfer Pro
**Type:** Simple large-file transfer with password protection  
WeTransfer Pro adds password protection to transfers, with files encrypted in transit (TLS) and at rest (AES-256) on EU-based AWS servers [citation:14]. Password is never included in notification emails, and restricted access can limit downloads to specific email addresses. ISO 27001 certified and GDPR-compliant, with Data Processing Agreements available for business plans. Recipients do not need accounts to download [citation:5][citation:14].  
**Best for:** Creative professionals and teams needing simple, reliable large-file transfers with optional password protection and EU data residency.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Secure File Transfer tools. The open-source ecosystem is **limited**—FileSender is the only mature, production-grade option, with FiNo serving as an experimental proof-of-concept.

### FileSender
**Stack:** PHP / PostgreSQL / Docker | **License:** Open Source (GÉANT)  
FileSender is a mature open-source file transfer application developed by GÉANT for the research and education community, with **version 3.0 released in January 2026** after extensive alpha, beta, and release candidate testing [citation:2]. It can be hosted on-premises, in a private cloud, or on a public cloud of choice, giving organizations full control over policies and legal compliance [citation:2]. Version 3.0 features a completely redesigned, modern UI with streamlined transfer flows, improved responsiveness, and accessibility. It is deployed by NRENs including AARNet (Australia), REANNZ (New Zealand), RNU (Uganda), RNP (Brazil), VPC (Latvia), and regionally by EOSC EU Node and RedCLARA [citation:2].  
**Best for:** Research institutions, universities, and organizations wanting a proven, self-hosted large-file transfer solution with full data sovereignty and a modern UI.

### FiNo
**Stack:** Python / Nostr / IPFS | **License:** Proof-of-Concept  
FiNo (File + Nostr) is an experimental CLI tool demonstrating **decentralized file sharing** using the Nostr protocol for messaging and IPFS for storage [citation:12]. Files are encrypted with AES-256-CBC using a random key, and IPFS CIDs are encrypted within Nostr DMs, so only sender and recipient can decrypt. It provides end-to-end encryption with no central servers and no metadata tracking. **Critical caveat:** The project explicitly states it is a proof-of-concept for research and education, **not intended for production use** without significant security audits [citation:12].  
**Best for:** Developers and researchers exploring decentralized file transfer concepts, not for production or sensitive data workflows.

---

## 📊 Comparison at a Glance

| Software | License | Stack | E2E Encryption | Audit Trail | Self-Hosted | Best For |
|----------|---------|-------|----------------|-------------|-------------|----------|
| **Axway SecureTransport** | Proprietary | On-prem/Cloud | (Transfer encryption) | ✅ Full | (On-prem) | Enterprise MFT at scale |
| **Progress MOVEit** | Proprietary | Cloud/On-prem | (Transfer encryption) | ✅ Tamper-evident | (On-prem) | Mature MFT + compliance |
| **Kiteworks** | Proprietary | On-prem/Cloud | (Vault-to-vault) | ✅ Standardized log | (Appliance) | Hardened MFT + DLP integration |
| **Titan MFT** | Proprietary | Cloud VM | (Transfer encryption) | (Logging) | (Cloud VM) | Cost-effective cloud MFT |
| **SendSafely** | Proprietary | Cloud | ✅ Split-key | ✅ Full | ❌ | E2E encrypted workflow integration |
| **Citrix ShareFile** | Proprietary | Cloud/On-prem | (AES 256) | ✅ Reporting | (On-prem zones) | Enterprise file sharing |
| **WeTransfer Pro** | Proprietary | Cloud | (TLS/AES-256) | (Limited) | ❌ | Simple password-protected transfers |
| **FileSender** | Open Source | PHP/Postgres | (Transfer encryption) | (Logging) | ✅ | Research/education file transfer |
| **FiNo** | PoC | Python/Nostr/IPFS | ✅ Custom ECDH | ❌ | ✅ (Decentralized) | Experimental only |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Secure File Transfer or Distribution tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for **enterprise-grade secure file transfer** is very limited. **FileSender** is the only mature, production-ready option, backed by GÉANT and deployed by national research networks globally [citation:2]. Commercial MFT platforms (Axway, MOVEit, Kiteworks, Titan) provide enterprise clustering, tamper-evident audit trails, DLP integration, and SLA guarantees that open-source tools do not replicate [citation:7][citation:8][citation:9]. For teams needing end-to-end encryption within existing workflows, **SendSafely** offers a split-key architecture with native helpdesk/CRM integrations [citation:6]. **FiNo** demonstrates decentralized file transfer concepts but is explicitly a proof-of-concept, not a production tool [citation:12].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
