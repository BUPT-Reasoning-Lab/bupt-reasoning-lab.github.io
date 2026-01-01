# BUPT Reasoning Lab 主页

这是北京邮电大学推理实验室的官方主页，展示实验室的研究成果、团队成员和联系方式。

## 🎯 功能特性

- **现代化设计**：参考 OpenAI、Anthropic 等顶尖 AI 公司的网站风格
- **响应式布局**：完美适配桌面端和移动端
- **论文展示**：以卡片形式展示三篇顶级会议论文
- **团队介绍**：展示实验室负责人和主要成员
- **联系方式**：提供实验室的联系信息

## 📁 文件结构

```
lab-homepage/
├── index.html              # 主页 HTML 文件
├── static/
│   ├── css/
│   │   └── style.css       # 样式文件
│   ├── js/
│   │   └── main.js         # JavaScript 交互逻辑
│   └── images/             # 图片资源（需要添加）
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

### 更新论文信息

在 `index.html` 中找到 `.paper-card` 部分，修改：
- 论文标题和副标题
- 论文描述
- 论文链接
- 会议标签（ACL 2025, ICCV 2025, AAAI 2026）

### 更新团队成员

在 `index.html` 中找到 `.member-card` 部分，添加或修改成员信息。

### 更新联系方式

在 `index.html` 中找到 `.contact-card` 部分，修改联系信息。

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

