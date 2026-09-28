# Release prerequisites (personal TestFlight distribution)

- [ ] Record the upstream code, SD3-family base VAE, derived extractor and
  stability profile's exact sources, license texts or grants, redistribution
  conditions, reviewer, and review date in `LICENSES/ASSET_RIGHTS.md`.
- [ ] Establish whether this fork's weights match the Wispio VAE v1 Core ML
  export. Do not change the Wispio source lock without byte and provenance
  evidence. Keep that runtime artifact release-ineligible while unresolved.
- [ ] Add a root license only after the rights holder confirms its scope. A new
  fork license cannot authorize upstream or third-party weights by itself.
- [ ] On the actual packaging Mac, generate a dedicated Ed25519 manifest-signing
  key with the reviewed `qa/tools/model_release_signing.swift` utility. Keep
  its private key in that Mac's Keychain; do not copy it into this repository.
- [ ] Export `MODEL_DISTRIBUTION/ed25519-public.pem` from that same key, verify
  its SHA-256 SPKI key ID, and pin both the key ID and exact release assets in
  the signed Wispio App catalog. Review the public key before merging it.
- [ ] Sign the exact immutable release manifest on the packaging Mac; verify
  the detached signature, archive SHA-256, model tree hashes, license records,
  and minimum App/runtime version before publishing a release attachment.

Until these items are complete, this fork is not a model download source for
TestFlight or production. GCSA publication needs its own approved signing key.
