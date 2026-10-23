<!--stratified-action
{
  "created": 1792788322,
  "edges": [
    {
      "dst": "comp-proxy-runtime",
      "reason": "fm-launch.sh and the env config are part of the runtime",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "resp-stack-lifecycle",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "unclassified",
  "status": "drafting",
  "stratum": "responsibilities",
  "uid": "n0023",
  "version": 1
}
-->

Serves [[intent-run-the-stack|serves]]. Start, configure and cleanly stop fm serve and the proxy together, in [[comp-proxy-runtime]], with env-driven ports, binary and retry budget.
