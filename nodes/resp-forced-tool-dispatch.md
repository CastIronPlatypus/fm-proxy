<!--stratified-action
{
  "created": 1792788320,
  "edges": [
    {
      "dst": "comp-proxy-runtime",
      "reason": "buildToolDispatch/dispatchToToolCalls/emitSynthesisedStream live in the runtime",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "resp-forced-tool-dispatch",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "unclassified",
  "status": "drafting",
  "stratum": "responsibilities",
  "uid": "n0019",
  "version": 1
}
-->

Serves [[intent-forced-tool-calls|serves]]. Turn a forced tool_choice into a response_format dispatch schema and the schema-constrained reply back into OpenAI tool_calls, streaming via a synthesised SSE, in [[comp-proxy-runtime]]. Auto is deliberately untranslated.
