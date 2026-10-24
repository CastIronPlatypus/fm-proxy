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
  "succeeds": "intent-unmodified-schemas@v2",
  "uid": "n0029",
  "version": 3
}
-->

As an OpenAI-SDK client, I can send generator-emitted structured-output and tool schemas unmodified and get constrained output instead of a 400. That includes the recursive schemas pydantic and zod emit for trees, linked lists and comment threads. A recursive shape fm serve has not been shown to handle, including a cycle with no optional or array escape, is rejected with a 400 that names the recursion path and how to fix it, so it never hangs the server. Delivered by [[resp-schema-translation]].
