# 新员工培训策划助手 · 静态网站部署包

**中国医学论坛报 · 人力发展中心**
基于 2022–2025 年历年培训资料构建

---

## 文件说明

```
deploy/
├── index.html        ← 应用主文件（单页面，无外部依赖）
├── vercel.json       ← Vercel 部署配置
├── netlify.toml      ← Netlify 部署配置
└── README.md         ← 本说明文档
```

---

## 快速访问（本地）

直接用浏览器打开 `index.html` 即可使用，**无需安装任何软件，无需联网**。

---

## 部署到公网（三选一）

### 方案一：Vercel（推荐，国内访问流畅）

1. 注册 / 登录 [vercel.com](https://vercel.com)
2. 点击 **Add New → Project**
3. 选择 **"Upload"**，将 `deploy/` 文件夹整个拖入
4. 点击 **Deploy**，约 30 秒即可上线
5. 获得形如 `https://cmt-training-assistant.vercel.app` 的公网地址

> 如果关联了 GitHub 仓库，每次推送代码会自动重新部署。

---

### 方案二：Netlify（操作最简单）

1. 打开 [app.netlify.com/drop](https://app.netlify.com/drop)
2. **直接把 `deploy/` 文件夹拖拽进页面**
3. 等待几秒，自动完成部署
4. 点击生成的链接即可访问

---

### 方案三：GitHub Pages（免费，需要 GitHub 账号）

1. 在 GitHub 创建一个新仓库（Public）
2. 将 `deploy/` 目录下的所有文件上传到仓库根目录
3. 进入仓库 **Settings → Pages**
4. Source 选择 `main` 分支 / `/ (root)` 目录
5. 保存后等待 1-2 分钟，访问 `https://<用户名>.github.io/<仓库名>/`

---

### 方案四：腾讯云 EdgeOne Pages（国内访问最快）

1. 登录 [腾讯云控制台](https://console.cloud.tencent.com/edgeone/pages)
2. 进入 **EdgeOne Pages → 创建项目**
3. 选择 **上传本地文件夹**，选择 `deploy/` 文件夹
4. 部署完成后获得 `.edgeone.app` 域名

---

## 功能模块

| Tab | 功能 | 说明 |
|-----|------|------|
| 🔍 每周创意雷达 | 全网培训趋势聚合 | 展示8大平台创意培训形式，含历年CMT参照 |
| 💡 生成培训主题 | 智能主题方案生成 | 按年份/岗位/关键词/模块生成5套定制方案 |
| 📣 培训通知文案 | 一键生成正式通知 | 支持4种风格，自动填充关键信息 |
| 🎨 培训物料生成 | 海报预览+视频脚本 | 含4种配色实时海报预览+5类视频分镜脚本 |

---

## 技术说明

- **纯静态单文件**：所有代码内嵌于 `index.html`，无外部 CDN / API 依赖
- **离线可用**：下载后断网也可正常使用所有功能
- **兼容性**：支持 Chrome / Edge / Firefox / Safari（2020年以后版本）
- **移动端适配**：响应式布局，支持平板和手机访问

---

## 数据更新

所有培训历史数据和主题模板内嵌于 `index.html` 的 JavaScript 数组中：

- `CMT_HISTORY` — 2022–2025年历年培训记录（第1060行附近）
- `TREND_TEMPLATES` — 全网趋势主题模板（第1110行附近）
- `THEME_POOLS` — 培训主题方案池（第1169行附近）

如需添加 2026 年及以后的培训记录，直接编辑 `index.html` 对应数组即可。

---

*中国医学论坛报 · 人力发展中心 · 2026*
