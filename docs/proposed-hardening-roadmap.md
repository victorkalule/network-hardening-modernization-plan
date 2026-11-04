# Proposed Hardening Roadmap

> **Status:** Proposed design / training case study. The work below is not presented as having been implemented or independently validated.

## Phase 1 — Establish asset visibility

**Source-derived recommendations**

- Inventory servers, workstations, network devices, applications, and operating systems across the five-site training scenario.
- Record system ownership, business purpose, lifecycle state, and critical dependencies in a lightweight CMDB.
- Classify essential business systems and data, including finance, inventory, and customer information.

**Suggested implementation evidence if carried out later:** Redacted asset inventory, data classification summary, change-log entry, or dependency diagram.

## Phase 2 — Restore foundational network protections

**Source-derived recommendations**

- Renew or replace the expired home-office firewall subscription.
- Enable traffic filtering, intrusion prevention, and logging.
- Separate server, employee, and guest/BYOD networks using VLANs.
- Apply critical patches to servers and endpoints, documenting changes.
- Enable MFA for privileged and remote access accounts.

**Suggested validation methods (not performed in the source):** Review firewall and IDS status, test permitted/blocked inter-VLAN paths in an authorized lab, inspect patch compliance, and confirm MFA enforcement for in-scope accounts.

## Phase 3 — Stabilize and simplify infrastructure

**Source-derived recommendations**

- Introduce a supported Windows Server 2022 domain controller at the main office while maintaining branch-site read-only domain controllers where appropriate.
- Remove redundant systems after dependency assessment.
- Move suitable file services, backups, and non-latency-sensitive workloads toward cloud services while retaining necessary on-premises components.
- Keep an understandable, measured hybrid design that can be maintained across locations.

**Suggested validation methods (not performed in the source):** Recovery tests, identity service health checks, and documented migration or rollback plans.

## Phase 4 — Establish useful monitoring

**Source-derived recommendations**

- Send firewall and identity logs to a managed security monitoring service rather than staffing an internal SOC for the training scenario's current needs.
- Alert on unauthorized access attempts, malware-related activity, and operational failures.
- Avoid adding SOAR before the organization has sufficient process maturity and a demonstrated need.

**Suggested validation methods (not performed in the source):** Confirm log arrival and timestamps, validate alert ownership and escalation, and run agreed benign test events.

## Phase 5 — Improve governance and change discipline

**Source-derived recommendations**

- Document acceptable-use, BYOD, account management, access control, and basic incident response procedures.
- Use SaaS device management to require encryption, screen locks, and corporate-data remote wipe capability for BYOD.
- Standardize approvals for account creation, permission changes, and system updates.

**Suggested validation methods (not performed in the source):** Policy approval records, device-compliance reports, and sampled access/change tickets.

## Prioritization note

The **five phases follow the source proposal's order**. The source document does not include formal cost estimates, implementation dates, measured risk reductions, or verified completed changes. Those should be added only after real implementation evidence exists.
