# 🇨🇳 国产大模型接入指南

> OpenClaw 支持任何兼容 OpenAI API 格式的模型。以下是中国开发者常用的国产模型接入方式。

## 快速配置

在 OpenClaw 配置文件中添加自定义 provider：

```yaml
# ~/.openclaw/config.yaml
providers:
  - name: deepseek
    baseUrl: https://api.deepseek.com/v1
    apiKey: ${DEEPSEEK_API_KEY}
    models:
      - deepseek-chat
      - deepseek-coder
      - deepseek-reasoner

  - name: qwen
    baseUrl: https://dashscope.aliyuncs.com/compatible-mode/v1
    apiKey: ${DASHSCOPE_API_KEY}
    models:
      - qwen-turbo
      - qwen-plus
      - qwen-max

  - name: glm
    baseUrl: https://open.bigmodel.cn/api/paas/v4
    apiKey: ${ZHIPU_API_KEY}
    models:
      - glm-4-plus
      - glm-4-flash

  - name: moonshot
    baseUrl: https://api.moonshot.cn/v1
    apiKey: ${MOONSHOT_API_KEY}
    models:
      - moonshot-v1-8k
      - moonshot-v1-32k
      - moonshot-v1-128k

  - name: doubao
    baseUrl: https://ark.cn-beijing.volces.com/api/v3
    apiKey: ${DOUBAO_API_KEY}
    models:
      - doubao-pro-32k
      - doubao-lite-32k
```

## 各模型申请地址

| 模型 | 申请地址 | 免费额度 | 特点 |
|------|----------|----------|------|
| DeepSeek | [platform.deepseek.com](https://platform.deepseek.com/) | 新用户送 500 万 tokens | 性价比极高，推理能力强 |
| 通义千问 | [dashscope.console.aliyun.com](https://dashscope.console.aliyun.com/) | 100 万 tokens/月 | 阿里云生态，中文理解好 |
| 智谱 GLM | [open.bigmodel.cn](https://open.bigmodel.cn/) | 新用户送额度 | 清华系，学术背景强 |
| Moonshot | [platform.moonshot.cn](https://platform.moonshot.cn/) | 新用户送 15 元 | 长上下文支持好 |
| 豆包 | [console.volcengine.com/ark](https://console.volcengine.com/ark) | 50 万 tokens | 字节系，响应快 |
| 百川 | [platform.baichuan-ai.com](https://platform.baichuan-ai.com/) | 新用户送额度 | 搜索增强能力 |
| MiniMax | [platform.minimaxi.com](https://platform.minimaxi.com/) | 新用户送额度 | 多模态支持 |

## 环境变量配置

```bash
# ~/.zshrc 或 ~/.bashrc
export DEEPSEEK_API_KEY="sk-xxx"
export DASHSCOPE_API_KEY="sk-xxx"
export ZHIPU_API_KEY="xxx.xxx"
export MOONSHOT_API_KEY="sk-xxx"
export DOUBAO_API_KEY="xxx"
```

## 使用建议

1. **日常对话**：DeepSeek Chat 或 Qwen Turbo（便宜够用）
2. **代码生成**：DeepSeek Coder 或 GLM-4-Plus
3. **长文档处理**：Moonshot 128K 或 Qwen-Long
4. **复杂推理**：DeepSeek Reasoner（R1）

## 常见问题

**Q: 为什么用国产模型？**
- 网络稳定，无需代理
- 价格便宜（通常是 GPT-4 的 1/10）
- 中文理解更好
- 数据合规

**Q: 如何切换默认模型？**
```yaml
# config.yaml
defaultModel: deepseek/deepseek-chat
```

**Q: 遇到 API 报错怎么办？**
- 检查 API Key 是否正确
- 确认账户余额充足
- 查看模型是否在白名单内

---

> 💡 欢迎 PR 补充更多国产模型接入方式！
