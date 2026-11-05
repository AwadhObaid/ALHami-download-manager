# ALHami's update keys (ADR-0011, section 3)

These public keys are built into ALHami (`src/update.rs`) and are also
used to verify the signed video-tools list. Private keys must never be
stored in this directory or committed to the repository.

- `signing.pub`: the ALHami release signing public key. Its matching
  private key is held by the owner and must be supplied securely to the
  GitHub `release` environment before publishing signed releases or tools
  lists.
- `emergency.pub`: optional offline recovery key, used only if the
  signing key is compromised (ADR-0011, section 4). It is currently empty;
  ALHami accepts no emergency-key signatures until a separate recovery key
  is generated and added here.

The signing public key is configured. No signed release or tools list can
be produced without the matching private key, and no private key belongs
in this repository.
