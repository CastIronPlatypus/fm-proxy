<!--stratified-action
{
  "created": 1792788289,
  "edges": [
    {
      "dst": "impl-fm-proxy-test-js",
      "reason": "unit and stub-integration test layer",
      "type": "accomplished-by"
    },
    {
      "dst": "impl-tools-wire-baseline-js",
      "reason": "deterministic wire-diff layer for refactors",
      "type": "accomplished-by"
    },
    {
      "dst": "impl-tools-deviation-probe-js",
      "reason": "live-upstream deviation layer",
      "type": "accomplished-by"
    },
    {
      "dst": "impl-tools-test-plan-md",
      "reason": "documents how the layers are run and read",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "comp-verification",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "impl",
  "status": "drafting",
  "stratum": "components",
  "uid": "n0014",
  "version": 1
}
-->

Serves [[resp-behaviour-verification|serves]]. The three test layers: unit/integration tests [[impl-fm-proxy-test-js]], the deterministic wire baseline [[impl-tools-wire-baseline-js]], the live deviation probe [[impl-tools-deviation-probe-js]], and their guide [[impl-tools-test-plan-md]].
