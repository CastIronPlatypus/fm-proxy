<!--stratified-action
{
  "created": 1792788230,
  "edges": [],
  "impl_path": "tools/gen-fm-docs.py",
  "is_bead": true,
  "name": "impl-tools-gen-fm-docs-py",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:2793",
  "status": "drafting",
  "stratum": "implementation",
  "uid": "n0011",
  "version": 1
}
-->

Serves [[comp-upstream-audit|serves]]. Python script: runs FM_BIN --experimental-dump-help once, parses the ArgumentParser JSON tree, and writes [[impl-docs-fm-reference-md|flow]] (or --outdir) as markdown option tables. Step 1 of the audit in [[impl-agents-md]].
