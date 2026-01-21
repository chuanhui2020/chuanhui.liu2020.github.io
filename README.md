# CV 网站

这是一个基于 Vue3 + Vite + Tailwind CSS 构建的现代化个人简历网站。

## 功能特性

- 📱 响应式设计，支持移动端和桌面端
- 🌓 深色/浅色主题切换
- ⚡ 基于 Vite 的快速开发体验
- 🎨 使用 Tailwind CSS 的现代化 UI
- 🚀 自动部署到 GitHub Pages

## 本地开发

### 安装依赖
```bash
npm install
```

### 启动开发服务器
```bash
npm run dev
```

访问 http://localhost:5173 查看网站

### 构建生产版本
```bash
npm run build
```

### 预览生产版本
```bash
npm run preview
```

## 自定义内容

编辑以下文件来自定义你的简历内容：

- `src/components/Hero.vue` - 首页信息（姓名、职位、简介、社交链接）
- `src/components/Experience.vue` - 工作经历
- `src/components/Projects.vue` - 项目展示
- `src/components/Skills.vue` - 技能专长
- `src/components/Contact.vue` - 联系方式

## 部署

推送代码到 `main` 分支后，GitHub Actions 会自动构建并部署到 GitHub Pages。

首次部署需要在仓库设置中启用 GitHub Pages：
1. 进入仓库的 Settings > Pages
2. Source 选择 "GitHub Actions"
3. 等待部署完成后访问 https://chuanhui.liu2020.github.io

## 技术栈

- Vue 3 - 渐进式 JavaScript 框架
- Vite - 下一代前端构建工具
- Tailwind CSS - 实用优先的 CSS 框架
- GitHub Pages - 静态网站托管
