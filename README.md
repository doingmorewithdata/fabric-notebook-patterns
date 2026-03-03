# Fabric Notebook Engineering Patterns

Practical patterns and templates for building **production-ready Microsoft Fabric notebooks** with an engineering-first mindset.

## The core structure

- **Cell 1: Parameters as a contract**  
  Centralize inputs and control flags (debug vs execute, schema mapping, incremental vs rebuild, etc.).

- **Cell 2: Derived namespace**  
  Compute *every derivable variable up front* (paths, fully-qualified object names, schema file locations, output names).  
  After this cell, the notebook becomes “pure work” — fewer surprises, lower cognitive load, safer reruns.

- **Everything after: Work**  
  Read → transform → write, without sprinkling configuration across the notebook.

## Included notebooks

### 1) Load Files to Bronze Tables
Bronze ingestion template driven by the parameter contract + derived namespace pattern.

### 2) Bronze to Silver - Incremental
Silver accumulation template that supports debug vs execute behavior and generates a **metadata-driven MERGE statement** by inspecting the destination table schema.

## Status
Work in progress. The patterns here will evolve as I continue refining notebook structure, parameterization, and operational safety.
