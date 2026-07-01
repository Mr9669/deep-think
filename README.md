# deep-think 🧠

**结构化推理增强器** — 一行代码为任何LLM注入第一性原理推理能力。

## 为什么用 deep-think？

GPT-4、DeepSeek、Claude 都很强，但它们的回答质量取决于 prompt 质量。`deep-think` 提供了一个经过验证的结构化推理框架，自动注入到你的 LLM 调用中。

## 安装

```bash
pip install deep-think
```

## 快速开始

```python
from deep_think import enhance

# 获得增强后的 system prompt
system_prompt = enhance()
print(system_prompt)  # 包含完整推理框架

# 直接注入到 messages
from deep_think import wrap_messages
messages = [{"role": "user", "content": "分析量子计算的未来"}]
enhanced = wrap_messages(messages)

# 装饰器模式 — 自动注入
from deep_think import inject_seed

@inject_seed
def my_llm_call(messages):
    return openai.ChatCompletion.create(model="gpt-4", messages=messages)
```

## 推理框架包含

- ✅ 第一性原理分析
- ✅ 多角度审视
- ✅ 认知诚实
- ✅ 结构化思维（定义→分解→分析→综合→验证）

## License

MIT
