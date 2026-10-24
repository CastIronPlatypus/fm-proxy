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
  "status": "drafting",
  "stratum": "implementation",
  "succeeds": "impl-fm-launch-sh@v1",
  "uid": "n0006",
  "version": 2
}
-->

Serves [[comp-proxy-runtime|serves]]. Bash launcher. Parses --fm-port/--proxy-port/--fm-bin/--health-timeout (env FM_PORT, PROXY_PORT, FM_BIN, HEALTH_TIMEOUT_MS) and exports the ports and binary so [[impl-fm-proxy-js|flow]] uses them. Before starting anything it checks both ports: a healthy fm serve already on the fm port is reused and left running, and anything else on either port is a startup error. Otherwise it starts the proxy as a tagged background child, then fm serve by PID, and waits on it. INT/TERM/HUP/EXIT traps stop the proxy and only the fm serve this script started, never one it found running. Prints the OpenAI base URL once the stack is up. Documented in [[impl-readme-md]].
