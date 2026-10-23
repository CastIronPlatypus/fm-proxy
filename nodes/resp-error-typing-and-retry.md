<!--stratified-action
{
  "created": 1792788321,
  "edges": [
    {
      "dst": "comp-proxy-runtime",
      "reason": "classifyError, createRetryPlan and createAttemptGate live in the runtime",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "resp-error-typing-and-retry",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "unclassified",
  "status": "drafting",
  "stratum": "responsibilities",
  "uid": "n0020",
  "version": 1
}
-->

Serves [[intent-typed-errors|serves]]. Classify fm serve failures into OpenAI error types and retry only the transient ones before the client head is committed, in [[comp-proxy-runtime]].
