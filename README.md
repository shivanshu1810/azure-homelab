# Azure Homelab — Beginner Build Writeup

A self-directed learning project: a small Azure homelab I planned and built with free/student resources to practise cloud fundamentals that support an IT support career — networking, a Windows Server virtual machine, identity basics, file sharing, backup, and cost control.

> **Honest framing:** This is a personal learning lab, not professional Azure employment experience, and I do not hold Azure certifications. Everything here was built in a free/student subscription, at the smallest sizes, and torn down or auto-shut-down when not in use. Steps are written so another beginner can follow them; where a step can vary by region or portal layout, I say so.

## What the lab includes

| Guide | What it covers |
|---|---|
| [01 — Virtual network and Windows Server VM](docs/01-network-and-vm.md) | Resource group, virtual network and subnet, a small Windows Server VM, and connecting by RDP |
| [02 — Entra ID basics](docs/02-entra-id-basics.md) | Users, groups, and the identity ideas behind Microsoft 365 sign-ins |
| [03 — Azure Files share](docs/03-file-share.md) | A storage account and a file share you can map from Windows |
| [04 — Backup](docs/04-backup.md) | Recovery Services vault and a basic VM backup policy |
| [05 — Cost controls](docs/05-cost-controls.md) | Auto-shutdown, free-tier/small-size choices, budgets and alerts, and cleaning up |

## How to use this repo

Read the guides in order — each one builds on the previous one and ends with a short "check it worked" step and a cleanup note. You need:

- An Azure account with a free or student subscription (no payment beyond that subscription's own rules)
- A Windows PC for RDP and mapping the file share
- About 30–45 minutes per guide, working slowly

## Skills demonstrated

- Cloud fundamentals: resource groups, regions, virtual networks, subnets, and network security groups
- Windows Server basics in Azure: creating a VM, connecting securely, and keeping sizes appropriate for learning
- Identity concepts: users, groups, and how Entra ID relates to Microsoft 365 accounts
- Storage and protection: Azure Files, Recovery Services vault, and backup policies
- Cost discipline: auto-shutdown, budgets/alerts, and deleting resources when finished

## About

Recent Computer Systems Technician – Networking graduate (Georgian College, 2026) with Tier 1 Service Desk Analyst co-op experience at Royal Victoria Regional Health Centre, supporting Windows 11, Microsoft 365, Active Directory, and Halo ITSM. This lab is how I am extending that on-prem and Microsoft 365 experience into Azure fundamentals.
