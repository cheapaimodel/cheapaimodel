<div align="center">

# CheapAIModel

**一个 API，调用主流 AI 模型，价格低于官方。**

兼容 OpenAI · 按量付费 · 无绑定

[English](README.md) | 简体中文

[官网](https://cheapaimodel.ai/?utm_source=github&utm_medium=profile-zh) · [获取 API Key](https://console.cheapaimodel.ai/keys?utm_source=github&utm_medium=profile-zh) · [文档](https://github.com/cheapaimodel/docs/blob/main/zh-CN/quickstart.md) · [示例代码](https://github.com/cheapaimodel/examples)

</div>

---

## 为什么选择 CheapAIModel？

- **一个 API，多个模型。** 通过同一个接口调用不同厂商的模型。
- **价格更低。** 所有模型均比官方价格低 5%。最低充值 $5，无订阅。
- **兼容 OpenAI。** 已在使用 OpenAI SDK？只需修改 base URL 和 API Key。
- **按量付费。** 按 token 计费，无最低消费。

从 OpenRouter 迁移？只需改几行：[迁移指南（英文）](https://github.com/cheapaimodel/docs/blob/main/migrate-from-openrouter.md)

## 模型与价格

| 模型 | 输入 / 百万 tokens | 输出 / 百万 tokens |
| --- | --- | --- |
| `kimi-k3` | $2.85 | $14.25 |
| `glm-5.3` | $1.33 | $4.18 |
| `glm-5.3-flash` | $0.1425 | $0.475 |
| `deepseek-v4-1-flash` | $0.285 | $1.14 |

最新完整列表：[cheapaimodel.ai/models](https://cheapaimodel.ai/models?utm_source=github&utm_medium=profile-zh)

## 快速开始

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://api.cheapaimodel.ai/v1",
    api_key="YOUR_CHEAPAIMODEL_KEY",
)

res = client.chat.completions.create(
    model="glm-5.3-flash",
    messages=[{"role": "user", "content": "你好！"}],
)
print(res.choices[0].message.content)
```

在 Cline、Cherry Studio、LobeChat、SillyTavern、OpenClaw 等工具中，选择 **OpenAI Compatible**，填入 base URL `https://api.cheapaimodel.ai/v1`、你的 API Key 和模型 ID 即可。详细步骤：[examples/integrations](https://github.com/cheapaimodel/examples/tree/main/integrations)

## 开源项目

| 仓库 | 说明 |
| --- | --- |
| [python-sdk](https://github.com/cheapaimodel/python-sdk) | 轻量 Python 客户端，基于 OpenAI SDK |
| [typescript-sdk](https://github.com/cheapaimodel/typescript-sdk) | 轻量 TypeScript 客户端，基于 OpenAI SDK |
| [examples](https://github.com/cheapaimodel/examples) | 示例代码与各工具配置指南 |
| [docs](https://github.com/cheapaimodel/docs) | API 文档 |
| [awesome-cheapaimodel](https://github.com/cheapaimodel/awesome-cheapaimodel) | 支持 CheapAIModel 的工具与应用 |

---

<div align="center">Made in Vietnam 🇻🇳 · 为全球开发者打造</div>
