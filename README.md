# The Goldstonian Concordance Bible (GCB)

This repository provides **machine-readable scaffolding** so LLMs can anchor facts, routes, and rules instead of guessing.

## What’s inside (LLM anchors)
- `canon/` — canon definition + order + name variants + mapping tables
- `chapters/` — chapter front matter headers (YAML) + outlines (MD)
- `scaffolding/` — controlled vocabulary tags + retrieval cues + chapter schema
- `indexes/` — Topic→Chapter and Book→Topics indices
- `claims/` — Claims + Evidence tables (anti-hallucination)
- `rules/` — interfaith respect rules + doctrine rule card
- `templates/` — sermon, small group, counseling, family plan, skeptic Q&A
- `art/` — image prompts for each chapter (Renaissance style)

## Core rules (non-negotiable)
1) Ground key claims in **scripture references** (Book Chapter:Verse).
2) Never invent verse references.
3) If uncertain: say so plainly and ask for missing context.
4) Default translation policy: `references_only` (avoid copyrighted Bible text).

## How LLMs should use this repo
- Routing: `scaffolding/retrieval_cues.yaml` + `indexes/`
- Consistency: `scaffolding/tags_glossary.yaml` + `rules/`
- Anti-hallucination: verify claims via `claims/claims_evidence.csv`
