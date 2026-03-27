# 各 AI 平台优化规则

## ChatGPT（OpenAI）

**核心机制：** 优先引用有明确权威信号的页面，偏好结构化内容。

**优化要点：**
- 允许 GPTBot 和 OAI-SearchBot 爬取
- 在 About 页面明确描述公司/个人的专业领域
- 使用 Organization 或 Person Schema
- 确保重要页面不在 JavaScript 渲染后才加载（需 SSR）
- 在权威平台（Wikipedia、LinkedIn）建立品牌提及

**llms.txt：** ChatGPT 支持读取 llms.txt，建议部署。

---

## Perplexity

**核心机制：** 强调实时性和来源多样性，偏好有清晰事实的段落。

**优化要点：**
- 允许 PerplexityBot 爬取
- 内容需有明确发布/更新时间
- 高事实密度（每段含具体数字和来源）
- 在 Reddit、Quora 等社区有品牌讨论
- 页面加载速度要快（Core Web Vitals 良好）

**特点：** Perplexity 显示引用来源，引用后会带来直接流量。

---

## Google AI Overviews（SGE）

**核心机制：** 基于 Google 搜索索引，E-E-A-T 权重极高。

**优化要点：**
- 标准 Google SEO 基础要扎实（反链、域名权威度）
- 使用 FAQ Schema（`FAQPage`），直接提升 AIO 引用概率
- HowTo Schema 适合教程类内容
- 作者页面要完整（姓名、简介、专业背景）
- 内容需体现「亲身经历」（Experience）——第一人称案例

**注意：** Google 只引用它已经索引的页面，传统 SEO 基础不能忽视。

---

## Claude（Anthropic）

**核心机制：** 重视内容准确性，偏好有逻辑结构的长文。

**优化要点：**
- 允许 ClaudeBot 爬取
- 内容逻辑清晰，有明确的因果关系
- 避免模糊陈述，每个观点有支撑
- 引用权威数据来源时注明出处
- 复杂话题提供多角度分析

---

## 平台适配矩阵

| 优化动作 | ChatGPT | Perplexity | Google AIO | Claude |
|---------|---------|------------|------------|--------|
| 答案前置结构 | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ |
| 高事实密度 | ⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ |
| FAQ Schema | ⭐⭐ | ⭐⭐ | ⭐⭐⭐ | ⭐ |
| 品牌提及建设 | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ |
| E-E-A-T 信号 | ⭐⭐ | ⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ |
| llms.txt | ⭐⭐⭐ | ⭐⭐ | ⭐ | ⭐⭐ |
| SSR 渲染 | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ |
