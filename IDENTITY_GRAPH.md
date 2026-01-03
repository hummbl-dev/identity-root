# IDENTITY_GRAPH

## Identity Plane

The identity plane establishes entities and their cryptographic identifiers within the system. This plane defines:

- **Entity Types**: Natural persons, organizations, services, devices
- **Identifier Format**: Base120-encoded cryptographic identifiers (v1.0 frozen)
- **Identity Binding**: Cryptographic public keys bound to entity identifiers
- **Verification**: Proof-of-possession mechanisms for identity claims

## Control Plane

The control plane governs authority relationships and permission flows. This plane defines:

- **Authority Delegation**: Explicit chains from root authorities to derived permissions
- **Permission Scopes**: Bounded capabilities tied to specific operations
- **Revocation Paths**: Irreversible state transitions for compromised authorities
- **Temporal Constraints**: Time-bound validity windows for delegated authority

## Trust Roots

Trust roots anchor the system's security guarantees. Defined roots include:

- **Genesis Authority**: Self-signed root identifier for system bootstrap
- **Recovery Authorities**: N-of-M threshold authorities for root key rotation
- **Audit Authority**: Read-only observer with verification-only permissions
- **Temporal Anchor**: Block height or timestamp authority for time-based operations

## Dependencies

The identity system maintains explicit dependency relationships:

- **Cryptographic Primitives**: Ed25519 signatures, SHA-256 hashing, Base120 encoding
- **Storage Layer**: Content-addressed immutable data structures
- **Network Layer**: Transport-agnostic message passing
- **Clock Source**: Monotonic logical clocks for partial ordering

## Graph Properties

- **Acyclic Authority**: No authority delegation cycles permitted
- **Explicit Edges**: All relationships require cryptographic proof
- **Immutable History**: State transitions preserved in audit log
- **Bounded Depth**: Maximum delegation chain depth enforced
