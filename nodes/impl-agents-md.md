<!--stratified-action
{
  "created": 1792788228,
  "edges": [],
  "impl_path": "AGENTS.md",
  "is_bead": true,
  "name": "impl-agents-md",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:30282",
  "status": "drafting",
  "stratum": "implementation",
  "succeeds": "impl-agents-md@v2",
  "uid": "n0002",
  "version": 3
}
-->

Serves [[comp-upstream-audit|serves]]. Agent/maintainer source of truth for upstream fm serve behaviour on the 27.0 RC, the fm version fingerprint table, release history, and the per-OS-update audit recipe: regenerate [[impl-docs-fm-reference-md]] with [[impl-tools-gen-fm-docs-py|flow]] and diff (dump and per-leaf --help both captured; grep DUMP/HELP MISMATCH and test flagged flags against the binary), run the layers in [[impl-tools-test-plan-md]] including [[impl-tools-deviation-probe-js]], re-check known walls by hand (cyclic $defs last), and check the licence. Also documents what [[impl-fm-proxy-js]] corrects, expected test counts, Pi usage limits, the image token cost rule (3 + 16 prompt tokens per 168 px cell, at most 12 cells, so 19 to 195 per image regardless of content, format or file size), and structured-output dialect rules.
