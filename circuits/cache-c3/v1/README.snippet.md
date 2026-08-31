## Circuit provenance (paste into eni6ma/REGISTRY)

| Field | Value |
|-------|-------|
| Circuit id | `cache-c3` |
| Version | `v1` |
| Binary | `circuits/cache-c3/v1/eni6ma` |
| Sidecar | `circuits/cache-c3/v1/eni6ma.sha256` |
| SHA256 | `99d589181420fc74641f0d8337f3a794478f0967661eef106fb1336db5d37ea0` |
| Size (bytes) | `17796681` |
| DNA source | CIRCLE-HACK/circuit/private.json → linux/amd64 eni6ma (via api/bin/eni6ma or CIRCLE-HACK/bin/eni6ma.bin) |
| Layout | Path B — sibling `.sha256` (64 hex); no GitHub Releases for this pipeline |
| Anti-LFS | Commit raw ELF bytes; do not use Git LFS pointers |

**Raw URL:** `https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c3/v1/eni6ma`

**Pass+ try (after push to main):** `https://circuit.eni6ma.com/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c3/v1/eni6ma`

Optional local-only (`npm run dev`): `http://localhost:3000/passplus/?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/cache-c3/v1/eni6ma`

API base is same-origin (empty registry → relative `/api/...`). Path B needs `BLOB_READ_WRITE_TOKEN` on the deployment.
