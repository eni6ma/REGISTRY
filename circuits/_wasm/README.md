# WASM circuits (Path B)

Branch: `feat/wasm-circuits`

This branch hosts **minted WASM** circuit artifacts for browser / Wasmer clients.
`main` keeps the existing linux/amd64 ELF Path B twins (`eni6ma` + `eni6ma.sha256`).

## Layout (per circuit version)

```text
circuits/<circuit_id>/<version>/
  eni6ma_wasm.wasm          # published WASM bytes (Path-B pin; not Git LFS)
  eni6ma_wasm.wasm.sha256   # 64 hex digest of those bytes + trailing newline OK
  index.html                # optional Path-B browser smoke
  pkg/                      # optional wasm-bindgen web glue for browser run
  README.snippet.md         # optional human metadata
```

**Never commit `private.json` or mint secrets.**

## Validity rule (client)

1. Fetch `eni6ma_wasm.wasm` and `eni6ma_wasm.wasm.sha256` from this repo (raw URLs on this branch or after merge).
2. Compute SHA-256 over the exact downloaded WASM bytes.
3. Compare to the sidecar (trim whitespace). Mismatch or missing sidecar → **fail closed**.
4. Only then instantiate / run the module in the browser.

URL hint is untrusted; the digest is the pin. Prefer pinning the digest from Circuit Authority / onboarding, not from a client-supplied claim.

## Mint → publish

1. Mint with DEMO-MINT: `./scripts/mint-variant.sh wasm`
2. Unzip cohort: take `eni6ma_wasm.wasm` only
3. `shasum -a 256 eni6ma_wasm.wasm | awk '{print $1}' > eni6ma_wasm.wasm.sha256`
4. Place under `circuits/<id>/<version>/` and push to this branch (or use GCP publisher)

## Browser smoke (`demo-wasm/v1`)

Serve `circuits/demo-wasm/v1` over HTTP, open `index.html`, run the smoke. Digest must match before bindgen init. See that directory’s `README.snippet.md`.
