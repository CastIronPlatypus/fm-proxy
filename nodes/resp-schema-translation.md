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
  "status": "drafting",
  "stratum": "responsibilities",
  "succeeds": "resp-schema-translation@v1",
  "uid": "n0018",
  "version": 2
}
-->

Serves [[intent-forced-tool-calls|serves]], [[intent-unmodified-schemas|serves]]. Translate client JSON Schemas into the subset fm serve decodes, in [[comp-proxy-runtime]]: inline $defs/$ref, collapse type arrays and composition keywords, backfill tool descriptions, and handle recursive $defs. A recursive response_format schema keeps its $defs, gains the fm dialect and is forwarded only in the shapes proven on 27.0.1: each recursive $ref sits on a property of a $defs entry as a plain $ref, array items without minItems, or anyOf [$ref, null], and every cycle passes through an optional property or such an array. Any other recursion is rejected before any upstream connection with a 400 cyclic_schema naming the recursion path and the fix.
