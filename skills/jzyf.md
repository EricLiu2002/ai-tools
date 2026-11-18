---
name: jzyf
description: Correct the grammar of an English sentence or paragraph and provide two versions, a formal version and an informal version. Use this skill whenever the user types "jzyf", says "jzyf", or pastes an English sentence or paragraph and asks for it to be corrected, polished, or rewritten in formal and informal styles, even if they just paste the text after "jzyf".
---

# jzyf: Grammar Correction with Formal and Informal Versions

When the user gives you an English sentence or paragraph, return a grammatically correct version of it in two styles: formal and informal.

## Steps

1. Read the user's text carefully and identify the intended meaning. Do not change the meaning, facts, or key details.
2. Fix all grammar, spelling, punctuation, capitalization, and sentence structure errors.
3. Write the **Formal** version: professional and polished, suitable for work emails, reports, or academic writing. Avoid contractions, slang, and casual phrasing.
4. Write the **Informal** version: relaxed and conversational, suitable for chats, friendly messages, or social posts. Contractions and everyday phrasing are fine. It must still be grammatically correct.
5. If the input is already grammatically correct, say so briefly and still provide both versions.

## Output Format

Use this structure and nothing heavy beyond it:

**Formal**
[formal version as a single paragraph, or the same number of sentences as the input]

**Informal**
[informal version as a single paragraph, or the same number of sentences as the input]

Do not add bullet lists, tables, or lengthy explanations unless the user asks for them. If the user asks what was changed, give a short list of the main corrections.

## Rules

- Preserve the original meaning in both versions.
- Keep roughly the same length as the original, unless the grammar fix requires otherwise.
- If the input is not English, or is too unclear to correct, ask the user for clarification in one short question.
- If the user pastes only a single word, explain that this skill works on sentences and paragraphs, and offer to check the word's spelling or usage instead.
