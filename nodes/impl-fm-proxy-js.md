<!--stratified-action
{
  "created": 1792788229,
  "edges": [],
  "impl_path": "fm-proxy.js",
  "is_bead": true,
  "name": "impl-fm-proxy-js",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:67857",
  "status": "drafting",
  "stratum": "implementation",
  "succeeds": "impl-fm-proxy-js@v1",
  "uid": "n0007",
  "version": 2
}
-->

Serves [[comp-proxy-runtime|serves]]. The whole proxy, one Node stdlib file. Listens on PROXY_PORT (1977) and forwards to fm serve on FM_PORT (1976), which [[impl-fm-launch-sh|flow]] starts. fixTools rewrites each request: developer->system role, withholds stop and reasoning_effort, translates a forced tool_choice into a response_format dispatch schema (buildToolDispatch / dispatchToToolCalls), simplifies tool parameter schemas (fixToolSchema, inlineDefs, collapseTypeArray), backfills missing function.description, and inlines response_format $defs (fixResponseFormatSchema), keeping $defs with the fm dialect for a recursive schema. findUnescapableCycle then forwards recursion only in the shapes proven on 27.0.1 (a $ref, array items without minItems, or anyOf [$ref, null] on a $defs property, with every cycle escaping through an optional property or such an array) and answers anything else with 400 cyclic_schema naming the recursion path and the fix. prepareUpstreamRequest maps max_tokens to max_completion_tokens, pins stream:false when omitted, forces stream_options.include_usage, and strips Origin/Referer/Sec-Fetch-*. classifyError types upstream failures; createRetryPlan/createAttemptGate retry transient ones pre-commit with capped exponential backoff. relayStreamingChat and relayNonStreamingChat apply stop truncation, optional template-marker stripping, length finish rewrite, guardrail -> content_filter, and real-or-fallback usage (fmTokenCount shells out to FM_BIN count-tokens, latching the licence gate). emitSynthesisedStream turns a buffered dispatch reply into SSE. Non-chat paths (GET /v1/models, /health) pipe through with CORS headers. Exercised by [[impl-fm-proxy-test-js]], [[impl-tools-wire-baseline-js]] and [[impl-tools-deviation-probe-js]].
