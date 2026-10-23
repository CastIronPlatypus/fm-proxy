<!--stratified-action
{
  "created": 1792788322,
  "edges": [
    {
      "dst": "comp-proxy-runtime",
      "reason": "setCors and header scrubbing live in the runtime",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "resp-browser-access",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "unclassified",
  "status": "drafting",
  "stratum": "responsibilities",
  "uid": "n0022",
  "version": 1
}
-->

Serves [[intent-browser-clients|serves]]. Let browser clients reach the endpoint, in [[comp-proxy-runtime]]: answer CORS preflight, add CORS headers, and strip Origin/Referer/Sec-Fetch-* so fm serve does not 403.
