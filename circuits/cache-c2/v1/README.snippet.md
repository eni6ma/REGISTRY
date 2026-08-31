## Circuit provenance (paste into eni6ma/REGISTRY)

| Field | Value |
|-------|-------|
| Circuit id | `cache-c2` |
| Version | `v1` |
| Binary | `circuits/cache-c2/v1/eni6ma` |
| Sidecar | `circuits/cache-c2/v1/eni6ma.sha256` |
| SHA256 | `14ea8f52564603d25d380ff500ad8ef28f94b91b91590073ea23436723591f1b` |
| Size (bytes) | `17796801` |
| DNA source | CIRCLE-HACK/circuit/private.json → linux/amd64 eni6ma (via api/bin/eni6ma or CIRCLE-HACK/bin/eni6ma.bin) |
| Layout | Path B — sibling `.sha256` (64 hex); no GitHub Releases for this pipeline |
| Anti-LFS | Commit raw ELF bytes; do not use Git LFS pointers |

**Raw URL:** `https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c2/v1/eni6ma`

**Pass+ try (after push to main):** `https://circuit.eni6ma.com/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c2/v1/eni6ma`

Optional local-only (`npm run dev`): `http://localhost:3000/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c2/v1/eni6ma`

API base is same-origin (empty registry → relative `/api/...`). Path B needs `BLOB_READ_WRITE_TOKEN` on the deployment.
