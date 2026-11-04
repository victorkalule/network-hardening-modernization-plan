# Conceptual Network Segmentation Design

> **Design exercise only:** This is a simplified, illustrative architecture derived from the training proposal's recommended separation of servers, employee workstations, and guest/BYOD devices. It is not a map of any actual deployed network.

## Proposed logical layout

```text
                   External networks / Internet
                               |
                    Managed perimeter firewall
                   (filtering, IPS, security logs)
                               |
                     Core switching / routing
                    ___________|____________
                   |           |            |
              Server VLAN  Employee VLAN  Guest/BYOD VLAN
                   |           |            |
             Business apps  Staff PCs      Untrusted devices
             Identity svc.  Managed users   Internet access only
                   |
          Controlled, documented access

     Firewall and identity logs --> Managed monitoring provider
```

## Example policy principles

| Source zone | Destination | Proposed rule intent |
| --- | --- | --- |
| Guest/BYOD | Internal business networks | Deny by default unless a documented exception is required |
| Employee | Necessary business services | Allow only approved application traffic |
| Server | Other protected segments | Restrict to documented service dependencies |
| Administrative access | Identity and server infrastructure | Require approved administrative path and strong authentication |
| Security devices / identity systems | Managed monitoring | Send relevant security event records securely |

These are **proposed least-privilege principles**, not actual configured firewall rules. Specific ports, protocols, identities, and routing decisions would require validated asset dependencies and authorized implementation testing.

## Review questions before deployment

1. Which existing applications require cross-segment communications?
2. Which assets must remain on-premises for latency, compatibility, or continuity reasons?
3. How are administrative access, guest Wi-Fi, and remote users separated?
4. Who owns each inter-VLAN firewall exception and how is it reviewed?
5. Can authorized testing confirm that permitted business flows work and prohibited paths are blocked?

## Outcome expected, not measured

The intended result is to limit unnecessary reachability, reduce potential lateral-movement paths, and make monitoring easier. **The source proposal does not establish that these outcomes were achieved.**
