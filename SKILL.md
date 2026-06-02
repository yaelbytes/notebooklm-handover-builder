---
name: notebooklm-handover-builder
description: Build a lean, transition-ready handover package from messy work materials and prepare it for NotebookLM ingestion. Use when the user is leaving a role, transferring ownership, building a knowledge hub, consolidating chats/docs/SOPs/decisions into structured handover documents, or wants fast guidance on what to upload to NotebookLM, what to exclude, and how to prioritize when time is limited.
---

# NotebookLM Handover Builder

This skill turns scattered working materials into a **minimum-effective handover** that is clear, deduplicated, operationally useful, and ready for NotebookLM.

Use it when the user needs to:
- prepare a role-exit handover
- transfer ownership of projects, processes, or knowledge
- convert chats, notes, documents, and drafts into a NotebookLM-ready knowledge hub
- separate final knowledge from work-in-progress
- create a fast, usable handover rather than perfect documentation

## Core Operating Principles

1. **Speed over exhaustiveness**
   - Optimize for the smallest set of documents that preserves continuity.
   - Avoid documenting everything. Capture only what the successor needs to operate.

2. **Usability over prettiness**
   - Produce handover artifacts that are directly useful to a new owner.
   - Every document should answer at least one of these:
     - What exists?
     - Why does it matter?
     - What is the current status?
     - How does it work?
     - What remains unresolved?

3. **Separate knowledge types**
   Always distinguish between:
   - **Core knowledge**: enduring logic, frameworks, definitions, policies
   - **Operational workflows**: how work is done in practice
   - **Work in progress**: incomplete drafts, experiments, pending decisions
   - **Decisions & assumptions**: what was decided, why, and under which constraints
   - **Reference material**: source docs that are useful but not central

4. **Deduplicate aggressively**
   - Merge repeated topics across chats and docs.
   - Prefer the latest, clearest, most actionable version.
   - Mark older or conflicting versions as superseded when needed.

5. **NotebookLM only gets clean sources**
   - Prefer polished summaries, SOPs, decision logs, glossaries, and project pages.
   - Avoid uploading noisy raw chats unless the raw conversation itself contains irreplaceable context.

## Inputs This Skill Can Work From

Typical source materials:
- chat transcripts
- meeting notes
- strategy docs
- SOPs
- frameworks
- working drafts
- code comments / technical notes
- spreadsheets summaries
- project plans
- decision notes
- hand-written status bullets

If source material is messy, incomplete, or repetitive, do not stop. Infer structure conservatively and flag uncertainty explicitly.

## Required Outputs

Create as many of these as the user needs, but default to the smallest effective set:

1. **Master Handover Index**
   - the top-level map of topics, projects, owners, and linked artifacts

2. **Project / Process Pages**
   - one page per meaningful project, workflow, or system area

3. **Decision Log**
   - major decisions, rationale, rejected alternatives, and consequences

4. **Open Issues / Next Steps**
   - unresolved items, blockers, dependencies, and owner suggestions

5. **Glossary / Taxonomy**
   - essential terms, labels, market definitions, schema terms, acronyms

6. **NotebookLM Upload Plan**
   - classify documents as:
     - `upload as-is`
     - `clean before upload`
     - `do not upload`

## Standard Workflow

Follow this sequence unless the user already has part of it done.

### Step 1: Inventory
Create a compact inventory of the material:
- major projects or workstreams
- recurring themes
- recurring files/docs
- unfinished areas
- decisions that are likely scattered across multiple sources

Do **not** summarize everything yet. First build the map.

### Step 2: Cluster
Group source material by topic, not by original chat/session.
Typical cluster types:
- frameworks / system logic
- recurring operating processes
- active projects
- reference research
- templates and reusable outputs
- pending work

### Step 3: Triage
For each cluster, assign:
- importance: critical / useful / optional
- maturity: final / stable / draft / unclear
- handover need: must transfer / nice to have / archive only

### Step 4: Extract
For each meaningful cluster, extract:
- objective
- business purpose
- what was built / decided
- current status
- how it works in practice
- critical assets / files / formulas / scripts
- dependencies
- risks / pitfalls
- open questions

### Step 5: Normalize
Rewrite extracted content into a consistent handover format using the project template in `templates/project_handover_template.md`.

### Step 6: Package for NotebookLM
Use `references/notebooklm_packaging_rules.md` to decide:
- which docs are ready
- which docs need cleanup
- which docs should remain outside NotebookLM

### Step 7: Prioritize
If time is limited, produce only:
- Master Index
- top 5–10 project/process pages
- Decision Log
- Open Issues

## Output Rules

### Master Index Rules
The Master Index must:
- list each project/process once
- include one-line purpose
- include status
- point to the relevant handover page
- surface critical dependencies and risks at top level if they threaten continuity

### Project / Process Page Rules
Each page should usually include:
1. Name
2. Why it exists / business purpose
3. Current status
4. How it works (SOP / workflow)
5. Key outputs / assets
6. Decisions & assumptions
7. Risks / pitfalls
8. Next steps
9. Relevant links or source references

### Decision Log Rules
Each entry should include:
- topic
- decision
- rationale
- date or period (if known)
- alternatives rejected (if known)
- impact on future work

### Open Issues Rules
Each issue should include:
- issue name
- why it matters
- what is blocked
- recommended next action
- owner or owner type if known

## NotebookLM-Specific Guidance

When preparing sources for NotebookLM:

### Good uploads
- concise project summaries
- clean SOPs
- decision logs
- glossaries
- architecture/framework notes
- curated research summaries
- clean tables exported to documents with context

### Upload only after cleanup
- raw chats
- duplicate docs
- partial drafts
- brainstorming notes
- mixed-language fragments without headings
- docs with missing titles or unclear scope

### Usually avoid
- redundant versions of the same summary
- scratch notes with no decision value
- documents that are mostly noise
- stale drafts superseded by later docs

NotebookLM works best when each source has:
- a clear title
- a bounded scope
- consistent terminology
- minimal duplication
- enough context to stand alone

## Fast Mode

If the user explicitly wants a fast handover, use this compressed workflow:

1. Build a 1-page Master Index
2. Identify the 5 most important projects/processes
3. Create one page for each using the standard template
4. Extract 10–20 key decisions
5. Create one Open Issues page
6. Recommend a minimal NotebookLM upload set

In fast mode, do not over-document historical detail.

## Quality Bar

A strong result is:
- fast to scan
- understandable by a successor with no prior context
- explicit about what is final vs draft
- clear about unresolved issues
- ready or almost ready for NotebookLM upload

A weak result:
- mirrors the raw chats
- mixes final guidance with speculation
- preserves duplication
- lacks ownership, status, or next steps

## Suggested User-Facing Framing

When presenting results, prefer language like:
- “minimum effective handover”
- “continuity-first”
- “NotebookLM-ready”
- “final vs draft”
- “what the next owner needs to know”

## Bundled References
Use these when needed:
- `references/handover_schema.md`
- `references/notebooklm_packaging_rules.md`
- `templates/project_handover_template.md`
- `templates/master_index_template.md`
- `templates/decision_log_template.md`
- `templates/open_issues_template.md`
