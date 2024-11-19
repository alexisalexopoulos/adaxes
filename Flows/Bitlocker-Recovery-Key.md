```mermaid
    flowchart-elk
    start[Execute Bitlocker recovery key]
        validation{Is computer in OU/subtree:
        ASP
        Campus
        Courtroom
        DCS
        Deployment
        Field Offices
        OTP
        OTR
        Win7}
    AccessDenied[Access Denied]
    Bitlocker[show Bitlocker recovery key]
start --> validation
validation --> |NO| AccessDenied
validation --> |YES| Bitlocker
```