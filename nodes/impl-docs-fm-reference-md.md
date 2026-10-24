<!--stratified-action
{
  "created": 1792788229,
  "edges": [],
  "impl_path": "docs/fm-reference.md",
  "is_bead": true,
  "name": "impl-docs-fm-reference-md",
  "node_type": "impl",
  "origin": "ingest",
  "realized_at": "0.15.0",
  "realized_fp": "1792787917:7746",
  "status": "drafting",
  "stratum": "implementation",
  "succeeds": "impl-docs-fm-reference-md@v1",
  "uid": "n0005",
  "version": 2
}
-->

Serves [[comp-upstream-audit|serves]]. Generated, committed per build: the full fm command tree as per-command option tables, written by [[impl-tools-gen-fm-docs-py]] from fm --experimental-dump-help, plus each leaf command's ANSI-stripped --help text and a greppable DUMP/HELP MISMATCH note where the two disagree (27.0.1: --nested in the dump, --object in --help). Never hand-edited; it is the 'before' side of the structure diff in the audit recipe in [[impl-agents-md]].
