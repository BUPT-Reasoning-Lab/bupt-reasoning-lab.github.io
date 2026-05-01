# 快速开始指南

## 📦 文件位置

所有文件已创建在：`/home/bupt/FinMMR/lab-homepage/`

## 🚀 部署到 GitHub Pages 的快速步骤

### 1. 在 GitHub 创建仓库

访问 GitHub，创建名为 `bupt-reasoning-lab.github.io` 的公开仓库。

### 2. 复制文件到新目录

```bash
cd /home/bupt
mkdir bupt-reasoning-lab.github.io
cp -r FinMMR/lab-homepage/* bupt-reasoning-lab.github.io/
cd bupt-reasoning-lab.github.io
```

### 3. 初始化并推送

```bash
git init
git add .
git commit -m "Initial commit: Add lab homepage"
git remote add origin git@github.com:BUPT-Reasoning-Lab/bupt-reasoning-lab.github.io.git
git branch -M main
git push -u origin main
```

### 4. 启用 GitHub Pages

1. 在 GitHub 仓库页面，进入 `Settings` > `Pages`
2. Source 选择 `Deploy from a branch`
3. Branch 选择 `main`，Folder 选择 `/ (root)`
4. 点击 `Save`

### 5. 等待部署

几分钟后访问：`https://bupt-reasoning-lab.github.io/`

## ✏️ 自定义内容

### 修改论文信息

编辑 `index.html`，找到三个 `.paper-card` 部分，修改：
- 论文标题
- 论文链接（已设置为正确的 GitHub Pages 地址）

如果修改论文描述、标签、按钮等需要中英文切换的文案，请同步更新 `static/data/translations.json`。

### 修改首页重点项目

编辑 `index.html` 的 `#home` 区块，可以修改：
- 重点项目名称、简介、访问按钮和当前访问地址
- Demo 视频播放器
- 正式域名状态说明

如果替换 Demo 视频，请将 `.mp4` 文件放入 `static/videos/`，并更新 `index.html` 中 `<video>` 的 `source` 路径。建议控制视频文件大小，避免影响页面加载。

### 修改团队成员

编辑 `index.html`，找到 `.member-card` 部分，可以：
- 添加更多成员卡片
- 修改成员信息
- 更新个人主页链接

如果成员姓名、角色、简介等内容需要支持中英文切换，请同步更新 `static/data/translations.json`。

### 修改联系方式

编辑 `index.html`，找到 `.contact-card` 部分，更新：
- 邮箱地址
- 实验室地址
- GitHub 链接

## 🎨 添加图片

1. 将图片放入 `static/images/` 目录
2. 更新 `index.html` 中的图片路径
3. 推荐图片：
   - `favicon.png` - 网站图标（32x32 或 64x64）
   - `lab-banner.png` - 社交媒体分享图（1200x630）

## 🌐 维护中英文文案

本项目使用 `data-i18n` 和 `static/data/translations.json` 维护中英文切换。

新增可翻译文案时：

1. 在 `index.html` 中添加唯一的 `data-i18n` key
2. 在 `static/data/translations.json` 的 `zh` 和 `en` 中添加同名 key
3. 使用 HTTP 服务器本地预览，避免浏览器拦截本地 JSON 读取

## 📝 更新内容

修改文件后：

```bash
cd /home/bupt/bupt-reasoning-lab.github.io
git add .
git commit -m "Update: 描述更改"
git push origin main
```

## ⚠️ 重要提示

1. **仓库名称必须精确**：`bupt-reasoning-lab.github.io`（区分大小写）
2. **分支名称**：使用 `main` 分支
3. **文件路径**：所有静态资源使用相对路径（已配置好）
4. **部署时间**：GitHub Pages 通常需要 1-2 分钟完成部署

## 🔍 检查清单

部署前确认：
- [ ] 所有文件已复制到新目录
- [ ] Git 仓库已初始化
- [ ] 远程仓库地址正确
- [ ] 已推送到 GitHub
- [ ] GitHub Pages 已启用
- [ ] 等待部署完成（1-2 分钟）

## 📚 详细文档

- 完整部署指南：查看 [DEPLOYMENT.md](./DEPLOYMENT.md)
- 项目说明：查看 [README.md](./README.md)

---

如有问题，请检查 GitHub Pages 的构建日志。
