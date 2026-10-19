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
| C19 | ClusterAudienceKit | Remaining slices: temporal membership/churn/lifecycle/sensitivity/scenario comparison; price tier/affinity/sensitivity/competitive/threshold/demand/margin/bundles; revenue alerts/CAC/margins/upsell/concentration/cohort/growth; neural autoencoder/RNN | Open |
| C20 | PyReverseETL | Kafka/HDFS/Spark/dashboard not wired; Rust-side plugin registration open | Open (DuckDB/Postgres added `33514b2`) |
| C21 | PyDBTGuard | Snowflake/BigQuery/Redshift/MySQL not wired | Open (DuckDB/Postgres added `e8e7d23`) |
| C22 | PyStreamPDF | TLS added; mTLS, request-size limits, access logging, rate-limit persistence, cert rotation, checked-in OCR corpus remain | Partial (`e81c811`) |
| C23 | PyStreamMCP | Experimental adapters guarded but unimplemented | Open (documented) |
| C24 | PyStreamXL | `requires-python >=3.9` but CI tests only 3.10–3.12; no cp39 wheel/test; no wheel import smoke | Open |
| C25 | PyRoboReplay | PyPI only Linux x86_64 + macOS arm64; no Windows/Linux aarch64/macOS x86_64; no wheel import smoke | Open |
| C26 | CodeAtlas | Release config builds many wheels, PyPI 0.7.0 has only macOS arm64 + sdist; release has no wheel smoke | Open |
| C27 | pyvectorhound | No release workflow; PyPI 1.8.0 only cp312 macOS arm64 + sdist; no Linux/Windows wheels; no 3.8 CI | Open |
| C28 | PrismNote | Observed 10% CI failure rate (3/30): frontend lint errors, E2E failures, missing `grapify-ai/grapify-action` | Confirmed by run history |

---

## Recently fixed (traceability)

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
