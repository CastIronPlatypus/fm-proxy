<!--stratified-action
{
  "created": 1792788339,
  "edges": [
    {
      "dst": "resp-request-normalization",
      "reason": "this intent is delivered through resp-request-normalization",
      "type": "accomplished-by"
    },
    {
      "dst": "resp-response-relay",
      "reason": "this intent is delivered through resp-response-relay",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "intent-chat-completion",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "story",
  "status": "drafting",
  "stratum": "intent",
  "uid": "n0027",
  "version": 1
}
-->

As an OpenAI-SDK client, I can get a chat completion from the on-device model, as one JSON object or as an SSE stream ending in one finish_reason, with real token usage, without code changes. Delivered by [[resp-request-normalization]] and [[resp-response-relay]].
