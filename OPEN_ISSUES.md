# Portfolio Open Issues Register

**Last updated:** 2026-10-20
**Rule:** An issue is removed only after being **verified false with confidence**.
Unverified issues stay open and visible until fixed or disproven with evidence.

Legend: **C** = confirmed genuine · **U** = unverified/open (not disproven).

---

## Unverified — OPEN (keep visible)

| ID | Repo | Issue | Evidence so far | Next verification |
|---|---|---|---|---|
| U2 | PyReverseETL | Live CRM schema drift / opaque 400s | Only mock-server verification | Sandbox CRM contract tests |
| U3 | PyInferenceManager | Failover latency / token-budget miscalc | Routing works; latency/budget unmeasured | Instrument failover latency/budget |
| U5 | PyRoboSimulator | Cross-OS/version physics determinism | Same OS/version/load: byte-identical; MuJoCo 3.13 vs 3.5 differs by ~2e-14 (qpos) and 9.6e-13 (qvel) | Cross-OS runs; document tolerance |
| U6 | MudFish | DOM state desync on heavy SPAs | Not measured | Snapshot replay/diff |
| U7 | Himalayas-Browser | DOM/agent desync on dynamic pages | Not measured | Snapshot replay/diff |
| U8 | SHER-Kernel | Lock-free races / memory ordering | No Miri/Loom/stress suite | Miri/Loom + saturation stress |
| U9 | SHER-Kernel | Syscall error mapping / I/O perf | No fault injection | Fault-injection + benchmarks |
| U11 | StatGuardian | Rejected-record persistence / DLQ | No reject sink found; requirement unconfirmed | Confirm design |
| U12 | PyStreamPDF | Cross-project import claims | Guarded imports exist; docs may overclaim | Audit claims |
| U13 | PyRoboFrames | Structurally-valid-but-corrupt deep reads | Open-path fuzz exists | Deep-read mutation corpus |
| U14 | pyvectorhound | Quantization fidelity on real embeddings | Round-trip only | Recall/nDCG before/after |

---

## Confirmed genuine — OPEN

| ID | Repo | Issue | Status / evidence |
|---|---|---|---|
| C10 | SHER-Graphics | Vulkan wired behind `vulkan` feature via render-thread adapter + software fallback; per-op Draw/Dispatch, real memory allocation, draw/pipeline validation remain | Partial (`36275e7`) |
| C11 | SHER-Display | Independent per-output frame scheduler implemented; no vblank/presentation feedback, hardware mixed-refresh unvalidated | Partial (`34de7b0`) |
| C13 | PyRoboFrames | Native MP4 decode not fuzzed; `secure=True` sandbox opt-in | Open (documented) |
| C14 | PyInferenceManager | No native async/streaming (asyncio facade only) | Open (documented) |
| C15 | PyTokenCalc | Baseline output samples caller-supplied | Open (documented) |
| C16 | pyvectorhound | Quantization in-process only; no remote write-through | Open (documented) |
| C17 | PyRoboReplay | Remaining phase 16–20 ops not bridged (decision reconstruction, alternative timelines, clustering, window analysis, scenarios, rule extraction) | Open |
| C18 | PyTerrainMap | Remaining op limits: LOD/georeferencing, typed APIs, network SRTM | Open (documented) |
| C19 | ClusterAudienceKit | History/momentum/tier/affinity/CAC + composition/what-if/discount/attribution/forecast added; remaining slices: lifecycle/scenario comparison, competitive/threshold/demand/margin/bundles, neural autoencoder/RNN | Partial (`aed30cb`, `310a08b`) |
| C20 | PyReverseETL | Kafka/HDFS/Spark/dashboard not wired; Rust-side plugin registration open | Open (DuckDB/Postgres added `33514b2`) |
| C21 | PyDBTGuard | Snowflake/BigQuery/Redshift/MySQL not wired | Open (DuckDB/Postgres added `e8e7d23`) |
| C22 | PyStreamPDF | TLS/mTLS, body limits, access logging, streaming and real Tesseract OCR verified; rate-limit persistence, cert rotation, checked-in OCR corpus remain | Partial (`e81c811`, `ad04725`) |
| C23 | PyStreamMCP | Experimental adapters guarded but unimplemented | Open (documented) |
| C24 | PyStreamXL | Fixed in repo: 3.9 added to CI + wheel import smoke | Fixed (`a583150`), not yet released |
| C25 | PyRoboReplay | Fixed in repo: expanded release matrix + wheel smoke | Fixed (`7cb9dfb`), not yet released |
| C26 | CodeAtlas | Fixed in repo: manylinux/cp39 build fixes + release wheel smoke | Fixed (`d865130`), not yet released |
| C27 | pyvectorhound | Fixed in repo: release workflow with multi-platform wheels + 3.8 CI | Fixed (`ad123ae`), not yet released |
| C28 | PrismNote | Was 3/30 CI failures (lint, E2E, missing Graphify action); now lint clean + 207/207 E2E | Fixed (`775d917`), not yet released |

