# Skill Spec: thought-article-workflow

## Skill Name

`thought-article-workflow`

## Description Candidate

Use when turning a rough personal draft based on real observations, experiences, or unfinished thoughts into a clear, structured article while preserving the correct writing scene, especially sharing vs conversion.

## Why This Skill Exists

The user does not mainly need “another AI writer.”

The real gap is the layer between noisy raw thought and polished article:

- identify what the article is truly trying to say
- expose where the thought is still blurry
- mark what needs evidence, examples, or quotes
- rebuild structure before rewriting
- preserve the user's real voice while adapting to platform needs
- preserve the correct scene tone instead of flattening all writing into one style

## Primary Job

This skill should take a draft and do the following in order:

1. Diagnose before rewriting
2. Produce a problem map and a rebuilt outline
3. Clarify the most important unresolved thinking
4. Trigger research only where needed
5. Produce one mother draft
6. Adapt the mother draft for platform use
7. Respect the scene mode before optimizing for style
8. Capture stable preference updates for future iterations

## Input Contract

The ideal input includes:

- draft stage: `messy-draft` / `get-cleaned-draft` / `ai-first-draft` / `second-draft`
- target platform: `wechat` / `xiaohongshu` / `both`
- scene mode: `sharing` / `conversion` / `analysis`
- core point the user wants to express
- what the user feels is still unclear
- word count if needed

If some are missing, defaults should be:

- stage: `get-cleaned-draft`
- platform: `wechat`
- scene: `sharing`
- goal: clarify the thought without losing realness

## Output Contract

The default first response should not jump straight to a polished final article.

It should output:

1. Core claim
2. Problem map
3. Missing thinking / missing support
4. Rebuilt structure outline
5. Short list of clarifying questions or assumptions

Only after that should the skill move into writing.

## Supported Article Type

V1 serves one article family:

- viewpoint articles
- based on lived experience, observation, or practical reflection
- written to clarify the user's thinking and build trust
- may later be adapted to platform-specific sharing or conversion use

It does not yet target:

- fiction
- academic papers
- general copywriting
- pure commercial conversion writing

## Required Behaviors

### 1. Diagnose First

The skill must resist the temptation to “helpfully rewrite immediately.”

It should first identify:

- what the draft is really about
- where the structure is loose
- where emotion exists without insight
- where claims need evidence
- where examples, scenes, data, or quotes are missing

### 2. Preserve the User's Voice

The skill should not rewrite into a generic expert voice.

It should preserve:

- a companion-like tone
- practical reflection
- scene-based explanation
- real uncertainty where appropriate

### 3. Respect Scene Mode

The skill must distinguish between at least two different Xiaohongshu scenes:

#### Scene A: `sharing`

This is for genuine experience-sharing posts.

It should preserve:

- lived texture
- personal backstory where useful
- conversational tone
- human warmth
- concrete details and side comments

It should avoid:

- over-optimizing for hooks
- sounding like a conversion funnel
- cutting away too much personality in the name of efficiency
- stuffing the post with CTA or lead-magnet logic

#### Scene B: `conversion`

This is for posts where traffic, inquiry, or conversion is part of the goal.

It may use:

- stronger hooks
- tighter compression
- more obvious benefit framing
- clearer CTA placement

But it must still avoid fake authority or manipulative tone.

### 4. Separate Mother Draft From Platform Rewrite

When asked for multiple platforms, the skill should not write separate articles from scratch first.

It should:

1. build one mother draft
2. then adapt it

### 5. Use Quote Support Selectively

When a section needs book-based support, the skill should invoke `book-quote-skill` rather than inventing authority.

### 6. Update Preference Memory

If the user repeatedly corrects the same things, the skill should note them as stable preferences for future runs.

## Related Modules

This main skill should cooperate with:

- `book-quote-skill`
- `style-profile-memory.md`
- a future `benchmark-article-analysis` module

## Benchmark Samples Already Identified

### Self sample to protect

`AI发展速度这么快，普通人的机会在哪儿？`

This is important because it reflects a version of the user's writing they can already control.

### External benchmark samples to study

- `此刻我在想什么`
- `Untitled-1`

These are not for imitation at the sentence level.
They are for learning:

- structural lift
- concept building
- mechanism-level reasoning

## What This Skill Should Avoid

- becoming a generic “article beautifier”
- over-theorizing before clarifying the actual point
- imitating admired articles too directly
- flattening the user's personality into polished emptiness
- skipping diagnosis when the draft feels urgent
- treating sharing posts like conversion posts
- automatically inserting CTA logic into genuine sharing content

## Next Step Before Writing SKILL.md

Per `writing-skills`, this should not become a final skill yet.

We still need RED-phase evidence:

1. define pressure scenarios
2. observe likely failure modes
3. use those failures to write the final skill
