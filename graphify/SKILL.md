---
name: graphify
description: "Inspects and generates codebase architecture graphs using Graphify before making changes to any project."
---

# Graphify Codebase Inspector & Knowledge Graph

This skill ensures that before analyzing or making changes to any project, the codebase structure and relationship map are inspected through Graphify.

## Core Rules

1. **Mandatory Pre-Flight Check:**
   Before executing modifications or architectural changes in a repository, verify if a Graphify knowledge graph (`graphify-out/` or `GRAPH_REPORT.md` or `graph.json`) exists.

2. **Generate if Missing:**
   If the project does not have Graphify initialized:
   - Run `/graphify .` or generate the graph using `graphifyy` CLI / AST analysis.
   - Inspect `graphify-out/GRAPH_REPORT.md` and `graphify-out/graph.json` to understand the modules, dependencies, and entrypoints.

3. **Read Before Writing:**
   Read the graph report first to understand how components interact, preventing side-effects or architectural breaks.
