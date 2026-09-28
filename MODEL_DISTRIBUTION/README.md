# Wispio model release verification (personal TestFlight source)

The distribution signing key must be generated on the designated packaging
Mac. This fork does not yet contain a trusted distribution public key. Before
publishing a release, generate an Ed25519 key there, add its SPKI public key as
`ed25519-public.pem`, and pin its SHA-256 key ID here and in the app catalog.
Keep the private key on the packaging Mac; never commit or attach it.

The future key will belong to `quinn521/Image-Steganography-Invisible-Watermark-Pipeline`
TestFlight resource releases. It will not authorize Apple app signing or a
future GCSA production publisher. Consumers must pin the repository, release
tag, asset name, archive SHA-256, manifest signing key ID, model tree hashes,
and supported App/runtime range in the signed App catalog. A GitHub URL or
public key alone grants no model identity or redistribution right.

Do not publish an asset until its exact model and all included third-party
files have recorded source, license, redistribution permission, and digests
in `LICENSES/ASSET_RIGHTS.md`. Release attachments must be immutable; corrections
use a new tag. GCSA promotion republishes byte-identical approved archives
with a separate GCSA signing identity and a new App catalog.
