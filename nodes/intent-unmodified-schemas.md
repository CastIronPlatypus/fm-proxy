<!--stratified-action
{
  "created": 1792788340,
  "edges": [
    {
      "dst": "resp-schema-translation",
      "reason": "this intent is delivered through resp-schema-translation",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "intent-unmodified-schemas",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "story",
  "status": "drafting",
  "stratum": "intent",
  "uid": "n0029",
  "version": 1
}
-->

As an OpenAI-SDK client, I can send generator-emitted structured-output and tool schemas unmodified and get constrained output instead of a 400, and the server is protected from a cyclic $defs that would hang it. Delivered by [[resp-schema-translation]].
