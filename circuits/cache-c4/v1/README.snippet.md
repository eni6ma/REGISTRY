## Circuit provenance (paste into eni6ma/REGISTRY)

| Field | Value |
|-------|-------|
| Circuit id | `cache-c4` |
| Version | `v1` |
| Binary | `circuits/cache-c4/v1/eni6ma` |
| Sidecar | `circuits/cache-c4/v1/eni6ma.sha256` |
| SHA256 | `18c3df9c2569ee27c6918bc2da6b28978c61b3b298cf504d087366a552314bbd` |
| Size (bytes) | `17796497` |
| DNA source | CIRCLE-HACK/circuit/private.json → linux/amd64 eni6ma (via api/bin/eni6ma or CIRCLE-HACK/bin/eni6ma.bin) |
| Layout | Path B — sibling `.sha256` (64 hex); no GitHub Releases for this pipeline |
| Anti-LFS | Commit raw ELF bytes; do not use Git LFS pointers |

**Raw URL:** `https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c4/v1/eni6ma`

**Pass+ try (after push to main):** `https://circuit.eni6ma.com/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c4/v1/eni6ma`

Optional local-only (`npm run dev`): `http://localhost:3000/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c4/v1/eni6ma`

API base is same-origin (empty registry → relative `/api/...`). Path B needs `BLOB_READ_WRITE_TOKEN` on the deployment.
