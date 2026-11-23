# 🧙 One Ring Identity Platform

A Lord of the Rings themed Identity and Access Management (IAM), Active Directory, and Systems Administration lab built on Microsoft Hyper-V.

The goal of this project is to simulate an enterprise Identity Governance and Administration (IGA) environment using Active Directory, RBAC, access governance, lifecycle management, and security administration concepts within a Middle-earth themed organization.

---

# Current Environment

## Platform

- Hyper-V
- Windows Server 2022
- Active Directory Domain Services
- DNS

## Domain

```text
middleearth.local
```

## Infrastructure

| Server | Role |
|----------|----------|
| ME-DC01 | Domain Controller & DNS Server |

---

# Active Directory Design

## Organizational Units

```text
middleearth.local
└─ Middle-Earth
    ├─ Users
    │   ├─ Gondor
    │   ├─ Rohan
    │   ├─ Rivendell
    │   ├─ Hobbiton
    │   ├─ Isengard
    │   └─ Mordor
    │
    ├─ Groups
    │   ├─ Role Groups
    │   ├─ Application Groups
    │   └─ Resource Groups
    │
    ├─ Computers
    ├─ Servers
    ├─ Service Accounts
    └─ Privileged Accounts
```

---

# Identity Governance Model

## Role Groups

Role groups define a user's business role.

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

Application groups define access to business systems.

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

Resource groups will control file share and infrastructure permissions.

```text
DL_FS_GONDOR_RW
DL_FS_GONDOR_RO

DL_FS_HOBBITON_RW
DL_FS_HOBBITON_RO

DL_FS_COUNCIL_RW
```

---

# IAM Access Model

The lab follows RBAC and Active Directory group nesting concepts.

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

---

# Current User Population

## Gondor

```text
aragorn
boromir
faramir
denethor
beregond
```

## Rohan

```text
theoden
eomer
eowyn
gamling
```

## Rivendell

```text
elrond
legolas
glorfindel
arwen
```

## Hobbiton

```text
frodo
samwise
merry
pippin
```

## Isengard

```text
saruman
grima
