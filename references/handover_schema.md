# Handover Schema

Use this schema when extracting structured handover content from messy inputs.

## Core fields
- `name`
- `type` — project / process / framework / system area / reference
- `business_purpose`
- `status` — final / stable / active / draft / blocked / archived
- `priority` — critical / useful / optional
- `owner` — person, team, or unknown
- `sources` — chats, docs, notes, files

## Required extraction fields
- `what_exists_now`
- `why_it_matters`
- `how_it_works`
- `key_outputs`
- `decisions_and_assumptions`
- `risks_and_pitfalls`
- `open_questions`
- `next_steps`

## Status interpretation
- `final`: ready for use, low ambiguity
- `stable`: in use, may evolve, but successor can operate it
- `active`: currently being developed or maintained
- `draft`: incomplete, not safe to rely on fully
- `blocked`: requires external input or dependency
- `archived`: keep for reference only

## Extraction rules
1. Prefer explicit decisions over inferred ones.
2. If there are conflicting sources, use the latest clear source and note the conflict.
3. If status is uncertain, mark as `unclear` in working notes, then map to the nearest status with a note.
4. Preserve operational knowledge even if the project is incomplete.
5. Distinguish between:
   - what was discussed
   - what was decided
   - what was implemented
