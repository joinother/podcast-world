# PodcastWorld · 播客世界

> 🍎 Apple Podcasts 风格的全球播客发现平台，支持 28 种语言、模糊搜索、AI 问答、学习模式。GitHub Pages 托管 + 通行密钥（Passkey）身份验证。

---

## 🚀 一键部署到 GitHub Pages

### 第一步：创建 GitHub 仓库

1. 打开 [github.com/new](https://github.com/new)
2. **Repository name** 填写：`podcast-world`（或其他名字）
3. 选择 **Private**（私有仓库，只有你能访问）
4. ❌ 不要勾选 "Add a README file"（保持空白仓库）
5. 点击 **Create repository**

---

### 第二步：上传 index.html

仓库创建后，你会看到一个空仓库页面。按以下步骤操作：

**方法 A：网页上传（最简单，推荐）**

1. 在空仓库页面，找到 **"uploading an existing file"** 区域
2. 把 `podcast-world/index.html` 文件拖进去
3. 点击 **Commit changes**

**方法 B：命令行上传**

```bash
# 克隆空仓库
git clone https://github.com/你的用户名/podcast-world.git
cd podcast-world

# 把 index.html 复制进去（替换为你的实际路径）
cp /c/Users/11348/WorkBuddy/20260407154016/podcast-world/index.html ./

# 提交并推送
git add index.html
git commit -m "feat: PodcastWorld with Passkey + Favorites"
git branch -M main
git push -u origin main
```

---

### 第三步：开启 GitHub Pages

1. 进入仓库 → 点击 **Settings**（顶部菜单）
2. 左侧菜单找到 **Pages**
3. **Source** 选：**Deploy from a branch**
4. **Branch** 选：**main** → **/ (root)** → 点击 **Save**
5. 等待 1-2 分钟，页面顶部会出现绿条：
   > ✅ Your site is published at **https://你的用户名.github.io/podcast-world/**

---

### 第四步：访问你的播客世界

1. 打开上面的链接
2. **首次使用**：点击「注册 Passkey」，输入一个用户名（如 `me`），按提示完成通行密钥注册
3. **之后访问**：点击「登录」，使用已注册的通行密钥解锁
4. （可选）点击「游客模式」跳过验证本地使用

---

## 🔐 关于通行密钥（Passkey）

| 功能 | 说明 |
|------|------|
| 注册 | 首次使用输入用户名，按浏览器提示创建 Passkey |
| 登录 | 输入用户名 → 生物识别/PIN/密码验证 |
| 存储 | 凭证数据存在你**当前设备**的浏览器 localStorage 中 |
| 设备限制 | 每个设备单独注册，多设备需各自注册 |
| 游客模式 | 不注册直接跳过验证，但数据仅保存在本设备 |

> ⚠️ **重要**：如果清除了浏览器数据或换设备，需要重新注册 Passkey。GitHub Pages 无法帮你管理后端凭证，凭证是与你的浏览器/设备绑定的。

---

## 📁 项目文件说明

```
podcast-world/
└── index.html   ← 整个应用，单文件，包含所有功能
```

所有代码、样式、数据都在这一个文件里，无需任何构建工具或后端服务。

---

## ✨ 功能概览

| 功能 | 状态 |
|------|------|
| 🍎 Apple Podcasts 风格界面 | ✅ |
| 🌐 28 种语言播客分类 | ✅ |
| 🔍 Fuse.js 模糊搜索 | ✅ |
| ❤️ 收藏/收藏夹 | ✅ |
| 🔐 Passkey 通行密钥认证 | ✅ |
| 🎵 播客播放与进度控制 | ✅ |
| 📝 原文 + 中文翻译字幕 | ✅ |
| 🤖 AI 问答（模拟） | ✅ |
| ⬇️ 下载到本地 | ✅ |
| 📊 分类 + 流行度筛选 | ✅ |

---

## 🔧 自定义修改

如果你想修改播客数据，编辑 `index.html` 中 `PODCASTS` 常量数组。每条播客格式：

```javascript
{
  id: "podcast-id",
  title: "播客名称",
  author: "作者",
  lang: "日语",
  langCode: "ja",
  country: "🇯🇵",
  category: "新闻",
  popularity: 4.5,
  description: "描述文字",
  website: "https://...",
  rss: "https://...",
  cover: "https://...",
  episodes: [...]
}
```

---

有任何问题欢迎提 Issue！
