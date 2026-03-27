# 🤖 AI-SEO：让你的网站被 AI 搜索引用

> 传统 SEO 优化 Google 排名。AI-SEO 优化 ChatGPT / Perplexity / Claude 的引用。

AI 搜索流量正在爆炸式增长，转化率是普通搜索的 **4.4倍**。但只有 **23%** 的站长在做这件事。

---

## 📊 为什么现在必须做 AI-SEO

| 数据 | 来源 |
|------|------|
| AI 引用流量增长 +527%（2025年） | SparkToro |
| AI 流量转化率是普通搜索 4.4倍 | 行业数据 |
| 品牌提及对 AI 引用的权重是反链 3倍 | Ahrefs 2025 |
| 2028年 Google 搜索流量预计下降 50% | Gartner |
| 目前只有 23% 的营销人员在做 GEO | 行业调研 |

---

## ✨ 功能

| 命令 | 功能 |
|------|------|
| `/ai-seo audit <url>` | 完整 AI-SEO 审计（评分 0-100 + 行动清单） |
| `/ai-seo quick <url>` | 60秒快速快照 |
| `/ai-seo citability <url>` | AI 可引用性评分 |
| `/ai-seo crawlers <url>` | 检查 AI 爬虫是否能访问你的网站 |
| `/ai-seo llmstxt <url>` | 分析或生成 llms.txt |
| `/ai-seo brands <url>` | 品牌提及扫描（Reddit/YouTube/Wikipedia） |
| `/ai-seo schema <url>` | 结构化数据检测与生成 |
| `/ai-seo content <url>` | 内容质量 + E-E-A-T 评估 |
| `/ai-seo technical <url>` | 技术 SEO 审计 |
| `/ai-seo report <url>` | 生成完整 Markdown 报告 |

---

## 🚀 安装

```bash
# 克隆到 Claude Code skills 目录
git clone https://github.com/linxumoney/ai-seo.git ~/.claude/skills/ai-seo

# 在 Claude Code 中使用
/ai-seo audit https://yourwebsite.com
```

---

## 📐 评分体系

| 维度 | 权重 |
|------|------|
| AI 可引用性 & 可见性 | 25% |
| 品牌权威信号 | 20% |
| 内容质量 & E-E-A-T | 20% |
| 技术基础 | 15% |
| 结构化数据 | 10% |
| 平台优化（ChatGPT/Perplexity/Google AIO） | 10% |

---

## 🧠 核心概念：什么是 AI 可引用性

AI 搜索在回答问题时，会从网页中提取「可引用段落」。研究发现（Princeton/Georgia Tech，2024），符合以下特征的段落被引用率高出 30-115%：

- ✅ 首句直接给出答案（答案前置）
- ✅ 134-167字，自成一体
- ✅ 包含具体数据和命名实体
- ✅ 无需上下文即可理解

---

## 📁 文件结构

```
ai-seo/
├── SKILL.md                      ← Claude Code skill 主文件
└── references/
    ├── citability.md             ← AI 可引用性详细评分标准
    ├── crawlers.md               ← 14+ AI 爬虫列表及 robots.txt 配置
    ├── platform-rules.md         ← ChatGPT/Perplexity/Google AIO 优化规则
    └── schema-templates.md       ← 6种网站类型 JSON-LD 模板
```

---

## 📡 关注我

这是「**[林序聊AI · 开源计划](https://github.com/linxumoney)**」的开源项目之一。我会持续开源更多 AI 内容创作工具。

| 平台 | 链接 |
|------|------|
| 🐦 X (Twitter) | [@linxumoney](https://x.com/linxumoney) |
| 📺 YouTube | [@LinXuMoney](https://www.youtube.com/@LinXuMoney) |
| 💻 GitHub | [github.com/linxumoney](https://github.com/linxumoney) |

觉得有用的话，**点个 Star ⭐ 支持一下**，让更多人发现这个工具。

---

## 📄 License

MIT License — 自由使用、修改、分发。
