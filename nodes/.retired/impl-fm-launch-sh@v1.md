<!--stratified-action
{
  "created": 1792788229,
  "edges": [],
  "impl_path": "fm-launch.sh",
  "is_bead": true,
  "name": "impl-fm-launch-sh",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:6351",
  "retire_reason": "launcher never exported its ports to the proxy, and its cleanup pkill-ed any fm serve on the port, including one it did not start",
  "retired_at": 1792796852,
  "status": "retired",
  "stratum": "implementation",
  "uid": "n0006",
  "version": 1
}
-->

Serves [[comp-proxy-runtime|serves]]. Bash launcher. Parses --fm-port/--proxy-port/--fm-bin/--health-timeout (env FM_PORT, PROXY_PORT, FM_BIN, HEALTH_TIMEOUT_MS), starts [[impl-fm-proxy-js|flow]] as a tagged background child, waits for fm serve health, then runs FM_BIN serve in the foreground; INT/TERM/HUP/EXIT traps tear the proxy down so it cannot orphan. Prints the OpenAI base URL once the stack is up. Documented in [[impl-readme-md]].
