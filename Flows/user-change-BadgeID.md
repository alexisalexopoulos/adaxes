```mermaid
flowchart-elk
%% Nodes
start((start))
hasbadgeID{has badge ID}
accessdenied[access denied]
umrapoc{Account with same badgeID in UmraPoC}
badgeidpresent{account already present with badge ID}
setbadgeIDtarget[set badge ID from current user to inactive user]
replaceID[replace existing badge ID on active account with given badgeID]
deprovision[start deprovision flow inactive newly created account]
cancel[cancel operation]
finish((end))
%%linking
start -->hasbadgeID
hasbadgeID --> |NO| accessdenied
hasbadgeID --> |YES| badgeidpresent
badgeidpresent --> |YES|umrapoc
umrapoc --> |NO| cancel
umrapoc --> |YES| setbadgeIDtarget--> replaceID --> deprovision -->  finish
badgeidpresent -->|NO|replaceID --> finish
```