---

## Recently fixed (traceability)

- PyStreamXL `a583150` — 3.9 CI + wheel smoke (C24).
- PyRoboReplay `7cb9dfb` — expanded release matrix + wheel smoke (C25).
- CodeAtlas `d865130` (+`e3b7450`,`b5f0513`,`16b004f`,`7c04ade`) — release build fixes (C26).
- pyvectorhound `ad123ae` — multi-platform release workflow (C27).
- PrismNote `775d917` — CI stabilization, 207/207 E2E (C28).
- PyStreamPDF `ad04725` — mTLS, body limits, access logs, real OCR (C22).
- ClusterAudienceKit `310a08b` — history/momentum/tier/affinity/CAC (C19).

- SHER-Graphics `36275e7` — Vulkan feature wiring + fallback.
- SHER-Display `34de7b0` — per-output scheduler.
- ClusterAudienceKit `aed30cb` — composition/what-if/discount/attribution/forecast.
- PyDBTGuard `e8e7d23` / PyReverseETL `33514b2` — DuckDB + Postgres connectors.
- PyStreamPDF `e81c811` — optional TLS, streaming proxy, expanded scanned fixtures.
- PyStreamPDF `3b271b5` — remote MCP auth + scanned/table fixtures.
- PyRoboReplay `6999f7a` — phase 16–20 JSON bridge.
- PyTerrainMap `be21482` — advanced ops bridge.
- Himalayas-Browser `59a9ff3` — rate limiting/retries.
- SHER-Aurora `f62ed1d` — OS theme listener.
- PyStreamMCP `01c758a` — unsupported extras removed/guarded.
- PyAirflowTester `0353b02` — DAG metadata.
- StatGuardian `0320ca6`, PyStreamMCP `7b49d87`, PyStreamPDF `8573a70` — shared MCP base.
- pyvectorhound `2addeb4` — quantization + compare/drift.
- MudFish `ac8331c` — rate limiting/backoff.
- PyRoboSimulator `eab10d3` — seeded RNG.
- PyTokenCalc `10fb37f` — baseline CLI + p95.
- PyInferenceManager `7e5dcfb` — asyncio facade.
- PyRoboFrames `7fc18b6` — ingestion fuzz + secure option.
- ClusterAudienceKit `e6e00de`, `9ff8402` — pattern/segment APIs.
- PyWeatherEnriched `08bf654` — reverse geocoding/UHI.
- PyBlastRadius `1da136d`, `064f983` — webhook GIL + placeholders.
- PrismNote `0830938` — security workflow.
- PyStreamPDF `f75a065` — tokenizer warning.
- PyStreamXL `1b90337`, PyRoboVision `a885441`, CodeAtlas `1e8cd15` — docs/releases.

---

## Verified false with confidence — dropped

U4 (PyTokenCalc Unicode divergence): 75/75 exact matches across 5 models
(`tiktoken 0.14.0`), max absolute/relative error 0.

Also dropped earlier: PyBlastRadius auth weakness, PyTerrainMap dense-voxel
memory, blanket macOS-only wheels (superseded by per-repo C24–C27), PrismNote
Zustand/Redux defect, PyVectorHound embedding-cache disk I/O, SHER "monorepo"
framing.
