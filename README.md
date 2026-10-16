<div align="center">

# CheapAIModel

**One API for every AI model — at the lowest price.**

OpenAI-compatible · Pay as you go · No lock-in

English | [简体中文](README.zh-CN.md)

[Website](https://cheapaimodel.ai?utm_source=github&utm_medium=profile) · [Get an API key](https://console.cheapaimodel.ai/keys?utm_source=github&utm_medium=profile) · [Docs](https://github.com/cheapaimodel/docs) · [Examples](https://github.com/cheapaimodel/examples)

</div>

---

## Why CheapAIModel?

- **One API, many models.** Call models from different providers through a single endpoint.
- **Low prices.** Every model is 5% below the official list price. Top up from $5, no subscription.
- **OpenAI-compatible.** Already using the OpenAI SDK? Change the base URL and API key — that's it.
- **Pay as you go.** No subscriptions, no minimums.

Coming from OpenRouter? Switching takes a few lines: [migration guide](https://github.com/cheapaimodel/docs/blob/main/migrate-from-openrouter.md).

## Models

| Model | Input / 1M tokens | Output / 1M tokens |
| --- | --- | --- |
| `kimi-k3` | $2.85 | $14.25 |
| `glm-5.3` | $1.33 | $4.18 |
| `glm-5.3-flash` | $0.1425 | $0.475 |
| `deepseek-v4-1-flash` | $0.285 | $1.14 |

Full, always up-to-date list: [cheapaimodel.ai/models](https://cheapaimodel.ai/models?utm_source=github&utm_medium=profile)

## Quickstart

**Python**

```bash
pip install openai
```

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://api.cheapaimodel.ai/v1",
    api_key="YOUR_CHEAPAIMODEL_KEY",
)

res = client.chat.completions.create(
    model="glm-5.3-flash",
    messages=[{"role": "user", "content": "Hello!"}],
)
print(res.choices[0].message.content)
```

**JavaScript / TypeScript**

```bash
npm install openai
```

```ts
import OpenAI from "openai";

const client = new OpenAI({
  baseURL: "https://api.cheapaimodel.ai/v1",
  apiKey: process.env.CHEAPAIMODEL_API_KEY,
});

const res = await client.chat.completions.create({
  model: "glm-5.3-flash",
  messages: [{ role: "user", content: "Hello!" }],
});
console.log(res.choices[0].message.content);
```

**cURL**

```bash
curl https://api.cheapaimodel.ai/v1/chat/completions \
  -H "Authorization: Bearer $CHEAPAIMODEL_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"glm-5.3-flash","messages":[{"role":"user","content":"Hello!"}]}'
```

## Our open source

| Repo | What it is |
| --- | --- |
| [python-sdk](https://github.com/cheapaimodel/python-sdk) | Lightweight Python client, built on the OpenAI SDK |
| [typescript-sdk](https://github.com/cheapaimodel/typescript-sdk) | Lightweight TypeScript client, built on the OpenAI SDK |
| [examples](https://github.com/cheapaimodel/examples) | Ready-to-run examples and setup guides for Cline, Cherry Studio, Codex CLI and more |
| [docs](https://github.com/cheapaimodel/docs) | API documentation |
| [awesome-cheapaimodel](https://github.com/cheapaimodel/awesome-cheapaimodel) | Tools and apps that work with CheapAIModel |

---

<div align="center">Made in Vietnam 🇻🇳 · Built for developers everywhere</div>
