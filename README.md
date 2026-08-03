# REGISTRY

Path B circuit binaries for ENI6MA Pass+ (Vercel / WEB-6ELF).

Each circuit version is a directory containing:

- `eni6ma` — linux/amd64 ELF (raw bytes; **not** Git LFS)
- `eni6ma.sha256` — 64 hex digest of the ELF bytes (sibling sidecar)

Servers fetch `…/eni6ma` and `…/eni6ma.sha256` from raw.githubusercontent.com.

## Shared DNA note (ALICE / BOB)

`alice/v1` and `bob/v1` are **labeled Path B paths** over the **same** CIRCLE-HACK standard linux/amd64 twin. Digests are identical by design (CIRCLE-HACK shared-twin model). They are not separate DNA compiles.

## Circuits

### alice / v1

| Field | Value |
|-------|-------|
| Circuit id | `alice` |
| Version | `v1` |
| Binary | `circuits/alice/v1/eni6ma` |
| Sidecar | `circuits/alice/v1/eni6ma.sha256` |
| SHA256 | `381a338cf0fbcaa6bc9b3577db10abe544801341d49cac8c4e1a474f0d607a45` |
| Size (bytes) | `17892017` |
| DNA source | CIRCLE-HACK/circuit/private.json → linux/amd64 eni6ma (via ENI6MA-WEB-6ELF `api/bin/eni6ma`) |
| Layout | Path B — sibling `.sha256` (64 hex); no GitHub Releases for this pipeline |
| Anti-LFS | Commit raw ELF bytes; do not use Git LFS pointers |

**Raw URL:** `https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/alice/v1/eni6ma`

**Pass+ try:** `?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/alice/v1/eni6ma`

### bob / v1

| Field | Value |
|-------|-------|
| Circuit id | `bob` |
| Version | `v1` |
| Binary | `circuits/bob/v1/eni6ma` |
| Sidecar | `circuits/bob/v1/eni6ma.sha256` |
| SHA256 | `381a338cf0fbcaa6bc9b3577db10abe544801341d49cac8c4e1a474f0d607a45` |
| Size (bytes) | `17892017` |
| DNA source | CIRCLE-HACK/circuit/private.json → linux/amd64 eni6ma (via ENI6MA-WEB-6ELF `api/bin/eni6ma`) |
| Layout | Path B — sibling `.sha256` (64 hex); no GitHub Releases for this pipeline |
| Anti-LFS | Commit raw ELF bytes; do not use Git LFS pointers |

**Raw URL:** `https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/bob/v1/eni6ma`

**Pass+ try:** `?binary_url=https://raw.githubusercontent.com/eni6ma/REGISTRY/main/circuits/bob/v1/eni6ma`

## Layout

```text
circuits/
  alice/v1/eni6ma
  alice/v1/eni6ma.sha256
  bob/v1/eni6ma
  bob/v1/eni6ma.sha256
```
