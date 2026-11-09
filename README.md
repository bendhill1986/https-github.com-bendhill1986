# ☁️ Enterprise Cloud Architect & DevOps Lead

### **Designing & Orchestrating Next-Generation Cloud Foundations**
An expert Cloud Architect specializing in massive scale migrations, automated Governance, and immutable Infrastructure as Code (IaC). Proven track record of architecting **Enterprise Landing Zones and migrating 100+ multi-tier workloads** across multi-subscription hybrid cloud ecosystems.

---

## 🏗️ Core Architecture & Migration Blueprint

This repository serves as a master blueprint for an enterprise-grade, multi-region architecture designed for the migration and governance of **100+ applications** across Development, UAT, and Production environments.

```
┌─────────────────────────────────────────────────────────┐
│                 Microsoft Entra ID Tenant               │
└────────────────────────────┬────────────────────────────┘
▼
┌─────────────────────────────────┐
│        Tenant Root Group        │
└────────────────┬────────────────┘
│
┌─────────────────────────────────────┼─────────────────────────────────────┐
▼                                     ▼                                     ▼
┌──────────────────┐                  ┌──────────────────┐                  ┌──────────────────┐
│   Platform MG    │                  │  Application MG  │                  │    Sandbox MG    │
└────────┬─────────┘                  └────────┬─────────┘                  └──────────────────┘
│                                     │
├─► Identity Sub                      ├─► Dev/UAT Subs
├─► Management Sub                    └─► Prod Subs
└─► Connectivity (Hub) Sub
```

---

## ⚡ Technical Framework & Capabilities

### 🏢 Enterprise Governance & Identity Hierarchy
* **Tenant & Management Group Design:** Multi-layered Management Group hierarchies segmented by function (`Platform`, `Application`, `Sandbox`, `Decommissioned`) enforce a clean blast radius.
* **Identity & Lifecycle Management:** Built using Microsoft Entra ID with deterministic User/Group structures, robust Role-Based Access Control (RBAC), subscription automated onboarding/offboarding workflows, and strictly justified, time-bound policy exemptions.
* **Continuous Compliance:** Standardized guardrails mapped via custom Azure Policies and Enterprise Initiatives to guarantee continuous security monitoring through Microsoft Defender for Cloud.

### 🌐 Secure Hub & Spoke Networking Model
* **IPAM & CIDR Strategy:** Deep assessment of On-premises CIDR ranges to ensure deterministic, non-overlapping IP allocation across hybrid networks.
* **Centralized Connectivity:** High-availability Hub Virtual Networks (VNets) hosting VPN Gateways and ExpressRoute circuits coupled with centralized Azure Firewall inspection engines.
* **Secured Egress & Private Channels:** Zero-trust architecture routing traffic via precise User Defined Routes (UDRs), Private Endpoints, and strictly isolated Private DNS Zones.

### 📜 Infrastructure as Code (IaC) Landing Zones
* **Production-Grade Terraform:** Modular, reusable, and deterministic IaC frameworks leveraging state-file encryption at rest and isolated remote backends with restricted least-privilege access.
* **Advanced Pipelines & Guardrails:** Automated validation workflows embedded with static code analysis (`tflint`), secret scanning (`gitleaks`), automated cloud costing tools (`infracost`), manual approval steps, and daily automated Drift Detection.

### 🚀 Enterprise DevSecOps Pipelines
* **Trunk-Based Branching Strategy:** Enforced through short-lived feature branches, mandatory code owners reviews, strict PR merge criteria, and branch protection rules prohibiting direct deletion.
* **Resilient Pipeline Templates:** Highly reusable Azure DevOps yaml blocks orchestrating atomic sequence phases: Validate & Test -> Artifact Build -> Dry Run / Plan -> Manual Approval -> Blue-Green Deployment -> Auto-Rollback.
* **Automated Configuration:** Immutable compute provisioning utilizing modular custom data scripts to bake middleware environments seamlessly on boot.

### 🔄 Large-Scale Cloud Migrations
* **CAF Framework Alignment:** Strategy built strictly around the **Microsoft Cloud Adoption Framework (CAF)** lifecycle phases: Strategy -> Plan -> Ready -> Adopt -> Govern -> Secure -> Manage.
* **Phased Migration Execution:** Executing structural multi-tier migration strategies driven by programmatic discovery assessments, hypercare observation support, and rigorous pre/during/post-cutover verification checklists.

### 💰 FinOps & Infrastructure Optimization
* **Wastage Mitigation:** Programmatic tracking to automatically clean up orphaned resources, unattached managed disks, oversized compute types, and unnecessary log ingestions.
* **Cost Control Policies:** Automated scheduling policies to shut down non-production workloads alongside strategic Reserved Capacity planning and calculated backup retention windows.

### 🛡️ Resilience, HA, & Observability
* **Business Continuity (BCDR):** High-availability constructs designed using Zone-Redundant (ZRS) and Geo-Redundant (GRS) configurations engineered to hit aggressive RTO and RPO objectives.
* **Observability Matrix:** End-to-end telemetry collections linking cross-subscription metrics to centralized Log Analytics workspaces and distributed monitoring dashboards.

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
