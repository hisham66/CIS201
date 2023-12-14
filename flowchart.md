```mermaid
flowchart LR
    start((Start)) --> login{Merchant Logs In}
    login --> staffTab[Select "Merchant Staff Tab"]
    staffTab --> decision{Decision: Action?}
    decision -->|Create| inputDetails[Input Email, Name, Phone]
    inputDetails --> assignRoles[Assign Roles/Permissions]
    assignRoles --> createSubUser[Create Sub-User]
    decision -->|View| viewSubUsers[Display Sub-Users]
    decision -->|Edit| selectSubUser[Select Sub-User]
    selectSubUser --> editDetails[Edit Details/Permissions]
    editDetails --> updateSubUser[Update Sub-User]
    decision -->|Delete| selectSubUserToDelete[Select Sub-User]
    selectSubUserToDelete --> confirmDeletion[Confirm Deletion]
    createSubUser --> end((End))
    viewSubUsers --> end
    updateSubUser --> end
    confirmDeletion --> end
```