# Asset rights register

This fork has no verified root license grant for all upstream code and
weights. A model signature proves the published bytes, not permission to
distribute them. The records below are release gates, not license grants.

| Asset group | Pinned source | Redistribution status | Evidence needed before a public release |
|---|---|---|---|
| Existing Wispio VAE v1 Core ML export | `erjinyi/watermark@979b1e96a7c217c56c383ec1b4ee4d9cd9da7c6b`, `VAE_v1.0` | **Unresolved** in the Wispio native adapter source lock | Base VAE, fine-tuned extractor, training data, stability profile, conversion, and derived weight redistribution rights; exact hashes |
| This repository's VAE pipeline weights | `gcsagroup/Image-Steganography-Invisible-Watermark-Pipeline@9f126633893651140b0821f23dda1b848d6bdcfd` | Pending | Source and weight licenses and proof of any relationship to the Wispio VAE v1 bytes |
| Referenced SD3-family base VAE | The exact upstream checkpoint is not pinned in this repository's rights record | **Unresolved** | Identify the exact Stability AI model and accepted license version; review use, modification, and redistribution conditions for the intended TestFlight and public distribution |

The repository's current VAE pipeline is not automatically identical to the
Wispio VAE v1 runtime artifact. Do not change the Wispio source lock to point
here without byte identity and a new review. Store the final reviewed license
text or immutable source link, reviewer, review date, and decision alongside
each signed release manifest.
