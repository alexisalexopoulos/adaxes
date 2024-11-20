```mermaid
flowchart TB
%% Nodes
start((start))
    subgraph group [group management]
    direction TB
        managedgroup{Managed Groups}-->|YES|add[Add user to group]
        managedgroup{Managed Groups}-->|NO|accessdenied[accessdenied]
    end
start --> group
group --> finish((end))
```