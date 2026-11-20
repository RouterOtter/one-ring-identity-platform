# 🧙 One Ring Identity Platform

A Lord of the Rings themed Identity and Access Management (IAM), Active Directory, and Systems Administration lab built using Microsoft Hyper-V and Windows Server.

The goal of this project is to simulate a small enterprise Identity Governance and Administration (IGA) environment using Middle-earth inspired identities, applications, resources, and access controls.

---

# Current Environment

## Domain

```text
middleearth.local
```

## Infrastructure

| Server | Role |
|----------|----------|
| ME-DC01 | Primary Domain Controller |

---

# Project Objectives

- Active Directory Administration
- Identity Access Management (IAM)
- Role-Based Access Control (RBAC)
- Active Directory Group Design
- Identity Governance
- User Lifecycle Management
- PowerShell Automation
- Windows Systems Administration

---

# Active Directory Organizational Structure

```text
middleearth.local
└─ Middle-Earth
    ├─ Users
    │  ├─ Gondor
    │  ├─ Rohan
    │  ├─ Rivendell
    │  ├─ Hobbiton
    │  └─ Mordor
    │
    ├─ Groups
    │  ├─ Role Groups
    │  ├─ Application Groups
    │  └─ Resource Groups
    │
    ├─ Computers
    ├─ Servers
    ├─ Service Accounts
    └─ Privileged Accounts
```

---

# Identity Model

## Role Groups

Role groups determine who a user is within the organization.

```text
SG_ROLE_KING
SG_ROLE_WIZARD
SG_ROLE_LOREMASTER
SG_ROLE_STEWARD
SG_ROLE_RANGER
SG_ROLE_SMITH
SG_ROLE_CITIZEN
SG_ROLE_ALLY
SG_ROLE_TRAVELER
```

---

## Application Groups

Application groups determine which applications a user can access.

```text
SG_APP_PAL_USER
SG_APP_PAL_ADMIN

SG_APP_PP_USER
SG_APP_PP_APPROVER
SG_APP_PP_ADMIN

SG_APP_RIV_USER
SG_APP_RIV_ADMIN
```

---

## Resource Groups

Resource groups control access to file shares and protected resources.

```text
DL_FS_GONDOR_RW
DL_FS_GONDOR_RO

DL_FS_HOBBITON_RW
DL_FS_HOBBITON_RO

DL_FS_COUNCIL_RW
```

---

# IAM Access Flow

The lab follows Active Directory RBAC and AGDLP principles.

```text
User
  ↓
Role Group
  ↓
Application Group
  ↓
Resource Group
  ↓
Access Granted
```

Example:

```text
Frodo
  ↓
SG_ROLE_CITIZEN
  ↓
SG_APP_PP_USER
  ↓
DL_FS_HOBBITON_RW
  ↓
File Share Access
```

---

# Current Progress

## Phase 1 - Active Directory Foundation

- [x] Hyper-V environment created
- [x] Windows Server 2022 installed
- [x] DNS configured
- [x] Active Directory Domain Services installed
- [x] middleearth.local forest created
- [x] Organizational Unit structure created
- [x] Initial RBAC group design implemented

## Phase 2 - Identity Administration

- [ ] Create fellowship user accounts
- [ ] Assign enterprise roles
- [ ] Configure privileged accounts
- [ ] Implement group memberships

## Phase 3 - Resource Access Management

- [ ] Deploy file server
- [ ] Configure AGDLP
- [ ] Implement NTFS permissions
- [ ] Create shared resources

## Phase 4 - Identity Governance

- [ ] Joiner Process
- [ ] Mover Process
- [ ] Leaver Process
- [ ] Access Reviews

## Phase 5 - Security Operations

- [ ] SIEM Integration
- [ ] Sysmon Monitoring
- [ ] Event Auditing
- [ ] Threat Simulation

---

# Lessons Learned

## Day 1

- Successfully deployed Active Directory Domain Services.
- Created the Middle-earth organizational hierarchy.
- Designed initial IAM-focused AD structure.
- Rebuilt the environment after losing administrator credentials.
- Implemented checkpoint and recovery planning for future work.

---

# Future Enhancements

- Microsoft Entra ID Integration
- Self-Service Access Requests
- Approval Workflows
- Group Lifecycle Management
- Governance Dashboard
- Automated Provisioning using PowerShell

---

> One Ring Identity Platform is an educational IAM and Systems Administration project designed to demonstrate enterprise identity management concepts using Active Directory, RBAC, governance processes, and automation.
