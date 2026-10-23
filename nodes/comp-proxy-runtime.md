<!--stratified-action
{
  "created": 1792788288,
  "edges": [
    {
      "dst": "impl-fm-proxy-js",
      "reason": "the proxy process is the runtime's core translator",
      "type": "accomplished-by"
    },
    {
      "dst": "impl-fm-launch-sh",
      "reason": "the launcher brings up fm serve and the proxy together",
      "type": "accomplished-by"
    }
  ],
  "is_bead": false,
  "name": "comp-proxy-runtime",
  "no_requirement": "recovered by ingest; requirements are linked later",
  "node_type": "impl",
  "status": "drafting",
  "stratum": "components",
  "uid": "n0013",
  "version": 1
}
-->

Serves [[resp-browser-access|serves]], [[resp-error-typing-and-retry|serves]], [[resp-forced-tool-dispatch|serves]], [[resp-request-normalization|serves]], [[resp-response-relay|serves]], [[resp-schema-translation|serves]], [[resp-stack-lifecycle|serves]]. The running stack: the translating proxy [[impl-fm-proxy-js]] and its launcher [[impl-fm-launch-sh]], which together put an OpenAI-compatible endpoint in front of fm serve.
