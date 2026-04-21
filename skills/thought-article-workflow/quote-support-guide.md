# Quote Support Guide

This guide integrates `book-quote-skill` into `thought-article-workflow`.

## Core Principle

Do not add quotes just to make an article look deeper.

Use quotes only when they do one of these jobs:

- Clarify a difficult idea
- Give authority to a claim that needs support
- Add a memorable formulation the draft cannot produce by itself
- Connect the user's personal insight to a larger intellectual tradition

## When To Use Book Quotes

Use `book-quote-skill` when the draft has:

- A strong claim but weak support
- A concept that would benefit from a thinker, scholar, or classic book
- A section where the user explicitly asks for original passages
- A WeChat article that needs more intellectual weight

Avoid book quotes when:

- The post is a Xiaohongshu sharing scene and the quote would break the real-person texture
- The paragraph only needs a concrete personal example
- The quote is being used as decoration
- The source cannot be verified

## Quote Selection Rules

Prefer quotes that are:

- Close to the user's actual point
- Short enough to keep reading smooth
- Clear to non-specialist readers
- More action- or image-based than abstract
- Easy to embed into the user's own reasoning

Avoid:

- Long academic passages
- Vague inspirational quotes
- Quotes that sound impressive but do not support the paragraph
- Unverified or unattributed internet quote cards

## Workflow

1. Identify the claim that needs support.
2. Decide whether it needs personal detail, data/case, book quote, or clearer reasoning.
3. If it needs a book quote, pass three inputs to `book-quote-skill`:
   - current article or paragraph
   - target book/author if known
   - the exact point the quote should support
4. Ask for 2-3 candidate passages with recommendation levels and reasons.
5. Choose one quote and embed it into the article.
6. After embedding, check that the paragraph still sounds like the user.

## Output Shape Inside The Main Workflow

When diagnosing a draft, mark quote needs like this:

```markdown
需要引用补强：
- 位置：
- 当前判断：
- 为什么需要引用：
- 建议寻找的作者/书：
- 如果找不到，替代方案：
```

When embedding a chosen quote:

- Introduce why the quote appears
- Quote briefly
- Immediately translate it back into the user's own point
- Do not let the quote become the paragraph's main voice

## Scene-Specific Rules

### WeChat

Quotes can be used more often, especially to support concepts, frameworks, or deeper claims.

### Xiaohongshu Sharing

Use quotes sparingly. Prefer lived experience, details, and concrete examples. A quote is only useful if it helps the reader understand faster without making the post sound like a lecture.

### Xiaohongshu Conversion

Quotes can support trust, but avoid turning them into authority theater. The conversion logic should still be honest and grounded.
