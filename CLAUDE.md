# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在此代码库中工作时提供指导。

## 仓库概述

这是一个基于 Vue3 + Vite + Tailwind CSS 构建的现代化个人简历网站，托管在 GitHub Pages 上。网站访问地址为 `https://chuanhui.liu2020.github.io`。

## 技术栈

- **Vue 3**: 渐进式 JavaScript 框架，使用 Composition API
- **Vite**: 下一代前端构建工具，提供快速的开发体验
- **Tailwind CSS**: 实用优先的 CSS 框架
- **GitHub Actions**: 自动化构建和部署

## 常用命令

### 开发
```bash
npm install          # 安装依赖
npm run dev          # 启动开发服务器 (http://localhost:5173)
npm run build        # 构建生产版本
npm run preview      # 预览生产版本
```

## 项目架构

### 目录结构
```
src/
├── components/      # Vue 组件
│   ├── Navbar.vue      # 导航栏（包含深色模式切换）
│   ├── Hero.vue        # 首页/关于我
│   ├── Experience.vue  # 工作经历
│   ├── Projects.vue    # 项目展示
│   ├── Skills.vue      # 技能专长
│   └── Contact.vue     # 联系方式
├── App.vue          # 根组件（深色模式状态管理）
├── main.js          # 应用入口
└── style.css        # Tailwind CSS 配置
```

### 核心功能

1. **深色模式**:
   - 状态管理在 `App.vue` 中
   - 使用 `localStorage` 持久化主题设置
   - 支持系统主题偏好检测
   - Tailwind 的 `dark:` 类实现样式切换

2. **响应式设计**:
   - 使用 Tailwind 的响应式工具类 (`sm:`, `md:`, `lg:`)
   - 移动优先设计理念

3. **平滑滚动**:
   - 导航栏点击平滑滚动到对应section
   - 使用 `scrollIntoView` API

### 自定义内容

修改以下组件中的数据对象来更新简历内容：

- `Hero.vue` 中的 `personalInfo` - 个人信息和社交链接
- `Experience.vue` 中的 `experiences` - 工作经历数组
- `Projects.vue` 中的 `projects` - 项目列表
- `Skills.vue` 中的 `skillCategories` - 技能分类和等级
- `Contact.vue` 中的 `contactInfo` - 联系方式

## 部署

### GitHub Pages 自动部署

推送到 `main` 分支会触发 GitHub Actions workflow (`.github/workflows/deploy.yml`)：
1. 安装依赖
2. 构建项目 (`npm run build`)
3. 将 `dist/` 目录部署到 GitHub Pages

### 首次部署设置

1. 进入仓库的 **Settings** > **Pages**
2. **Source** 选择 "GitHub Actions"
3. 推送代码后等待 workflow 完成
4. 访问 https://chuanhui.liu2020.github.io

## 注意事项

- Vite base 路径已配置为 `/`（适用于 username.github.io 仓库）
- 深色模式偏好存储在 localStorage 的 `theme` 键中
- 所有组件都使用 `<script setup>` 语法（Vue 3 Composition API）
