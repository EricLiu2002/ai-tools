---
name: "fyf"
description: Translate French into Chinese (Simplified). Use this skill whenever the user types "/fyf", says "fyf", or asks to translate French words, phrases, sentences, or passages into Chinese, even if they just paste French text after "fyf". For a single French word, also give its pronunciation and example sentences.
---

# fyf — French → Chinese translator

Translate the French input the user provides into natural, accurate Simplified Chinese.

## Decide the input type

- **Single word** (one French word, e.g. "bibliothèque", "manger"): use the *Single word* format below.
- **Anything longer** (phrase, sentence, paragraph): use the *Text* format below.

## Single word format

Give:

1. **Word**, part(s) of speech, and grammatical gender for nouns (m./f.). For verbs, note the infinitive if a conjugated form was given; for adjectives, give the feminine form if it differs.
2. **Pronunciation**: IPA (e.g. /bi.bli.jɔ.tɛk/) plus a simple respelling an English/Chinese speaker can read (e.g. bee-blee-oh-TEK). Mention silent letters or liaison if relevant.
3. **Chinese meaning(s)**: the main Chinese translation(s), one line per sense if the word has several common meanings (e.g. 图书馆).
4. **Example sentences**: 3 natural French sentences using the word (covering different senses if there are several), each followed by its Chinese translation.

Example layout:

**bibliothèque** (nom féminin, f.)
发音: /bi.bli.jɔ.tɛk/ · bee-blee-oh-TEK
中文: 图书馆；书架

例句:
1. Je vais à la bibliothèque tous les samedis.
   我每个星期六都去图书馆。
2. ...

## Text format

- Give the Chinese translation directly. Keep meaning, tone, and register (tu/vous politeness) faithful to the original; prefer natural Chinese over word-for-word renderings.
- Keep names, numbers, and formatting (line breaks, lists) intact.
- If an idiom has no direct equivalent, translate the meaning and add a short note.
- Do not add pronunciation or example sentences for multi-word input unless the user asks.

## General

- Never show pinyin or any other romanization of the Chinese, in any format, unless the user explicitly asks for it. Pronunciation applies only to the source word.
- Use Simplified Chinese unless the user asks for Traditional.
- If accents are missing (e.g. "bibliotheque"), recognize the intended word and show it with correct accents.
- If the input is not French (e.g. it is English), say so briefly and translate it anyway, or suggest the `fye` skill for English.
