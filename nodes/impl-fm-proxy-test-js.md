<!--stratified-action
{
  "created": 1792788229,
  "edges": [],
  "impl_path": "fm-proxy.test.js",
  "is_bead": true,
  "name": "impl-fm-proxy-test-js",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:121856",
  "status": "drafting",
  "stratum": "implementation",
  "uid": "n0008",
  "version": 1
}
-->

Serves [[comp-verification|serves]]. node --test suite (~144 tests) that requires [[impl-fm-proxy-js|flow]] as a module (it exports fixTools, fixToolSchema, fixResponseFormatSchema, findCyclicDefs, classifyError, errorFrame, fmTokenCount, _isLicenseGate, stripTemplateMarkers, truncateAtStop, buildToolDispatch, dispatchToToolCalls) for unit tests, and spawns the proxy against a stub upstream for integration tests: CORS, 502 on unreachable upstream, image passthrough, description backfill, $defs inlining, cyclic-schema 400 before upstream, error classification, streaming finish/usage, dispatch. A few tests call the real fm binary and skip when it cannot answer. It is the unit layer of [[impl-tools-test-plan-md]].
