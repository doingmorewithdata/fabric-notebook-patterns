# Load Files to Bronze Tables

This notebook demonstrates a repeatable Bronze ingestion pattern centered on:

## 1) Parameter Contract (Cell 1)

All inputs and control flags are defined up front so the notebook can run:
- interactively (safe debugging)
- or via orchestration (pipeline-controlled)

## 2) Derived Namespace (Cell 2)

All derivable variables (file paths, schema file path, output table name, etc.) are computed immediately.

After the first two cells, the remaining logic becomes straightforward data work:
read → transform → write.
