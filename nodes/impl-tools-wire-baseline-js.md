<!--stratified-action
{
  "created": 1792788230,
  "edges": [],
  "impl_path": "tools/wire-baseline.js",
  "is_bead": true,
  "name": "impl-tools-wire-baseline-js",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:9736",
  "status": "drafting",
  "stratum": "implementation",
  "uid": "n0012",
  "version": 1
}
-->

Serves [[comp-verification|serves]]. Deterministic refactor guard: spawns [[impl-fm-proxy-js|flow]] against a recording stub upstream with canned JSON/SSE replies, sends a fixed set of requests (14 cases, 3 endpoints), and writes normalised JSON of exactly what was forwarded upstream and returned. Diff two runs to prove no behaviour change; pin FM_BIN=/nonexistent so the usage fallback is the heuristic. Second layer of [[impl-tools-test-plan-md]].
