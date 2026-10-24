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
  "succeeds": "impl-tools-gen-fm-docs-py@v1",
  "uid": "n0011",
  "version": 2
}
-->

Serves [[comp-upstream-audit|serves]]. Python script: runs fm --experimental-dump-help once for the ArgumentParser JSON tree, then runs each leaf command's own --help and strips ANSI colour. It compares the flags each source names (hidden dump args excluded, --[no-]x expanded) and writes [[impl-docs-fm-reference-md|flow]] (or --outdir) as option tables plus each leaf's --help text, with a DUMP/HELP MISMATCH note wherever the sources disagree. Never picks one silently; deterministic output. Step 1 of the audit in [[impl-agents-md]].
