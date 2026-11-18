---
name: "zwjs"
description: Translate English phrases, sentences, or technical terms into Simplified Chinese and explain the key components and technical terms in a structured breakdown. Use this skill whenever the user types "/zwjs" followed by text, says "zwjs", or asks to translate and explain English text in the zwjs style, even if they only paste English text after the command. Also use it when the user wants a Chinese translation of technical English (engineering, product, standards, or tooling terms) together with an explanation of each term.
---

# zwjs: English to Simplified Chinese Translation with Structured Explanation

When the user types `/zwjs` followed by text, says "zwjs", or asks to translate and explain text in the zwjs style, produce the response in the exact structure below.

## Output structure

Always use this order and these labels:

```
Translation: [Simplified Chinese translation]

中文详细解释：
[1-2 sentences summarizing the overall meaning in context]

具体拆解如下：

* [Term 1]（[Chinese translation / meaning]）：
   * [What the term is, its role, and why it matters in this context]
   * [For a single English word: pronunciation and example sentences, per the fye rule below]
* [Term 2]（[Chinese translation / meaning]）：
   * [What the term is, its role, and why it matters in this context]
```

## Section rules

1. **Translation**: Give a clear, natural-sounding Simplified Chinese translation of the full input. Prefer idiomatic Chinese over word-for-word rendering. Keep widely used English technical terms (for example API, JSON, OAuth) in English inside the translation when Chinese engineers commonly do so.

2. **中文详细解释 (Summary / Overview)**: Write 1-2 sentences in Chinese explaining what the input means in context: its purpose, who it is for, or what action it implies.

3. **具体拆解如下 (Detailed Breakdown)**: List the key technical terms, tools, standards, or concepts in the input as top-level bullets. For each:
   * Put the term first, then its Chinese translation or meaning in full-width parentheses, for example `Webhook（网络钩子）：`.
   * Under it, add one or more sub-bullets giving a concise technical explanation: what it is, what it is used for, and why it matters in this context.
   * Keep each explanation to roughly 1-3 sentences. Do not pad.

4. Word explanations (fye rule): Apply the fye word format only to English words that the user places in parentheses in their input. For example, in do you know what is (good), explain “good” with the fye format. Do not apply it to other single words in the breakdown, and do not apply it to any word the user did not put in parentheses. For each parenthesized single word, add these sub-bullets under the term:
Pronunciation: US and UK IPA, plus a syllable respelling with the stressed syllable in capitals, for example 发音: US /eɪ.pi.aɪ/ · UK /eɪ.pi.aɪ/ · ay-pee-eye.
Chinese meaning(s): one line per common sense if the word has several, for example 中文: 应用程序编程接口.
Example sentences: 3 natural English sentences using the word, each followed by its Chinese translation. Where the word has several senses, cover different senses.
Multi-word terms get no pronunciation or example sentences, even if they appear in parentheses. Their explanation in the normal sub-bullet is enough.
Never show pinyin or any romanization of Chinese. Pronunciation applies only to the English source word.

## Scope guidance

- **Single word or short phrase**: Still provide the Translation, a brief overview, and a breakdown only if the term has a meaningful technical sense. Skip the breakdown for plain everyday words. If the input is a single English word, the fye word format applies to it.
- **Sentence or paragraph**: Break down only the terms that carry technical weight. Usually 3-6 terms is enough; do not list every noun.
- **Input that is already Chinese**: Translate it into English instead and apply the same structure in reverse, with the breakdown in Chinese. The fye rule does not apply in this case.
- **Ambiguous terms**: Choose the sense that fits the context and, if a second common meaning exists, note it briefly inside the explanation.

## Style

- Write the explanatory text in Simplified Chinese. Use English only for terms that are normally written in English.
- Use the full-width colon `：` after section labels and term names, as shown in the template.
- Keep formatting clean: use the labels and bullets shown above, and avoid extra headings, tables, or closing remarks.
- Do not add disclaimers or commentary about the skill itself.

## Example

Input: `/zwjs The API returns a JSON payload authenticated with a bearer token.`

Translation: API 返回一个由 Bearer 令牌认证的 JSON 负载。

中文详细解释：
这句话描述了某个接口的返回格式和访问认证方式，常见于后端接口文档或技术说明中，强调调用方需要携带有效凭证才能获取数据。

具体拆解如下：

* API（应用程序编程接口）：
   * 一组预先定义的接口规范，允许不同软件系统之间相互调用和交换数据，是前后端或服务间通信的基础。
   * 发音: US /eɪ.pi.aɪ/ · UK /eɪ.pi.aɪ/ · ay-pee-eye
   * 中文: 应用程序编程接口
   * 例句:
     1. The company published a public API so developers can build apps on its data.
        该公司发布了公开 API，方便开发者基于其数据开发应用。
     2. Our payment API handles all refund requests automatically.
        我们的支付 API 会自动处理所有退款请求。
     3. Make sure the API version matches the one in the documentation.
        请确保 API 版本与文档中的版本一致。
* JSON（JavaScript 对象表示法）：
   * 一种轻量级的数据交换格式，以键值对形式组织数据，易于人和机器读写，是 Web API 最常用的返回格式。
   * 发音: US /ˈdʒeɪ.sɑn/ · UK /ˈdʒeɪ.sɒn/ · JAY-sun
   * 中文: JSON 格式；（作形容词时）与 JSON 相关的
   * 例句:
     1. The server sends its response as a JSON file.
        服务器以 JSON 文件的形式发送响应。
     2. Please validate the JSON before importing it.
        导入之前请先校验 JSON 格式。
     3. The config is stored in a JSON object for easy editing.
        配置以 JSON 对象的形式存储，便于编辑。
* payload（负载/数据体）：
   * 指请求或响应中真正承载的数据内容，不包括协议头等附加信息，在这里指接口返回的实际数据。
   * 发音: US /ˈpeɪ.loʊd/ · UK /ˈpeɪ.ləʊd/ · PAY-lohd
   * 中文: 负载；有效载荷；数据体
   * 例句:
     1. The message payload contains the user ID and the timestamp.
        消息负载中包含用户 ID 和时间戳。
     2. Large payloads can slow down the mobile app.
        过大的数据负载可能会拖慢移动应用。
     3. The payload was encrypted before it was sent.
        负载在发送前已被加密。
* bearer token（Bearer 令牌）：
   * 一种访问令牌，持有者即被视为有权访问的身份，调用方通常在 HTTP 请求头 Authorization 中以 "Bearer" 前缀携带它，用于无状态的身份认证。
