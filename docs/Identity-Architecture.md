# Identity Architecture

## Domain

```text
middleearth.local
```

---

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
    │   ├─ Kingdom Groups
    │   ├─ Role Groups
    │   ├─ Application Access Groups
    │   └─ Resource Groups
    │
    ├─ Computers
    ├─ Servers
    ├─ Service Accounts
    └─ Privileged Accounts
```

---

## Kingdom Groups

Kingdom groups represent organizational or regional affiliation.

```text
SG_KINGDOM_GONDOR
SG_KINGDOM_ROHAN
SG_KINGDOM_RIVENDELL
SG_KINGDOM_HOBBITON
SG_KINGDOM_ISENGARD
SG_KINGDOM_MORDOR
```

---

## Role Groups

Role groups represent functional responsibilities within the organization.

```text
SG_ROLE_KING
SG_ROLE_WIZARD
SG_ROLE_LOREMASTER
SG_ROLE_STEWARD
SG_ROLE_COMMANDER
SG_ROLE_RANGER
SG_ROLE_SMITH
SG_ROLE_CITIZEN
SG_ROLE_ALLY
SG_ROLE_TRAVELER
SG_ROLE_WRAITH
SG_ROLE_DARKLORD
```

---

## Application Access Groups

Application access groups provide role-based access to business applications.

```text
SG_APP_PAL_USER
SG_APP_PAL_ADMIN

SG_APP_PP_USER
SG_APP_PP_APPROVER
SG_APP_PP_ADMIN

SG_APP_RIV_USER
SG_APP_RIV_ADMIN
```

### Applications

```text
PAL = Palantír Monitoring Platform
PP  = Prancing Pony Service Desk
RIV = Rivendell Knowledge Repository
```

---

## Resource Groups

Resource groups will be used to assign permissions to file shares and resources.

```text
DL_FS_GONDOR_RW
DL_FS_GONDOR_RO

DL_FS_HOBBITON_RW
DL_FS_HOBBITON_RO

DL_FS_COUNCIL_RW
```

### Naming Convention

```text
DL = Domain Local
FS = File Share

RW = Read/Write
RO = Read Only
```

---

## User Locations

### Gondor

```text
aragorn
boromir
faramir
denethor
beregond
```

### Rohan

```text
theoden
eomer
eowyn
gamling
```

### Rivendell

```text
elrond
legolas
glorfindel
arwen
```

### Hobbiton

```text
frodo
samwise
merry
pippin
```

### Isengard

```text
saruman
grima
```

### Mordor

```text
sauron
witchking
mouthofsauron
```

---

## Planned Identity Model

```text
User
  ↓
Kingdom Group
  ↓
Role Group
  ↓
Application Access Group
  ↓
Resource Group
  ↓
Access Granted
```

---

## Future Phases

### Phase 2
- Role assignments
- RBAC implementation
- Governance documentation

### Phase 3
- File Server (ME-FS01)
- AGDLP implementation
- NTFS permissions

### Phase 4
- Joiner / Mover / Leaver workflows
- Access reviews
- Identity governance

### Phase 5
- Security monitoring
- SIEM integration
- Threat simulation
