<!--stratified-action
{
  "created": 1792788341,
  "edges": [
    {
      "dst": "resp-error-typing-and-retry",
      "reason": "this intent is delivered through resp-error-typing-and-retry",
      "type": "accomplished-by"
    },
    {
      "dst": "resp-response-relay",
      "reason": "this intent is delivered through resp-response-relay",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "intent-typed-errors",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "story",
  "status": "drafting",
  "stratum": "intent",
  "uid": "n0030",
  "version": 1
}
-->

As an OpenAI-SDK client, I receive typed OpenAI errors and content_filter finishes, with transient failures retried invisibly, so I can branch on cause. Delivered by [[resp-error-typing-and-retry]] and [[resp-response-relay]].
