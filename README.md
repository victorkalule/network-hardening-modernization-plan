# Network Hardening & Security Modernization Plan

**Project type:** Cybersecurity architecture and risk-reduction proposal (training case study)  
**Role:** Security analyst — assessment and recommendations  
**Focus:** Network segmentation, firewall security, identity hardening, monitoring, and phased IT modernization

## Executive summary

I developed a phased network and infrastructure security modernization proposal for a **simulated, multi-site organization** preparing for an ownership transition. The goal was to reduce avoidable cyber risk, improve asset visibility, stabilize core IT operations, and propose a practical future-state architecture without unnecessary spending.

This project documents **analysis, prioritization, and design recommendations**. It is **not evidence that I deployed the proposed controls to a production environment**.

## Security challenges identified in the training scenario

- Incomplete visibility of hardware, software, critical business services, and their dependencies across five locations.
- An expired firewall subscription at the main office, calling for renewed or replacement perimeter protection.
- Insufficient separation of servers, staff devices, and guest/BYOD traffic.
- Unpatched or unsupported infrastructure requiring a controlled modernization approach.
- Need for stronger privileged-access controls, ongoing monitoring, documentation, and business continuity planning.
- Desire to simplify a mixed on-premises environment through selective migration to a hybrid model.

## Proposed security improvements

| Workstream | Recommendation | Security purpose |
| --- | --- | --- |
| Asset management | Inventory devices, applications, owners, and dependencies; maintain a lightweight CMDB | Know what to protect and support change control |
| Network perimeter | Renew or replace the firewall service; enable filtering, intrusion prevention, and logging | Restore baseline traffic protection and visibility |
| Network segmentation | Separate servers, employee workstations, and guest/BYOD devices into distinct VLANs | Limit unnecessary cross-segment access and lateral-movement opportunities |
| Patch and identity hygiene | Patch critical systems, modernize supported identity infrastructure, and require MFA for privileged/remote access | Reduce exposure from outdated systems and compromised credentials |
| Monitoring | Send firewall and identity events to a managed security monitoring provider | Provide useful alerts without building an internal SOC prematurely |
| Operating controls | Document access management, BYOD, acceptable use, change approval, and basic incident response | Make security practices consistent and auditable |
| Architecture | Use a measured hybrid-cloud approach for suitable files, backups, and workloads | Improve resiliency and reduce unnecessary on-premises complexity |

## Proposed implementation approach

1. **Discover:** Build an asset inventory, identify critical data and services, and document dependencies.
2. **Secure essentials:** Restore firewall coverage, segment networks, patch critical assets, and enforce privileged-user MFA.
3. **Modernize selectively:** Stabilize identity services, consolidate systems where appropriate, and migrate suitable workloads to a hybrid model.
4. **Monitor:** Use managed monitoring for firewall and identity events, prioritizing actionable alerts over unnecessary tool complexity.
5. **Govern:** Establish lightweight IT policies, BYOD controls, approval processes, and incident response basics.

For a detailed planning view, see [the proposed hardening roadmap](docs/proposed-hardening-roadmap.md) and [the conceptual segmentation design](docs/conceptual-segmentation-design.md).

## Key security concepts demonstrated

- **Defense in depth:** Combine network controls, secure identities, patching, and monitoring rather than relying on one technology.
- **Least privilege:** Propose approved access paths between segments and stronger controls for privileged accounts.
- **Risk-based prioritization:** Address high-impact security hygiene before complex modernization.
- **Operational pragmatism:** Favor managed monitoring and selective migration when staffing and budget are constrained.
- **Clear communication:** Translate infrastructure improvements into availability, resilience, audit readiness, and business continuity benefits.

## Deliverables

- [Proposed hardening roadmap](docs/proposed-hardening-roadmap.md)
- [Conceptual network segmentation design](docs/conceptual-segmentation-design.md)

## Source and limitations

Adapted from a network modernization proposal I wrote for a **TripleTen cybersecurity training exercise** in January 2026. The underlying source is a **proposal**; there are no verified deployment logs, firewall exports, packet captures, or measured production outcomes in the source document. Any example controls and verification criteria in the companion files are **design-level suggestions** for a future implementation, not claims of completed changes.

Original course materials, confidential information, credentials, actual network diagrams, and internal configuration files are not included.
