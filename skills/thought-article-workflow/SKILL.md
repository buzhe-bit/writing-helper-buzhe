---
name: thought-article-workflow
description: Use when working with personal Chinese drafts for viewpoint articles, Xiaohongshu or WeChat posts, experience notes, benchmark article analysis, or rough thoughts where scene tone, structure, evidence, and author voice matter.
---

# Thought Article Workflow

## Overview

This skill helps turn rough personal thinking into clear Chinese articles without flattening the author's real voice. Core principle: diagnose the thinking and scene before rewriting the text.

## When to Use

Use this for:

- Rough drafts from notes, voice dumps, Get-cleaned drafts, AI first drafts, or second drafts
- WeChat viewpoint articles and Xiaohongshu experience/conversion posts
- Benchmark article analysis or self-sample review
- Drafts that need stronger support from data, cases, book quotes, or original source passages

## First Decision: Scene Mode

Before writing, identify the scene:

| Scene | Use When | Priority |
| --- | --- | --- |
| `sharing` | Experience posts, study notes, lessons learned, sincere Xiaohongshu sharing |真人感 -> 真实细节 -> 方法感 -> 传播效率 |
| `conversion` | Consultation, lead capture, product/service promotion, traffic conversion |痛点 -> 利益点 -> 行动引导 -> 承接动作 |
| `analysis` | Diagnose, review, benchmark analysis, style extraction |判断清楚 -> 区分可学/不可学 -> 给训练动作 |

Important: Xiaohongshu is not one scene. A sharing post must not be written like a conversion funnel.

## Default Flow

Do not jump straight into a polished article unless the user explicitly asks for direct rewriting.

1. Identify draft stage: messy draft, Get-cleaned draft, AI first draft, or second draft.
2. Identify platform and scene: WeChat, Xiaohongshu sharing, Xiaohongshu conversion, or analysis.
3. Diagnose first: core claim, strongest seeds, unclear thinking, missing support, structural drift.
4. Rebuild outline before full rewriting when the draft is unstable.
5. Decide support type: personal detail, public data/case, book quote, or original source passage.
6. Clarify only high-impact gaps; prefer safe assumptions over excessive questioning.
7. Write one mother draft before multi-platform adaptation.
8. Capture repeated corrections as style-memory candidates.

## Diagnosis Checklist

For every draft, look for:

- Core question: What is this really trying to answer?
- Core claim: What should the reader remember?
- Strong seeds: concepts, examples, metaphors, lived details
- Weak links: unsupported claims, emotion without insight, examples without conclusion
- Structure issue: repetition, loose order, multiple main topics
- Support needed: data, cases, book quotes, personal examples, or clearer reasoning

If book quotes or original passages are needed, use `quote-support-guide.md` and `book-quote-skill` instead of inventing authority.

## Platform Rules

### WeChat

Preserve complete reasoning, background, and conceptual buildup. Build a strong mother draft before polishing; do not over-compress into Xiaohongshu rhythm.

### Xiaohongshu Sharing

Use for genuine experience sharing.

- Start with a real person and situation, not just a hook
- Keep useful details, scores, tools, teachers, platforms, and lived texture when they support trust
- Allow conversational phrases, light side comments, and soft emotional endings
- Keep CTA light, late, or absent
- Do not sacrifice sincerity for "爆款感"

### Xiaohongshu Conversion

Use only when the user wants traffic, inquiry, resource pickup, or commercial conversion. Stronger hooks, benefit framing, and CTA are allowed, but keep the user's voice and avoid agency-template tone.

## Benchmark Article Analysis

When the user provides an admired article, do not imitate it directly.

Output:

1. Why the article works
2. What is worth learning
3. What should not be copied
4. How to translate the technique into the user's voice
5. One or two practice actions for the next draft

For the full guide, read `benchmark-analysis-guide.md`.

## Quote And Evidence Support

When a draft has a claim that feels true but unsupported, decide what kind of support it needs:

- Personal detail: use the author's own experience
- Public data/case: search current facts and cite source
- Book quote/original passage: use `book-quote-skill`
- Clearer reasoning: rewrite the logic instead of adding decoration

For full rules, read `quote-support-guide.md`.

## Style Memory

Use `style-profile-memory.md` when writing in the user's voice, especially for Xiaohongshu. Current stable rule: sharing posts preserve realness, personal texture, concrete details, and human warmth; conversion rules must not leak into sharing posts.

When the user says "this is not me" or repeats the same correction, record it as a future style-memory candidate rather than treating it as a one-time edit.

## Common Mistakes

- Rewriting too early -> diagnose the draft and scene first
- Treating Xiaohongshu as one style -> choose sharing or conversion before optimizing
- Over-compressing sharing posts -> preserve lived details and human texture
- Copying benchmark articles -> learn structure and technique, not surface voice
- Adding CTA by default -> add CTA only in conversion scenes or when requested

## Supporting Files

- `style-profile-memory.md`: confirmed user style and scene preferences
- `benchmark-analysis-guide.md`: how to analyze admired and self-written articles
- `quote-support-guide.md`: how to decide when and how to use quotes/source passages
- `case-study-ai-opportunity.md`: example of moving from raw idea to structured article
- `red-test-pack-ai-opportunity.md`: test pack for failure modes
- `red-phase-runbook.md`: verification method for future revisions
