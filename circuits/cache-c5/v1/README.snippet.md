## Circuit provenance (paste into eni6ma/REGISTRY)

| Field | Value |
|-------|-------|
| Circuit id | `cache-c5` |
| Version | `v1` |
| Binary | `circuits/cache-c5/v1/eni6ma` |
| Sidecar | `circuits/cache-c5/v1/eni6ma.sha256` |
| SHA256 | `f082672d703411c75ec8fc3fb6c267fbd0e8e0f79e997c1539332ee908c70746` |
| Size (bytes) | `17796409` |
| DNA source | CIRCLE-HACK/circuit/private.json → linux/amd64 eni6ma (via api/bin/eni6ma or CIRCLE-HACK/bin/eni6ma.bin) |
| Layout | Path B — sibling `.sha256` (64 hex); no GitHub Releases for this pipeline |
| Anti-LFS | Commit raw ELF bytes; do not use Git LFS pointers |

**Raw URL:** `https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c5/v1/eni6ma`

**Pass+ try (after push to main):** `https://circuit.eni6ma.com/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c5/v1/eni6ma`

Optional local-only (`npm run dev`): `http://localhost:3000/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c5/v1/eni6ma`

API base is same-origin (empty registry → relative `/api/...`). Path B needs `BLOB_READ_WRITE_TOKEN` on the deployment.
