# Oraicle hosting test sites

Three tiny static sites that Oraicle publishes on its own hosting, one folder each. An hourly check visits them from the outside: sites A and B must serve their own marker file and never each other's, and site S is kept suspended and must stay unreachable. If the check fails, Oraicle stops accepting new sites until it passes again.

Do not rename the folders or the marker files, and do not change what the marker files contain: the check compares them byte for byte.

| Folder | Site | Marker file | Kept |
|---|---|---|---|
| `a/` | `oraicle-canary-a.oraicle.app` | `/canary-a.txt` | served |
| `b/` | `oraicle-canary-b.oraicle.app` | `/canary-b.txt` | served |
| `s/` | `oraicle-canary-s.oraicle.app` | `/canary-s.txt` | suspended |
