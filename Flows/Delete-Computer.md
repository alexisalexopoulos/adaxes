```mermaid
    flowchart-elk
    start[Start delete computer]
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
    Delete[Delete Computer]
start --> validation
validation --> |NO| AccessDenied
validation --> |YES| Delete
```