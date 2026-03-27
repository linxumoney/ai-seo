# AI 爬虫完整列表与 robots.txt 配置

## 关键原则

超过35%的主流网站无意中屏蔽了至少一个主流 AI 爬虫（Originality.ai，2025）。
屏蔽 AI 爬虫 = 在 AI 搜索结果中彻底消失。

---

## Tier 1：必须放行（直接影响 AI 搜索可见性）

| 爬虫 | 运营商 | User-Agent | 影响 |
|------|--------|------------|------|
| GPTBot | OpenAI | `GPTBot` | ChatGPT 搜索和浏览 |
| OAI-SearchBot | OpenAI | `OAI-SearchBot` | ChatGPT 搜索（仅检索，不训练） |
| ChatGPT-User | OpenAI | `ChatGPT-User` | 用户让 ChatGPT 访问特定URL |
| ClaudeBot | Anthropic | `ClaudeBot` | Claude 网页搜索和引用 |
| Claude-User | Anthropic | `Claude-User` | 用户让 Claude 访问特定URL |
| PerplexityBot | Perplexity | `PerplexityBot` | Perplexity 搜索索引 |
| cohere-ai | Cohere | `cohere-ai` | Cohere AI 搜索 |

---

## Tier 2：建议放行（AI 平台训练，间接影响引用）

| 爬虫 | 运营商 | User-Agent |
|------|--------|------------|
| Google-Extended | Google | `Google-Extended` |
| Googlebot | Google | `Googlebot` |
| bingbot | Microsoft | `bingbot` |
| meta-externalagent | Meta | `meta-externalagent` |
| Bytespider | ByteDance | `Bytespider` |

---

## Tier 3：可选择性屏蔽（训练数据爬虫，无直接搜索影响）

| 爬虫 | 运营商 | 说明 |
|------|--------|------|
| CCBot | Common Crawl | 开放数据集，多个 AI 模型训练数据来源 |
| omgili | Webhose | 内容聚合 |
| Diffbot | Diffbot | 知识图谱构建 |

---

## 推荐 robots.txt 配置

### 最大化 AI 可见性（推荐大多数网站）
```
User-agent: GPTBot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: Google-Extended
Allow: /
```

### 允许搜索，屏蔽训练数据
```
# 放行搜索类爬虫
User-agent: GPTBot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

# 屏蔽纯训练数据爬虫
User-agent: CCBot
Disallow: /

User-agent: Google-Extended
Disallow: /
```

---

## 检测方法

```bash
# 检查 robots.txt
curl -s https://example.com/robots.txt

# 检查各爬虫的 meta 标签
curl -s https://example.com | grep -i "robots\|googlebot\|gptbot"
```

检查 `<meta name="robots">` 标签，如果包含 `noindex` 或 `nofollow`，AI 爬虫通常也会遵守。
