# demo-wasm / v1

Test publish of a DEMO-MINT wasm cohort onto feat/wasm-circuits.

| Artifact | Role |
|----------|------|
| `eni6ma_cohort_wasm_mint-job-99bb0806-e3f9-40c5-a916-f9c9f4a4ace2.zip` | Full cohort zip (contains eni6ma_wasm.wasm + private.json) |
| `eni6ma_cohort_wasm_mint-job-99bb0806-e3f9-40c5-a916-f9c9f4a4ace2.zip.sha256` | SHA-256 of the zip bytes |
| `eni6ma_wasm.wasm` | Isolated WASM for browser load |
| `eni6ma_wasm.wasm.sha256` | SHA-256 of the WASM bytes |
| `index.html` | Path-B browser smoke (digest → bindgen → `build_minimal_proof`) |
| `pkg/` | wasm-bindgen web glue (`eni6ma_wasm.js` + `eni6ma_wasm_bg.wasm`) |

## Raw URLs (this branch)

- WASM: https://raw.githubusercontent.com/eni6ma/REGISTRY/feat/wasm-circuits/circuits/demo-wasm/v1/eni6ma_wasm.wasm
- WASM digest: https://raw.githubusercontent.com/eni6ma/REGISTRY/feat/wasm-circuits/circuits/demo-wasm/v1/eni6ma_wasm.wasm.sha256
- Cohort zip: https://raw.githubusercontent.com/eni6ma/REGISTRY/feat/wasm-circuits/circuits/demo-wasm/v1/eni6ma_cohort_wasm_mint-job-99bb0806-e3f9-40c5-a916-f9c9f4a4ace2.zip

## Client rule

Fetch WASM + sidecar; recompute SHA-256; match or fail closed before instantiate.

Note: The cohort zip embeds private.json for mint/test continuity. Prefer loading the isolated WASM + digest in production browsers; treat zip private.json as sensitive.

## Local browser smoke

```bash
cd circuits/demo-wasm/v1
python3 -m http.server 8765
# open http://127.0.0.1:8765/ → Run proof smoke
```

Path-B gates on published `eni6ma_wasm.wasm` bytes; runtime loads `pkg/eni6ma_wasm_bg.wasm`. Challenge needs `timestamp`. BigInt-safe JSON for `tau`. Never publish loose `private.json` for browsers.
