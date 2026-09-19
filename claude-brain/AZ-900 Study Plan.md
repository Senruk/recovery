---
name: "AZ-900 Study Plan"
description: Microsoft Azure Fundamentals certification plan. 6-domain syllabus, free learning path, practice-test strategy, exam booking.
type: project
---


# AZ-900 — Microsoft Azure Fundamentals

**Started:** 2026-09-01
**Goal:** Pass AZ-900. Foundation-level, no prerequisites. Good first cert for the AI engineering track (shows real cloud, not just vibe-coding).

---

## Exam Structure

- **Format:** 50 multiple-choice questions
- **Duration:** 90 minutes
- **Pass mark:** 70% (35/50)
- **Cost:** ~£50–70 (varies; book at microsoft.com/learn → exam)
- **Retake policy:** 24 hours between attempts, up to 5 retries

---

## 6 Domains (weightings are approximate)

| # | Domain | Weight |
|---|--------|--------|
| 1 | Describe cloud concepts (public/private/hybrid, IaaS/PaaS/SaaS, elasticity, scalability) | 20–25% |
| 2 | Describe Azure workload and availability (regions, availability zones, SLAs, disaster recovery) | 10–15% |
| 3 | Describe Azure architecture and products (compute, storage, networking, apps) | 25–30% |
| 4 | Describe Azure management and governance (portal, CLI, PowerShell, resource groups, tags, RBAC, policies, Cost Management, Monitor) | 15–20% |
| 5 | Describe Azure security (AD, RBAC, NSGs, Firewall, Key Vault, encryption) | 10–15% |
| 6 | Describe Azure pricing and support (tiers, calculators, support plans, lifecycle) | 10–15% |

---

## Free Learning Path

1. **Microsoft Learn: Azure Fundamentals path** (100% free)
   - `AZ-900: Fundamentals of Azure` → 4 modules + assessments
   - https://learn.microsoft.com/training/paths/azure-fundamentals/
   - Do all 4 modules, take the module quizzes.

2. **Microsoft Learn: Azure Fundamentals (exam prep)**
   - https://learn.microsoft.com/training/modules/az-900-exam-prep/
   - Skills assessment with hints — the closest thing to the real exam.

3. **Microsoft Learn: Practice assessments**
   - Free 30-question practice test per skill area.

4. **YouTube (backup):** "AZ-900 Exam Prep" by Microsoft + free channels (John Savill, ITFreeTraining).

5. **MeasureUp / Whizlabs (paid, optional):** Full practice exams. Worth it if the free ones feel too easy. ~£25.

---

## Weekly Plan (6 weeks)

| Week | Focus | Outcome |
|------|-------|---------|
| 1 | Cloud concepts + Azure regions/availability | Can explain IaaS/PaaS/SaaS and where Azure runs |
| 2 | Compute + storage (VMs, App Service, Blob, Disk) | Can pick the right service for a workload |
| 3 | Networking (VNet, NSG, DNS, Firewall, VPN, ExpressRoute) | Can describe basic network topology |
| 4 | Management & governance (portal, CLI, RBAC, policies, tags, Cost) | Can navigate the portal and explain RBAC roles |
| 5 | Security (AD, RBAC, Key Vault, encryption, backup) | Can describe security controls |
| 6 | Pricing, support, SLAs + full practice exams + book exam | Ready to sit |

**Daily:** 45–60 min. One module section + its quiz. Don't skip the quizzes — they're the memory check.

---

## Key Concepts to Memorise (cheat-sheet)

- **IaaS / PaaS / SaaS:** IaaS = you manage OS (VMs). PaaS = you manage code (App Service). SaaS = you use it (Office 365).
- **Azure regions vs availability zones:** Region = geographic area. Zone = data centre within a region (1, 2, 3).
- **SLA:** Service Level Agreement — uptime guarantee.
- **RBAC roles:** Owner, Contributor, Reader, User Access Administrator, Backup Reader, etc.
- **Resource group:** Logical container. Can't span regions but can hold resources from different regions.
- **Tags:** key-value pairs for cost grouping.
- **Azure AD:** Identity. Not the same as on-prem AD (no domain join).
- **NSG:** Network Security Group — rules at subnet or NIC level.
- **Key Vault:** Stores secrets, keys, certificates.
- **Backup vs disaster recovery:** Backup = restore point in time. DR = failover to another region.
- **Support plans:** Developer (free), Standard, Professional Direct, Premier. Each unlocks more features.

---

## Exam Day Checklist

- [ ] Book exam at microsoft.com/learn → Certifications
- [ ] Have a quiet room, webcam, stable internet
- [ ] Government ID ready
- [ ] Clear desk — no notes
- [ ] 50 questions, 70% pass. Read every question twice; many have "select all that apply"

---

## After AZ-900

- Add "Microsoft Azure Fundamentals (AZ-900)" to CV
- Next cert options: Azure AI-900 (AI fundamentals — pairs well with the AI engineering track), then AZ-204 (Developer Associate, needs more hands-on)