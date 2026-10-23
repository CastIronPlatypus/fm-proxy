<!--stratified-action
{
  "created": 1792788340,
  "edges": [
    {
      "dst": "resp-forced-tool-dispatch",
      "reason": "this intent is delivered through resp-forced-tool-dispatch",
      "type": "accomplished-by"
    },
    {
      "dst": "resp-schema-translation",
      "reason": "this intent is delivered through resp-schema-translation",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "intent-forced-tool-calls",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "story",
  "status": "drafting",
  "stratum": "intent",
  "uid": "n0028",
  "version": 1
}
-->

As an OpenAI-SDK client, I can force a tool call and receive real tool_calls, streaming or not, despite fm serve's broken tool parser. Delivered by [[resp-forced-tool-dispatch]] using [[resp-schema-translation]].
