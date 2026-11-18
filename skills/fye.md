---
name: "fye"
description: Translate English into Chinese (Simplified). Use this skill whenever the user types "/fye", says "fye", or asks to translate English words, phrases, sentences, or passages into Chinese, even if they just paste English text after "fye". For a single English word, also give its pronunciation and example sentences.
---

# fye — English → Chinese translator

Translate the English input the user provides into natural, accurate Simplified Chinese.

## Decide the input type

- **Single word** (one English word, e.g. "resilient", "run"): use the *Single word* format below.
- **Anything longer** (phrase, sentence, paragraph): use the *Text* format below.

## Single word format

Give:

1. **Word** and part(s) of speech.
2. **Pronunciation**: IPA for both US and UK (e.g. US /rɪˈzɪliənt/, UK /rɪˈzɪliənt/), plus a simple syllable respelling with the stressed syllable in capitals (e.g. ri-ZIL-ee-uhnt).
3. **Chinese meaning(s)**: the main Chinese translation(s), one line per sense if the word has several common meanings (e.g. 有韧性的).
4. **Example sentences**: 3 natural English sentences showing the word in use (covering different senses if there are several), each followed by its Chinese translation.

Example layout:

**resilient** (adjective)
发音: US /rɪˈzɪliənt/ · UK /rɪˈzɪliənt/ · ri-ZIL-ee-uhnt
中文: 有韧性的；能迅速恢复的

例句:
1. Children are often more resilient than adults expect.
   孩子们往往比大人想象的更有韧性。
2. ...

## Text format

- Give the Chinese translation directly. Keep meaning, tone, and register faithful to the original; prefer natural Chinese over word-for-word renderings.
- Keep names, numbers, and formatting (line breaks, lists) intact.
- If an idiom or phrase has no direct equivalent, translate the meaning and add a short note.
- Do not add pronunciation or example sentences for multi-word input unless the user asks.

## General

- Never show pinyin or any other romanization of the Chinese, in any format, unless the user explicitly asks for it. Pronunciation applies only to the source word.
- Use Simplified Chinese unless the user asks for Traditional.
- If the input is not English (e.g. it is French), say so briefly and translate it anyway, or suggest the `fyf` skill for French.
- If the word is ambiguous or a typo, give the likely intended word and note it.
