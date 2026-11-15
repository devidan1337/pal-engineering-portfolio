# Diagnosing a DNS failure on a segmented network

**Outcome** Local DNS resolution recovered during a controlled retest. Direct DNS to an external resolver still timed out, consistent with the intended network policy.

## Symptom

A test client could reach its local gateway, but queries to the expected local resolver timed out. The firewall itself could resolve names. I needed to determine whether the failure was at the client, along the packet path, or at the resolver.

## Investigation

| Check | Observation | What it narrowed down |
| --- | --- | --- |
| Client route and gateway | The client selected its directly connected Ethernet route and could reach the gateway. | Basic local reachability worked. |
| Resolver check from the firewall | Recursive resolution succeeded on the firewall. | The resolver could answer from at least one vantage point. |
| Capture during the failure | The expected client DNS packets were absent at the firewall capture point. | The resolver alone could not explain the client symptoms. |
| Endpoint VPN service state | The VPN interface appeared disconnected while associated background services were still active. | Endpoint filtering remained a plausible cause. |
| Controlled retest | After stopping those services, local DNS port and query tests succeeded. Direct external DNS still timed out. | Local DNS recovery and the external-DNS restriction were observed in the same retest. |

## Conclusion

Endpoint VPN filtering was the strongest supported explanation. The test established functional recovery. The particular service responsible and the existence of a vendor defect remained unresolved.

## What I’d carry into the next incident

Record the client route, interface, resolver, and background service state before changing firewall policy. Preserve a before-and-after observation and include a negative test for the behavior that should stay blocked.
