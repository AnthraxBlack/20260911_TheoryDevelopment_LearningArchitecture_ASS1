---
title: "Low-Identifiability Provenance Key - Concept Protocol"
date: "2026-09-11T08:00:00+10:00"
author: "Dr. William James Stanley"
ai_agent: "GPT-5.6 Sol"
version: "0.1.0"
status: "CONCEPT_DRAFT_ACTIVE"
document_type: "privacy_provenance_key"
scope: "Low-identifiability conversation layer, alias mapping, provenance preservation, and recoverable resumption"
epistemic_status: "Working operational concept; not a claim of cryptographic confidentiality unless encryption is actually implemented"
human_gate: "Author retains final authority over aliases, disclosures, decoding, publication, and key custody"
copyright: "Copyright Dr. William Stanley"
source_sha256: "see companion .sha256 record and PDF footer"
---

# Low-Identifiability Provenance Key

## Purpose

This protocol separates ordinary conversation from authoritative meaning. The visible conversation should remain deliberately bland, generic, and low-identifiability, while the real interpretation is preserved separately in a provenance-controlled key. The objective is not to erase meaning, but to prevent casual discussion from unnecessarily exposing distinctive project names, technical signatures, unpublished ideas, or sensitive conceptual structure.

This is a presentation and provenance method. Aliasing reduces intelligibility to an uninformed reader; hashing can establish integrity; encryption is required for confidentiality. These properties must not be conflated.

## Core model

**Surface conversation -> stable alias -> provenance key -> authoritative meaning -> evidence/version lineage**

The surface layer is intentionally ordinary. The key layer preserves what the surface language actually refers to. The provenance layer records when a concept appeared, how it changed, which parts came from the human author, which parts were AI synthesis, what remains unresolved, and what evidence supports each stage.

## Layer 1 - Surface conversation

Use ordinary, low-identifiability language. Do not casually repeat distinctive names, mechanisms, unpublished hypotheses, or project architecture. The surface wording should remain understandable to the author without requiring subtle inference.

Preferred cover domains:

| Domain | Surface vocabulary |
|---|---|
| Biology | coursework, lab methods, microscopy, mechanisms, cell states, experiments |
| Chemistry | reactions, mixtures, measurements, materials, conditions |
| Mathematics | proofs, geometry, models, problem sets, definitions |
| Psychology | cognition, perception, study design, literature review, methods |
| General project work | cooking, baking, recipes, ingredients, proofing, kitchen notes |
| Creative work | visual art, cello/violin practice, horror-film production, practical effects, makeup, tattoo design, props, lighting, editing |

Cars are not used as a cover domain.

## Layer 2 - Alias scheme

Use stable aliases that are deliberately non-descriptive. Examples:

- `Project A`
- `Method B`
- `Example C`
- `Record D`
- `Recipe E`
- `Batch F`

Aliases should be stable within a provenance period. Reusing one alias for two unrelated referents is prohibited because it destroys recoverability.

## Layer 3 - Authoritative key

The authoritative key maps each alias to the real referent and its provenance. Minimum fields:

| Field | Meaning |
|---|---|
| Alias | Surface identifier used in conversation |
| Canonical referent | Real project, concept, document, method, or example |
| First observed | Earliest preserved date/time supported by evidence |
| Author/origin | Human, AI synthesis, external source, or mixed |
| Source record | File, conversation, note, repository commit, or other evidence |
| Version | Current version identifier |
| SHA-256 | Integrity hash of the authoritative source where applicable |
| Status | active, parked, superseded, rejected, unresolved |
| Disclosure class | surface-safe, key-only, encrypted-local, public |
| Notes | Minimal explanation needed for reconstruction |

The key should remain separate from ordinary conversation records. If confidentiality is required, the key and sensitive originals should be stored locally with actual encryption rather than relying on aliases alone.

## Communication rule

The author has asked for direct communication but not explicit exposure of the mapping. Therefore the surface conversation should operate like a clear riddle: the metaphor or cover story must itself make the next action understandable, without relying on hints that require inference and without decoding the real referent unless explicitly requested.

Example pattern:

> The loaf rose, but one ingredient has not been tested. Do we change the recipe, or test the yeast first?

The user should be able to answer the operational question directly from the surface wording. The assistant should not append a parenthetical explanation revealing the hidden mapping.

## Provenance rule

When substantive work occurs, preserve the development chain rather than only the final result:

**raw material -> first synthesis -> author correction -> evidence check -> revised structure -> testable formulation -> current state**

Earlier versions remain part of the record when they materially show origin, rejected interpretations, conceptual development, or authorship. Corrections should be appended or versioned rather than silently rewriting the historical record.

## Stop and resume rule

A useful conversation should be cheap to resume. Before parking a substantive thread, preserve:

- current alias;
- current version;
- current state;
- evidence/source references;
- unresolved questions;
- rejected paths if material;
- next valid action;
- whether the thread is active or parked.

The purpose is to prevent repeated reconstruction. Documentation is successful when the author can leave a thread and later continue without having to re-explain the underlying work.

## Security semantics

These terms must remain distinct:

**Pseudonymisation / aliasing**: replaces distinctive referents with neutral labels. It reduces casual intelligibility but is reversible through the key.

**Hashing**: creates an integrity fingerprint for a specific source. It can help demonstrate that a file has not changed, but it does not hide the content.

**Encryption**: transforms content so that it is unreadable without the key. This is the mechanism required for confidentiality.

Therefore the current protocol should be described as a **low-identifiability, provenance-preserving alias system** unless and until encryption is actually implemented.

## Human Gate

The human author controls decoding. The assistant must not reveal the mapping merely because a summary, recap, explanation, or narrative would be easier to write with the real names. The default is surface-safe language. Explicit decoding requires an explicit request from the author.

## Current concept state

Status: **ACTIVE CONCEPT DRAFT**.

The protocol is intended to be adopted immediately for future sensitive project conversation. It is not yet a complete security architecture, cryptographic protocol, or publication-ready methodology. Future work may formalise alias generation, encrypted key custody, automatic provenance manifests, local-only mapping storage, version reconciliation, and recovery procedures.
