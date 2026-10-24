<!--stratified-action
{
  "created": 1792788320,
  "edges": [
    {
      "dst": "comp-proxy-runtime",
      "reason": "fixToolSchema/fixResponseFormatSchema/findCyclicDefs live in the runtime",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "resp-schema-translation",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "unclassified",
  "retire_reason": "forward only the recursive shapes proven on 26A434, reject the rest naming the path",
  "retired_at": 1792871746,
  "status": "retired",
  "stratum": "responsibilities",
  "uid": "n0018",
  "version": 1
}
-->

Serves [[intent-forced-tool-calls|serves]], [[intent-unmodified-schemas|serves]]. Translate client JSON Schemas into the subset fm serve decodes, in [[comp-proxy-runtime]]: inline $defs/$ref, collapse type arrays and composition keywords, backfill tool descriptions, and reject cyclic $defs before any upstream connection.
