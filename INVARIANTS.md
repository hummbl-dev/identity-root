# INVARIANTS

## I-01: Explicit Authority

**Invariant**: Every permission or capability in the system must be traceable to an explicit cryptographic delegation chain originating from a recognized trust root.

**Failure Mode**: Implicit or ambient authority allows unauthorized actions to execute without proper cryptographic proof, breaking the security model and enabling privilege escalation attacks.

## I-08: Irreversibility Awareness

**Invariant**: All state transitions that cannot be reversed (such as key revocations, credential burns, or authority terminations) must be clearly marked and require explicit acknowledgment before execution.

**Failure Mode**: Unaware execution of irreversible operations leads to permanent loss of access, data, or authority relationships with no recovery path, causing operational failures and potential system lockout.
