# Vue 招聘平台 2024

一个基于 Vue 3 + Vite 构建的现代化招聘信息管理平台，提供职位浏览、发布、编辑和删除等完整功能。

![Vue.js](https://img.shields.io/badge/Vue.js-3.5.22-4FC08D?style=flat-square&logo=vue.js)
![Vite](https://img.shields.io/badge/Vite-7.1.11-646CFF?style=flat-square&logo=vite)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.4.18-38B2AC?style=flat-square&logo=tailwind-css)

## ✨ 功能特性

- 🏠 **首页展示** - 精美的首页设计，展示最新职位信息
- 📋 **职位列表** - 浏览所有可用职位，支持分页显示
- 🔍 **职位详情** - 查看职位的完整信息和公司详情
- ➕ **发布职位** - 通过表单发布新的招聘信息
- ✏️ **编辑职位** - 修改已发布的职位信息
- 🗑️ **删除职位** - 移除不再需要的职位
- 🎨 **响应式设计** - 完美适配桌面端和移动端
- 🔔 **消息提示** - 操作成功/失败的即时反馈
- ⚡ **加载动画** - 优雅的数据加载状态展示

## 🛠️ 技术栈

### 核心框架
- **Vue 3.5.22** - 渐进式 JavaScript 框架
- **Vue Router 4.6.3** - 官方路由管理器
- **Vite 7.1.11** - 下一代前端构建工具

### UI 与样式
- **TailwindCSS 3.4.18** - 实用优先的 CSS 框架
- **PrimeIcons 7.0.0** - 丰富的图标库
- **Vue Toastification 2.0.0** - 优雅的消息提示组件
- **Vue Spinner 1.0.4** - 加载动画组件

### 数据与通信
- **Axios 1.13.2** - HTTP 客户端
- **JSON Server 1.0.0** - 模拟 REST API 后端

### 开发工具
- **Vue DevTools 8.0.3** - Vue 开发者工具
- **PostCSS 8.5.6** - CSS 转换工具
- **Autoprefixer 10.4.22** - CSS 自动添加浏览器前缀

## 📋 系统要求

- **Node.js**: ^20.19.0 或 >=22.12.0
- **npm** 或 **yarn** 或 **pnpm**

## 🚀 快速开始

### 1. 克隆项目

```bash
git clone <repository-url>
cd vue-crash-2024
```

### 2. 安装依赖

```bash
npm install
```

### 3. 启动开发服务器

项目需要同时运行前端开发服务器和后端 API 服务器。

#### 终端 1 - 启动前端开发服务器

```bash
npm run dev
```

前端服务将运行在 `http://localhost:3001`

#### 终端 2 - 启动 JSON Server（模拟后端 API）

```bash
npm run server
```

API 服务将运行在 `http://localhost:8000`

### 4. 访问应用

在浏览器中打开 [http://localhost:3001](http://localhost:3001)

## 📁 项目结构

```
vue-crash-2024/
├── public/                 # 静态资源
│   └── favicon.ico
├── src/
│   ├── assets/            # 资源文件
│   │   ├── img/          # 图片资源
│   │   └── main.css      # 全局样式
│   ├── components/        # 可复用组件
│   │   ├── BackButton.vue      # 返回按钮
│   │   ├── Card.vue            # 卡片组件
│   │   ├── Hero.vue            # 首页横幅
│   │   ├── HomeCards.vue       # 首页卡片
│   │   ├── JobListing.vue      # 单个职位卡片
│   │   ├── JobListings.vue     # 职位列表
│   │   └── Navbar.vue          # 导航栏
│   ├── router/            # 路由配置
│   │   └── index.js
│   ├── views/             # 页面视图
│   │   ├── HomeView.vue        # 首页
│   │   ├── JobsView.vue        # 职位列表页
│   │   ├── JobView.vue         # 职位详情页
│   │   ├── AddJobView.vue      # 添加职位页
│   │   ├── EditJobView.vue     # 编辑职位页
│   │   └── NotFoundView.vue    # 404 页面
│   ├── App.vue            # 根组件
│   ├── main.js            # 应用入口
│   └── jobs.json          # 职位数据（JSON Server 数据源）
├── _theme_files/          # 主题静态文件
├── index.html             # HTML 入口
├── vite.config.js         # Vite 配置
├── tailwind.config.js     # TailwindCSS 配置
├── postcss.config.js      # PostCSS 配置
├── jsconfig.json          # JavaScript 配置
└── package.json           # 项目依赖
```

## 🔧 可用脚本

```bash
# 启动开发服务器（前端）
npm run dev

# 启动 JSON Server（后端 API）
npm run server

# 构建生产版本
npm run build

# 预览生产构建
npm run preview
```

## 🌐 路由配置

| 路径 | 组件 | 说明 |
|------|------|------|
| `/` | HomeView | 首页 |
| `/jobs` | JobsView | 职位列表页 |
| `/jobs/add` | AddJobView | 添加职位页 |
| `/jobs/:id` | JobView | 职位详情页 |
| `/jobs/edit/:id` | EditJobView | 编辑职位页 |
| `*` | NotFoundView | 404 页面 |

## 🔌 API 端点

JSON Server 提供以下 REST API 端点：

- `GET /api/jobs` - 获取所有职位
- `GET /api/jobs/:id` - 获取单个职位详情
- `POST /api/jobs` - 创建新职位
- `PUT /api/jobs/:id` - 更新职位信息
- `DELETE /api/jobs/:id` - 删除职位

> **注意**: Vite 配置了代理，将 `/api` 请求转发到 `http://localhost:8000`

## 🎨 样式说明

项目使用 TailwindCSS 进行样式开发，主要配色方案：

- **主色调**: 绿色 (`green-500`, `green-600`)
- **辅助色**: 蓝色 (`blue-50`)
- **中性色**: 灰色系列
- **强调色**: 黑色用于按钮和导航

## 📦 构建部署

### 构建生产版本

```bash
npm run build
```

构建产物将生成在 `dist/` 目录中。

### 预览生产构建

```bash
npm run preview
```

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📝 开发注意事项

1. **路径别名**: 项目配置了 `@` 别名指向 `src` 目录
2. **API 代理**: 开发环境下 `/api` 请求会被代理到 `http://localhost:8000`
3. **端口配置**: 前端默认端口 `3001`，后端 API 端口 `8000`
4. **数据持久化**: 修改 `src/jobs.json` 文件会自动更新 API 数据

## 📄 许可证

本项目仅供学习和参考使用。

## 👨‍💻 作者

Draky

---

**Happy Coding! 🎉**
