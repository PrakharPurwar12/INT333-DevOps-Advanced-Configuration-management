# 🔧 INT333 - DevOps Advanced Configuration Management

This repository contains my practical work and hands-on learning for **INT333: DevOps Advanced Configuration**, focused on **Puppet** for configuration management, automation, and infrastructure provisioning on **AWS**.

---

## 📚 Practicals

### 1️⃣ Puppet Master-Agent Setup & Certificate Signing
📄 [Puppet Practical 1](https://github.com/PrakharPurwar12/INT333-DevOps-Advanced-Configuration-management/blob/main/Puppet%20practical%201.pdf)

Sets up the foundational Puppet infrastructure on AWS:
- Provisioning EC2 instances for Puppet **Master** and **Agent**
- Installing Puppet Server and Puppet Agent packages
- Configuring the agent to point to the master
- Generating and submitting the agent's SSL certificate signing request (CSR)
- Signing the certificate on the master (`puppet cert sign`)
- Verifying successful Master–Agent communication

**Tools:** Puppet, AWS


---

### 2️⃣ Creating and Applying Puppet Manifests
📄 [Puppet Practical 2](https://github.com/PrakharPurwar12/INT333-DevOps-Advanced-Configuration-management/blob/main/Puppet%20Practical%202.pdf)

Builds on the Master-Agent setup by writing and applying Puppet manifest (`.pp`) files:
- Writing resource declarations (files, directories, packages, services) directly in manifests
- Applying manifests from the Puppet Master to the Agent node
- Understanding the Puppet catalog compilation and application process
- Verifying resource state changes on the agent node

**Tools:** Puppet, AWS

---

### 3️⃣ Implementation of Puppet Classes for Reusable Configuration Management
📄 [Puppet Practical 3](https://github.com/PrakharPurwar12/INT333-DevOps-Advanced-Configuration-management/blob/main/Puppet%20Practical%203.pdf)

Refactors raw manifest logic into a reusable **Puppet class** to demonstrate scalable configuration management:
- **Problem:** Managing an `myapp` application directory setup directly inside `site.pp` becomes hard to maintain as infrastructure grows
- **Solution:** Encapsulate all related resources into a custom class `myapp`
- Class defines:
  - `/home/Man` directory
  - `/home/Man/myapp` directory (dependent on the parent directory)
  - `/home/Man/myapp/config.txt` file with managed content
- Uses `require` metaparameters to enforce correct resource ordering (directories before file)
- Class is invoked from `site.pp` using `include myapp`
- Verified using `puppet agent --test` on the agent, confirming the catalog applies successfully and the config file content is managed by Puppet

**Tools:** Puppet, AWS

---

## 🛠️ Technologies

| Technology | Purpose |
|---|---|
| ![Puppet](https://img.shields.io/badge/Puppet-FFAE1A?style=flat&logo=puppet&logoColor=black) | Configuration Management & Automation |
| ![Ansible](https://img.shields.io/badge/Ansible-black?style=flat&logo=ansible) | Automation & Configuration Management |
| ![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat&logo=terraform&logoColor=white) | Infrastructure as Code (IaC) |
| ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white) | Cloud Infrastructure |

---

## 📌 Course Information

**Course Code:** INT333  
**Course:** DevOps Advanced Configuration

> 🚧 More practicals, configurations, and implementations will be added as the course progresses.

---

## 👤 Author

**Prakhar Purwar**
