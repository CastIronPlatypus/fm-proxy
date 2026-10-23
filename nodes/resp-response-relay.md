<!--stratified-action
{
  "created": 1792788321,
  "edges": [
    {
      "dst": "comp-proxy-runtime",
      "reason": "relayStreamingChat/relayNonStreamingChat live in the runtime",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "resp-response-relay",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "unclassified",
  "status": "drafting",
  "stratum": "responsibilities",
  "uid": "n0021",
  "version": 1
}
-->

Serves [[intent-chat-completion|serves]], [[intent-clean-content-optin|serves]], [[intent-typed-errors|serves]]. Relay replies in OpenAI shape on both paths, in [[comp-proxy-runtime]]: one finish_reason (length rewrite, content_filter on guardrail), stop truncation with hold-back, optional template-marker stripping, real usage with a count-tokens fallback.
