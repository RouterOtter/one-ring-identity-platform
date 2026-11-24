## Business Roles

| AD Group | Role Name | Description |
|-----------|-----------|-------------|
| GG_ROLE_KING | King | Executive leadership |
| GG_ROLE_STEWARD | Steward | Department managers |
| GG_ROLE_RANGER | Ranger | Operations and security personnel |
| GG_ROLE_LOREMASTER | Loremaster | Knowledge management and archives |
| GG_ROLE_WIZARD | Wizard | Identity and infrastructure administrators |
| GG_ROLE_SMITH | Smith | Engineering and development personnel |
| GG_ROLE_CITIZEN | Citizen | Standard workforce |
| GG_ROLE_ALLY | Ally | External partners |
| GG_ROLE_TRAVELER | Traveler | Temporary or guest access |


## Role to Entitlement Mapping

| Role Group | Keycloak | GLPI | Wazuh | Resource Access |
|------------|----------|------|--------|----------------|
| GG_ROLE_KING | KC_REALM_ADMIN | GLPI_SUPER_ADMIN | WAZUH_ADMIN | DL_FS_COUNCIL_RW |
| GG_ROLE_STEWARD | KC_MANAGER | GLPI_APPROVER | WAZUH_READONLY | DL_FS_COUNCIL_RW |
| GG_ROLE_RANGER | KC_USER | GLPI_TECHNICIAN | WAZUH_ANALYST | DL_FS_GONDOR_RW |
| GG_ROLE_WIZARD | KC_REALM_ADMIN | GLPI_SUPER_ADMIN | WAZUH_ADMIN | DL_FS_COUNCIL_RW |
| GG_ROLE_CITIZEN | KC_USER | GLPI_REQUESTER | N/A | DL_FS_HOBBITON_RO |


