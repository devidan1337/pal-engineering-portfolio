# Dan Padro — PAL Engineering Portfolio

PADRO AI Labs (PAL) is my independent engineering lab for network operations, local AI retrieval, and governed automation. I work in telecom switch and transport operations. In PAL, I apply the same habits of fault isolation, change validation, and evidence-based handoff to systems I can build and test myself.

## Start here

| Workstream | What I tested or documented |
| --- | --- |
| [Network troubleshooting](case-studies/segmented-network-dns.md) | Isolated a client DNS failure and verified recovery while checking the restriction on direct external DNS. |
| [Remote access and recovery](case-studies/remote-access-validation.md) | Verified authenticated off-site access and recorded the shutdown, wake, and login observations separately. |
| [Governed artifact closeout](case-studies/governed-artifact-closeout.md) | Produced a pending-review packet and verified that a restricted item was excluded from reading. |
| [Candidate ingestion and integrity](case-studies/approval-aware-ingestion.md) | Admitted individually approved documents and verified duplicate refusal, with source and approval traceability. |
| [Read-only retrieval and agent handoff](case-studies/read-only-retrieval-and-handoff.md) | Verified a one-tool interface, measured a token reduction, and used a retrieved excerpt in a documentation review. |
| [Encrypted storage and evidence governance](case-studies/storage-recovery-and-governance.md) | Tested recovery using synthetic data and separated storage, recovery custody, and authorization decisions. |

## Reusable standards

- [Network change record](standards/network-change-record.md)
- [Validation evidence](standards/validation-evidence.md)
- [VLAN design patterns](standards/vlan-design-patterns.md)
- [Management-plane security](standards/management-plane.md)

## Design and review record

The [proposal archive](proposals/README.md) documents 18 scoped proposals, including voice-first access, agent authority, and evidence workflows. Each entry explains its purpose, disposition, and what would justify further work.

The portfolio uses sanitized records from my independent lab. Case studies state the test scope and evidence limits. Live configuration, raw evidence, and operational recovery material are retained privately.
