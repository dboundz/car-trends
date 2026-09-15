# Car Trends data export

Cryptographically / mathematically verifiable snapshot of the data behind
https://dboundz.github.io/car-trends/ HTML pages.

**as_of (America/New_York):** `2026-09-15`  
**schema_version:** `1.0.0`

## Files

| Path | Purpose |
|------|---------|
| `latest.json` | Consolidated snapshot: meta, per-brand KPIs + commentary pointers, auction-watch, classic backfill summary refs, and index of brand files with sha256 |
| `brands/{ferrari,mclaren,lamborghini,ford}.json` | Full daily listing rows + KPIs for that brand |
| `sources/` | Verbatim copies of source artifacts (daily CSVs, summaries, auction-watch, market-commentary, classic backfill) |
| `manifest.json` | Every packaged file: `path`, `bytes`, `sha256`, optional `row_count` |
| `../manifest.json` | Copy of this manifest at `data/manifest.json` |

## Verify integrity (not a signature)

This is **content integrity verification**, not a digital signature. Anyone can
recompute hashes and compare. Optional later: sign `manifest.json` or
`aggregate_sha256` with minisign / GPG.

### 1. Check one file

```bash
# from the Pages site root (or a checkout of dboundz/car-trends)
shasum -a 256 data/export/latest.json
# compare to the sha256 listed for that path in data/export/manifest.json
```

### 2. Check every listed path

```bash
python3 - <<'PY'
import json, hashlib
from pathlib import Path
manifest = json.loads(Path("data/export/manifest.json").read_text())
ok = True
for e in manifest["files"]:
    p = Path(e["path"])
    if not p.is_file():
        print("MISSING", e["path"]); ok = False; continue
    h = hashlib.sha256(p.read_bytes()).hexdigest()
    if h != e["sha256"]:
        print("MISMATCH", e["path"], h, e["sha256"]); ok = False
    else:
        print("OK", e["path"])
print("aggregate_sha256 expected:", manifest["aggregate_sha256"])
lines = sorted({f"{e['path']}:{e['sha256']}" for e in manifest["files"]})
material = "\n".join(lines) + ("\n" if lines else "")
got = hashlib.sha256(material.encode()).hexdigest()
print("aggregate_sha256 computed:", got)
print("AGGREGATE", "OK" if got == manifest["aggregate_sha256"] else "MISMATCH")
print("ALL OK" if ok and got == manifest["aggregate_sha256"] else "FAILED")
PY
```

### Aggregate hash definition

`aggregate_sha256` = SHA-256 of the UTF-8 bytes of sorted unique lines of the form:

```text
path:sha256
```

(one `path:sha256` per line, lines sorted, trailing newline; see `manifest.json` → `aggregate_definition`).

Current aggregate: `9b1db1569876c8cbe631d8fbbdb14468976dd57945c722f7b5bf6665d0aa5d47`

## Geography

Listing metrics on the HTML overview are **US + Canada only**. Export CSVs are
the raw daily merges (may include non-US/CA rows); see site `GEO.md` notes in
meta and brand packages.
