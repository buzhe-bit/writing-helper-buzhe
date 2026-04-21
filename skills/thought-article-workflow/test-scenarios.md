# RED Phase Test Scenarios for thought-article-workflow

These scenarios exist to test whether the future skill actually enforces the right behavior.

The main question is:

**Without the skill, what does the agent do wrong when helping with a personal viewpoint article draft?**

## Expected Failure Pattern

Without a dedicated skill, the agent will likely:

- rewrite too early
- act helpful but skip diagnosis
- smooth language without fixing thinking
- imitate admired writing too literally
- mix platform rewriting with structural rebuilding
- fail to mark where support is missing

## Scenario 1: The Agent Rushes Into Rewriting

### Prompt

I pasted my Get-cleaned draft below. Please help me rewrite it into a polished article for my public account.

[draft omitted]

### What We Expect to See Without the Skill

- immediate rewrite
- no clear problem map
- no statement of the core claim
- no separation between “unclear thought” and “bad wording”

### Why This Scenario Matters

This is the most likely failure mode in real use.

## Scenario 2: The Agent Confuses Emotion With Insight

### Prompt

This draft is based on a strong feeling I had after an experience. Please make it deeper and more powerful.

[draft omitted]

### What We Expect to See Without the Skill

- amplifies tone
- adds grand language
- does not identify what the actual insight is
- creates fake depth instead of clarifying the point

### Why This Scenario Matters

The user's writing often starts from experience and feeling. The skill must turn feeling into thought, not decorate it.

## Scenario 3: The Agent Overfits to Benchmark Articles

### Prompt

I like these two articles very much. Please write mine in this style.

[benchmark article references omitted]

### What We Expect to See Without the Skill

- copies rhythm and sentence surface
- loses the user's real voice
- adopts a maturity level or authority tone the draft has not earned

### Why This Scenario Matters

The user wants to learn from admired articles, not become a clone of them.

## Scenario 4: The Agent Skips Missing-Support Detection

### Prompt

Please turn this draft into a convincing article.

[draft omitted]

### What We Expect to See Without the Skill

- keeps unsupported claims
- does not flag where data, examples, or book quotes are needed
- sounds fluent but remains weak

### Why This Scenario Matters

This skill must know when to stop writing and start researching.

## Scenario 5: The Agent Mishandles Dual-Platform Requests

### Prompt

Please make this into both a WeChat article and a Xiaohongshu post.

[draft omitted]

### What We Expect to See Without the Skill

- jumps straight to two versions
- no mother draft
- no explanation of what changes across platforms
- duplicated effort and inconsistent core message

### Why This Scenario Matters

The user wants both platforms, but the skill should still preserve one core argument.

## Scenario 6: The Agent Fails to Accumulate Preference Memory

### Prompt

I changed the same things again: stop making me sound like a teacher, and don't abstract too early.

### What We Expect to See Without the Skill

- treats this as a one-time edit note
- does not recognize repeated feedback as a stable preference
- makes the same mistake next round

### Why This Scenario Matters

This workflow is meant to get better over time, not restart from zero each run.

## What We Need to Capture During Testing

When these scenarios are run later, capture:

- what the agent did first
- whether it diagnosed before writing
- what rationalization it used for skipping diagnosis
- whether it preserved the user's voice
- whether it identified missing support
- whether it separated mother draft from platform rewrite

## Success Criteria for the Final Skill

The final skill passes when, under these scenarios, the agent reliably:

- diagnoses first
- names the core claim clearly
- marks unclear thinking separately from weak wording
- flags missing support
- avoids imitation drift
- writes one mother draft before platform adaptation
- records repeated preferences as stable memory
