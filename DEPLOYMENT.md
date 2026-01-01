# 实验室主页部署指南

本指南将帮助您将实验室入口页部署到 `https://bupt-reasoning-lab.github.io/`。

## 📋 前置要求

1. 拥有 GitHub 账号 `BUPT-Reasoning-Lab`
2. 已安装 Git
3. 已配置 SSH 密钥或使用 HTTPS 访问 GitHub

## 🚀 部署步骤

### 步骤 1: 创建 GitHub 仓库

1. 登录 GitHub 账号 `BUPT-Reasoning-Lab`
2. 点击右上角的 `+`，选择 `New repository`
3. 仓库名称设置为：`bupt-reasoning-lab.github.io`（必须完全匹配）
4. 设置为 `Public`（GitHub Pages 免费版需要公开仓库）
5. **不要**初始化 README、.gitignore 或 license
6. 点击 `Create repository`

### 步骤 2: 准备本地文件

1. 将 `lab-homepage` 文件夹中的所有内容复制到新位置：

```bash
# 在 /home/bupt 目录下
cd /home/bupt
mkdir bupt-reasoning-lab.github.io
cp -r FinMMR/lab-homepage/* bupt-reasoning-lab.github.io/
cd bupt-reasoning-lab.github.io
```

### 步骤 3: 初始化 Git 仓库并推送

```bash
# 初始化 Git 仓库
git init

# 添加所有文件
git add .

# 提交更改
git commit -m "Initial commit: Add lab homepage"

# 添加远程仓库（替换为您的仓库地址）
git remote add origin git@github.com:BUPT-Reasoning-Lab/bupt-reasoning-lab.github.io.git

# 推送到 main 分支
git branch -M main
git push -u origin main
```

### 步骤 4: 配置 GitHub Pages

1. 在 GitHub 仓库页面，点击 `Settings`
2. 在左侧菜单中找到 `Pages`
3. 在 `Source` 部分：
   - 选择 `Deploy from a branch`
   - Branch 选择 `main`
   - Folder 选择 `/ (root)`
4. 点击 `Save`

### 步骤 5: 等待部署完成

- GitHub Pages 通常需要几分钟来构建和部署
- 部署完成后，您可以在仓库的 `Settings > Pages` 页面看到绿色的成功提示
- 访问 `https://bupt-reasoning-lab.github.io/` 查看您的主页

## 📁 文件结构

部署后的文件结构应该是：

```
bupt-reasoning-lab.github.io/
├── index.html          # 主页文件
├── static/
│   ├── css/
│   │   └── style.css   # 样式文件
│   ├── js/
│   │   └── main.js     # JavaScript 文件
│   └── images/         # 图片文件夹（可选）
└── README.md           # 说明文档（可选）
```

## 🎨 自定义配置

### 添加实验室 Logo

1. 将 logo 图片放入 `static/images/` 目录
2. 在 `index.html` 中更新 favicon：
   ```html
   <link rel="icon" type="image/png" href="static/images/favicon.png">
   ```

### 添加实验室 Banner 图片

1. 准备一张 1200x630 像素的图片作为社交媒体分享图
2. 放入 `static/images/` 目录，命名为 `lab-banner.png`
3. 图片已在 HTML 的 meta 标签中引用

### 更新团队成员信息

在 `index.html` 中找到 `.member-card` 部分，修改：
- 成员姓名
- 成员角色
- 成员简介
- 个人主页链接
- Google Scholar 链接（如果有）

### 更新联系方式

在 `index.html` 中找到 `.contact-card` 部分，修改：
- 邮箱地址
- 实验室地址
- GitHub 组织链接

## 🔄 更新内容

当需要更新主页内容时：

```bash
cd /home/bupt/bupt-reasoning-lab.github.io

# 修改文件后
git add .
git commit -m "Update: 描述您的更改"
git push origin main
```

GitHub Pages 会自动重新部署（通常需要 1-2 分钟）。

## 📝 注意事项

1. **仓库名称必须精确匹配**：`bupt-reasoning-lab.github.io`（区分大小写）
2. **分支名称**：确保使用 `main` 分支（GitHub 默认）
3. **文件路径**：确保所有静态资源路径使用相对路径
4. **HTTPS**：GitHub Pages 自动提供 HTTPS，无需额外配置
5. **自定义域名**（可选）：可以在 `Settings > Pages > Custom domain` 中配置

## 🐛 常见问题

### 问题 1: 页面显示 404

- 检查仓库名称是否正确
- 确认 GitHub Pages 已启用
- 等待几分钟让部署完成

### 问题 2: 样式或脚本未加载

- 检查文件路径是否正确（使用相对路径）
- 确认所有文件都已提交到仓库
- 检查浏览器控制台是否有错误

### 问题 3: 图片不显示

- 确认图片文件已上传到仓库
- 检查图片路径是否正确
- 确认图片文件大小不超过 100MB（GitHub 限制）

## 📚 相关链接

- [GitHub Pages 文档](https://docs.github.com/en/pages)
- [三篇论文主页]：
  - [FinanceReasoning](https://bupt-reasoning-lab.github.io/FinanceReasoning/)
  - [FinMMR](https://bupt-reasoning-lab.github.io/FinMMR/)
  - [FinMMDocR](https://bupt-reasoning-lab.github.io/FinMMDocR/)

## ✨ 功能特性

- ✅ 响应式设计，支持移动端和桌面端
- ✅ 现代化的 UI 设计，参考 OpenAI、Anthropic 等公司风格
- ✅ 流畅的动画效果和交互
- ✅ 论文卡片展示，点击可跳转到论文主页
- ✅ 团队成员卡片，可跳转到个人主页
- ✅ 联系方式展示
- ✅ SEO 优化（meta 标签）

---

如有问题，请检查 GitHub Pages 的构建日志或联系维护人员。

