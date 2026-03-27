# Schema 结构化数据模板

## 为什么 Schema 对 AI-SEO 至关重要

结构化数据是机器读取「你是谁、你做什么」的主要信号。
AI 搜索引擎通过 Schema 建立实体图谱，完整的 Schema = 更高的引用概率。

---

## 6种网站类型模板

### 1. 企业/机构（Organization）

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "@id": "https://YOUR_DOMAIN/#organization",
  "name": "企业名称",
  "url": "https://YOUR_DOMAIN",
  "description": "一句话描述企业做什么",
  "foundingDate": "2020-01-01",
  "logo": {
    "@type": "ImageObject",
    "url": "https://YOUR_DOMAIN/logo.png"
  },
  "founder": {
    "@type": "Person",
    "name": "创始人姓名",
    "sameAs": [
      "https://twitter.com/YOUR_TWITTER",
      "https://www.linkedin.com/in/YOUR_LINKEDIN"
    ]
  },
  "sameAs": [
    "https://www.linkedin.com/company/YOUR_CO",
    "https://github.com/YOUR_GITHUB",
    "https://twitter.com/YOUR_TWITTER"
  ],
  "knowsAbout": ["领域1", "领域2", "领域3"]
}
```

---

### 2. SaaS 软件（SoftwareApplication）

```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "产品名称",
  "url": "https://YOUR_DOMAIN",
  "description": "产品一句话描述",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Web",
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "0",
    "priceCurrency": "USD"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "200"
  },
  "featureList": ["功能1", "功能2", "功能3"]
}
```

---

### 3. 本地服务（LocalBusiness）

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "店铺/服务名称",
  "url": "https://YOUR_DOMAIN",
  "telephone": "+86-XXX-XXXX-XXXX",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "街道地址",
    "addressLocality": "城市",
    "addressCountry": "CN"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 39.9042,
    "longitude": 116.4074
  },
  "openingHours": "Mo-Fr 09:00-18:00",
  "priceRange": "$$"
}
```

---

### 4. 文章/博客（Article + Person）

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "文章标题",
  "author": {
    "@type": "Person",
    "name": "作者姓名",
    "url": "https://YOUR_DOMAIN/about",
    "sameAs": ["https://twitter.com/AUTHOR"]
  },
  "datePublished": "2026-01-01",
  "dateModified": "2026-03-01",
  "publisher": {
    "@type": "Organization",
    "name": "网站名称",
    "logo": {
      "@type": "ImageObject",
      "url": "https://YOUR_DOMAIN/logo.png"
    }
  },
  "description": "文章摘要（150字以内）"
}
```

---

### 5. 电商产品（Product）

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "产品名称",
  "description": "产品描述",
  "brand": {
    "@type": "Brand",
    "name": "品牌名"
  },
  "offers": {
    "@type": "Offer",
    "price": "99",
    "priceCurrency": "CNY",
    "availability": "https://schema.org/InStock"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.5",
    "reviewCount": "100"
  }
}
```

---

### 6. FAQ 页面（FAQPage）—— 对 Google AIO 效果最强

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "问题1是什么？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "回答1，直接、具体、自包含。"
      }
    },
    {
      "@type": "Question",
      "name": "问题2怎么解决？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "回答2，最优长度134-167字。"
      }
    }
  ]
}
```

---

## 部署方式

把 JSON-LD 放在 HTML `<head>` 标签内：

```html
<head>
  <script type="application/ld+json">
  {
    // 你的 Schema JSON
  }
  </script>
</head>
```

## 验证工具

- Google Rich Results Test: https://search.google.com/test/rich-results
- Schema.org 验证器: https://validator.schema.org
