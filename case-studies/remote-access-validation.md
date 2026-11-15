# Validating remote access and workstation recovery

**Outcome** Authenticated off-site access to Windows and its Linux workspace was verified. A complete shutdown, relay wake, and pre-login SSH cycle was observed at home.

## Problem

I wanted a way to resume work on a workstation remotely and determine why a recovery attempt stopped. A wake request crosses multiple boundaries. The relay has to send the packet on the right network, the workstation has to leave its power state, and authenticated access has to become available.

## Validation record

| Question | Result |
| --- | --- |
| Could I reach an authenticated workstation session off-site? | Verified Windows SSH and Linux workspace access. |
| Did the relay and target have the intended local delivery path? | Verified the wired placement after moving the relay into the same broadcast domain as the workstation. |
| Could I complete a shutdown, wake, and login cycle at home? | Recorded a successful cycle, including SSH before local login. |
| Did those results establish a repeatable, fully off-site power cycle? | The recorded validations cover separate stages. An integrated off-site cycle remained pending at the baseline checkpoint. |

The diagnostic value was separating what each observation proved. A transmitted packet proves the sender acted. Power-on confirms the transition. An authenticated session establishes usable access.
