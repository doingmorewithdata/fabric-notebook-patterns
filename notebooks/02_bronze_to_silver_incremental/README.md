# Bronze to Silver - Incremental

This notebook demonstrates an incremental Silver pattern using a dynamically generated MERGE statement.

## Key ideas

- **Parameter Contract (Cell 1):** source/destination DB + schema + table, plus control flags like `DEBUG_MODE`.
- **Derived Namespace (Cell 2):** fully-qualified object names and key column selection are established early.
- **Metadata-driven MERGE generation:** the notebook inspects destination table metadata to build a MERGE statement on the fly, minimizing hard-coded column lists and simplifying schema evolution.

## Notes
A future enhancement is a “full rebuild” option (truncate/replace) controlled by a flag.
