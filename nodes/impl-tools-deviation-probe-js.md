<!--stratified-action
{
  "created": 1792788230,
  "edges": [],
  "impl_path": "tools/deviation-probe.js",
  "is_bead": true,
  "name": "impl-tools-deviation-probe-js",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:7037",
  "status": "drafting",
  "stratum": "implementation",
  "uid": "n0010",
  "version": 1
}
-->

Serves [[comp-verification|serves]]. Live probe: sends ordinary OpenAI-client requests to a running proxy (default port 1977) backed by real fm serve, and reports HANDLED/NOT for each fm serve deviation (omitted stream, usage, $defs, description backfill, forced tool_choice check 6, CORS, etc.; 11 checks). Implementation-agnostic, so it can compare [[impl-fm-proxy-js]] to another proxy. Third layer of [[impl-tools-test-plan-md]].
