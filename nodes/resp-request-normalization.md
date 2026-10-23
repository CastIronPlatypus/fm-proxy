<!--stratified-action
{
  "created": 1792788320,
  "edges": [
    {
      "dst": "comp-proxy-runtime",
      "reason": "fixTools/prepareUpstreamRequest in the runtime do the field rewrites",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "resp-request-normalization",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "unclassified",
  "status": "drafting",
  "stratum": "responsibilities",
  "uid": "n0017",
  "version": 1
}
-->

Serves [[intent-chat-completion|serves]]. Normalise standard OpenAI request fields that fm serve rejects or ignores, in [[comp-proxy-runtime]]: developer role to system, withhold stop and reasoning_effort, map max_tokens to max_completion_tokens, pin stream:false when omitted, force include_usage upstream.
