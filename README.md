# NotebookLM Handover Builder

A Claude skill for turning messy working materials into a lean, transition-ready handover package designed for NotebookLM ingestion.

## What it does

This skill helps transform raw materials such as:

* chat logs
* notes
* drafts
* SOPs
* framework documents
* decision records
* work-in-progress materials

into a structured handover package that includes:

* Master Index
* Project Handover Pages
* Decision Log
* Open Issues / Next Steps
* NotebookLM upload recommendations

## Purpose

The goal is not exhaustive documentation.
The goal is a **minimum effective handover** that is:

* fast to produce
* easy to maintain
* useful for the next owner
* clean enough for NotebookLM

## Core capabilities

* Extract projects, workflows, outputs, decisions, assumptions, and open issues
* Distinguish between core knowledge, operational workflows, work in progress, and reference material
* Reduce duplication across messy source materials
* Package knowledge into handover-friendly artifacts
* Recommend what should and should not be uploaded to NotebookLM

## Structure

* `SKILL.md` — main skill instructions
* `agents/openai.yaml` — agent metadata
* `references/` — handover schema and NotebookLM packaging rules
* `templates/` — reusable handover document templates

## Best use case

This skill is designed for:

* role transitions
* internal knowledge transfer
* startup teams with limited documentation time
* creating clean NotebookLM-ready knowledge hubs
