# BUPT Reasoning Lab 主页

这是北京邮电大学推理实验室的官方主页，展示实验室的研究成果、团队成员和联系方式。

## 🎯 功能特性

- **现代化设计**：参考 OpenAI、Anthropic 等顶尖 AI 公司的网站风格
- **响应式布局**：完美适配桌面端和移动端
- **重点项目展示**：首页首屏展示实验室最新产品或平台入口
- **论文展示**：以卡片形式展示三篇顶级会议论文
- **团队介绍**：展示实验室负责人和主要成员
- **联系方式**：提供实验室的联系信息
- **中英文切换**：导航栏提供语言切换按钮，翻译文案集中维护在 JSON 文件中

## 📁 文件结构

```
lab-homepage/
├── index.html              # 主页 HTML 文件
├── static/
│   ├── css/
│   │   └── style.css       # 样式文件
│   ├── js/
│   │   └── main.js         # JavaScript 交互逻辑
│   ├── data/
│   │   └── translations.json # 中英文翻译文案
│   ├── images/             # 图片资源（需要添加）
│   └── videos/             # 视频资源
├── DEPLOYMENT.md           # 部署指南
└── README.md               # 本文件
```

## 🚀 快速开始

### 本地预览

1. 使用简单的 HTTP 服务器预览（Python 3）：

```bash
cd lab-homepage
python3 -m http.server 8000
```

2. 在浏览器中访问 `http://localhost:8000`

### 部署到 GitHub Pages

详细部署步骤请参考 [DEPLOYMENT.md](./DEPLOYMENT.md)

## 🎨 自定义

### 更新首页重点项目

首页首屏的重点项目展示在 `index.html` 的 `#home` 区块中，主要包括：
- 产品名称、简介、访问按钮和当前访问地址
- Demo 视频播放器
- 正式域名状态说明

如果修改产品文案，请同步更新 `static/data/translations.json`。如果替换 Demo 视频，请将新视频放入 `static/videos/`，并更新 `index.html` 中 `<video>` 的 `source` 路径。建议视频使用 `.mp4` 格式，并尽量控制文件大小，避免影响首屏加载体验。

### 更新论文信息

在 `index.html` 中找到 `.paper-card` 部分，修改页面结构和链接：
- 论文标题和副标题
- 论文链接
- 会议标签（ACL 2025, ICCV 2025, AAAI 2026）

如果修改了需要中英文切换的可见文案，请同步更新 `static/data/translations.json` 中对应的 `zh` 和 `en` 字段。

### 更新团队成员

在 `index.html` 中找到 `.member-card` 部分，添加或修改成员信息。

如果成员姓名、角色、简介等内容需要支持中英文切换，请同步更新 `static/data/translations.json`。

### 更新联系方式

在 `index.html` 中找到 `.contact-card` 部分，修改联系信息。

### 维护中英文文案

本项目使用 `data-i18n` 属性和 `static/data/translations.json` 维护中英文切换。

1. 在 `index.html` 中给需要翻译的元素添加唯一 key：

```html
<p data-i18n="news.newPaper">我们的一篇新论文被接收。</p>
```

2. 在 `static/data/translations.json` 中同时添加中文和英文：

```json
{
  "zh": {
    "news.newPaper": "我们的一篇新论文被接收。"
  },
  "en": {
    "news.newPaper": "Our new paper has been accepted."
  }
}
```

3. 本地预览时请使用 HTTP 服务器访问页面：

```bash
python3 -m http.server 8000
```

语言切换功能会通过 `fetch` 加载 `static/data/translations.json`。如果直接双击打开 `index.html`，部分浏览器可能会拦截本地 JSON 文件读取，导致切换功能不可用。

## 📝 待办事项

- [ ] 添加实验室 Logo 和 favicon
- [ ] 添加实验室 Banner 图片（1200x630）
- [ ] 添加更多团队成员
- [ ] 添加实验室简介视频（可选）
- [ ] 添加研究领域介绍（可选）

## 🔗 相关链接

- [FinanceReasoning 主页](https://bupt-reasoning-lab.github.io/FinanceReasoning/)
- [FinMMR 主页](https://bupt-reasoning-lab.github.io/FinMMR/)
- [FinMMDocR 主页](https://bupt-reasoning-lab.github.io/FinMMDocR/)

## 📄 许可证

本项目使用 MIT 许可证。

---

© 2026 BUPT Reasoning Lab. All rights reserved.
