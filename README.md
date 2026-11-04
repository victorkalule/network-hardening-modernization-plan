# Network Hardening & Modernization Plan

**Security planning exercise | Network segmentation, identity, and risk reduction**

## About this project

For this training assignment, I put together a network and IT modernization proposal for a fictional organization with five locations. The company needed a practical way to improve security and simplify its infrastructure without taking on more work or cost than it could support.

I focused on what I would address first, what could wait, and how the recommendations would support day-to-day operations.

**This was a design and planning project. I did not deploy the proposed changes to a production network.**

## The main problems I considered

- Limited visibility into devices, software, and critical business systems across different locations.
- A firewall subscription that needed to be renewed or replaced.
- Servers, employee computers, and guest/BYOD devices that needed better separation.
- Aging systems and missing updates.
- A need for stronger administrator access controls and more useful security monitoring.
- Too much dependence on older on-premises infrastructure.

## My proposed plan

### 1. Find and document the important assets

Start with an inventory of hardware, software, system owners, and dependencies. Use a lightweight configuration management database (CMDB) to keep track of changes and identify systems that need attention.

### 2. Take care of the basic security gaps

Restore firewall protection and logging, separate different types of devices using VLANs, prioritize security patches, and require MFA for privileged and remote access.

### 3. Modernize without disrupting the business

Stabilize identity services, remove redundant systems only after checking dependencies, and consider moving suitable file services, backups, and other workloads to a hybrid-cloud setup.

### 4. Set up practical monitoring

Forward useful firewall and identity logs to a managed monitoring service. The proposal favored this over building an in-house SOC before the organization was ready for one.

### 5. Make the changes sustainable

Document access requests, account management, BYOD rules, incident response basics, and change approvals so the improvements can be maintained over time.

## Supporting documents

- [Five-phase hardening roadmap](docs/proposed-hardening-roadmap.md)
- [Conceptual network segmentation design](docs/conceptual-segmentation-design.md)

## What this project taught me

Security recommendations need to make sense for the organization they're meant to help. I worked on prioritizing risks, thinking through dependencies, and explaining why controls such as segmentation, patching, and MFA matter.

This repository is based on a TripleTen training proposal written in January 2026. The architecture and validation ideas are recommendations, not evidence of completed implementation or measured risk reduction. No original course reports, private network details, or credentials are included.
