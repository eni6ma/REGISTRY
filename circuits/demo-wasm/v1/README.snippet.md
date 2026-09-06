# demo-wasm / v1

Test publish of a DEMO-MINT wasm cohort onto feat/wasm-circuits.

| Artifact | Role |
|----------|------|
| `eni6ma_cohort_wasm_mint-job-99bb0806-e3f9-40c5-a916-f9c9f4a4ace2.zip` | Full cohort zip (contains eni6ma_wasm.wasm + private.json) |
| `eni6ma_cohort_wasm_mint-job-99bb0806-e3f9-40c5-a916-f9c9f4a4ace2.zip.sha256` | SHA-256 of the zip bytes |
| `eni6ma_wasm.wasm` | Isolated WASM for browser load |
| `eni6ma_wasm.wasm.sha256` | SHA-256 of the WASM bytes |

## Raw URLs (this branch)

- WASM: https://raw.githubusercontent.com/eni6ma/REGISTRY/feat/wasm-circuits/circuits/demo-wasm/v1/eni6ma_wasm.wasm
- WASM digest: https://raw.githubusercontent.com/eni6ma/REGISTRY/feat/wasm-circuits/circuits/demo-wasm/v1/eni6ma_wasm.wasm.sha256
- Cohort zip: https://raw.githubusercontent.com/eni6ma/REGISTRY/feat/wasm-circuits/circuits/demo-wasm/v1/eni6ma_cohort_wasm_mint-job-99bb0806-e3f9-40c5-a916-f9c9f4a4ace2.zip

## Client rule

Fetch WASM + sidecar; recompute SHA-256; match or fail closed before instantiate.

Note: The cohort zip embeds private.json for mint/test continuity. Prefer loading the isolated WASM + digest in production browsers; treat zip private.json as sensitive.
