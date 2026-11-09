# ☁️ Enterprise Cloud Architect & DevOps Lead

### **Designing & Orchestrating Next-Generation Cloud Foundations**

An expert Cloud Architect specializing in massive scale migrations, automated Governance, and immutable Infrastructure as Code (IaC). Proven track record of architecting **Enterprise Landing Zones and migrating 100+ multi-tier workloads** across multi-subscription hybrid cloud ecosystems.

---

## 🎨 System Architecture Overview

```
┌─────────────────────────────────────────────────────────┐
│                 Microsoft Entra ID Tenant               │
└────────────────────────────┬────────────────────────────┘
                             │
                             ▼
┌─────────────────────────────────────────────────────────┐
│                    Tenant Root Group                    │
└────────────────────────────┬────────────────────────────┘
                             │
         ┌───────────────────┼───────────────────┐
         ▼                   ▼                   ▼
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│   Platform MG   │ │  Application MG │ │   Sandbox MG    │
└────────┬────────┘ └────────┬────────┘ └─────────────────┘
         │                   │
         ├─► Identity Sub    ├─► Dev/UAT Subs
         ├─► Management Sub  └─► Prod Subs
         └─► Connectivity (Hub) Sub
```

---

## 🛠️ Deep-Dive Technical Framework

### 🏢 Enterprise Governance & Identity Hierarchy
* **Tenant & Management Group Design:** Structured Management Group hierarchies (`Platform`, `Application`, `Sandbox`, `Decommissioned`) to minimize blast radius and isolate business units.
* **Identity & Lifecycle Management:** Built on Microsoft Entra ID with rigid User/Group lifecycle patterns, strict Role-Based Access Control (RBAC), and automated subscription onboarding/offboarding workflows.
* **Continuous Compliance:** Enforcement of global security baselines via custom Azure Policies and Enterprise Initiatives coupled with automated compliance monitoring via Microsoft Defender for Cloud.

### 🌐 Secure Hub & Spoke Networking Model
* **IPAM & CIDR Strategy:** Full assessment of On-premises CIDR ranges to ensure overlapping network conflicts are mathematically eliminated before peering.
* **Centralized Connectivity:** High-availability Hub Virtual Networks (VNets) hosting shared VPN Gateways and ExpressRoute circuits to securely bridge cloud workloads.
* **Secured Egress & Private Channels:** Zero-trust architecture design featuring User Defined Routes (UDRs), centralized firewall edge rule tables, Private Endpoints, and strictly isolated Private DNS Zones.

### 📜 Infrastructure as Code (IaC) Landing Zones
* **Production-Grade Terraform:** Modular, highly reusable layout structures leveraging encrypted remote state files, state locking, and strict least-privilege identity access management.
* **Continuous Verification (CI/CD):** Native Azure DevSecOps pipeline workflows built to execute static code analysis (`tflint`), automated secret scanning, resource budgeting checks (`infracost`), manual validation steps, and programmatic continuous Drift Detection.

### 🚀 Enterprise DevSecOps Pipelines
* **Trunk-Based Branching:** Highly restrictive branching policies requiring mandatory peer code reviews, Code Owners consensus, and hard blocks preventing direct deletion of main branches.
* **Resilient Pipeline Templates:** Reusable, parameterized YAML configuration blocks split into deterministic stage steps:
  `Validate & Test` ➡️ `Artifact Build` ➡️ `Dry Run / Plan` ➡️ `Manual Approval` ➡️ `Blue-Green Deployment` ➡️ `Auto-Rollback`
* **Automated Configuration:** Immutable compute environment provisioning utilizing modular custom data scripts to bake platform and middleware configurations seamlessly on node boot.

### 🔄 Large-Scale Cloud Migrations
* **CAF Framework Alignment:** Migration processes structurally mapped across the **Microsoft Cloud Adoption Framework (CAF)** lifecycles:
  `Strategy` ➡️ `Plan` ➡️ `Ready` ➡️ `Adopt` ➡️ `Govern` ➡️ `Secure` ➡️ `Manage`
* **Execution & Checklists:** Rigorous, programmatic execution paths backed by end-to-end asset discovery assessments, detailed validation checklists (Pre/During/Post Cutover), and Hypercare observation structures.

### 💰 FinOps & Infrastructure Optimization
* **Wastage Mitigation:** Programmatic tracking to automatically detect and decommission idle resources, unattached managed disks, oversized compute instances, and redundant log analytics ingestions.
* **Cost Governance Runbooks:** Automated scheduling rules to shut down non-production workloads during off-peak hours paired with strategic Reserved Capacity optimizations.

### 🛡️ Resilience, HA, & Observability
* **Business Continuity (BCDR):** Mission-critical services configured across Zone-Redundant (ZRS) and Geo-Redundant (GRS) patterns engineered to hit aggressive RTO and RPO metrics.
* **Observability Matrix:** Universal telemetry collection linking distributed application metrics into centralized log query analytics workspaces.

---

## 🎯 Architecture Quality Matrix

| Architectural Pillar | Implementation Mechanism | Business Outcome |
| :--- | :--- | :--- |
| **Scalable** | Management Group hierarchies & Scale Sets (VMSS) | Frictionless horizontal enterprise growth |
| **Secure** | Zero-Trust network layer, RBAC, & Defender | High-barrier threat mitigation footprint |
| **Robust & Reliable** | Active-Active gateways & Multi-Region failovers | Uninterrupted mission-critical operational runtime |
| **Portable** | Modular Terraform layout configurations | Cloud-native agility with zero configuration lock-in |
| **Governed** | Immutable Azure Policy and Enterprise Initiatives | Automated organizational continuous compliance |
| **Cost Optimised** | Right-sizing algorithms & Scheduled runbooks | Eliminated waste & maximized cloud ROI investments |

---

<p align="center">
  <sub>Built with 💻 and ☁️ • Enterprise Architecture Portfolio</sub>
</p>
