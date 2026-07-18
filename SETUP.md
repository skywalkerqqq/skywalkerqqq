# 🚀 快速部署指南

## 第一步：创建 GitHub Profile 仓库

1. 登录你的 GitHub
2. 创建一个**与你 GitHub 用户名完全相同**的公开仓库
   - 例如：如果你的用户名是 `alice`，就创建 `alice/alice`
3. 勾选 "Add a README file"（如果你还没有的话）

## 第二步：替换占位符

在 `README.md` 中全局搜索替换：

| 占位符 | 替换为 |
|---------|--------|
| `YOUR_USERNAME` | 你的 GitHub 用户名 |
| `YOUR_SPOTIFY_USER` | 你的 Spotify 用户名（不需要可以删除该区块） |
| `Your Name` | 你的真实姓名 |
| `your.email@example.com` | 你的邮箱 |
| `your-portfolio.com` | 你的个人网站 |
| `your-blog.com` | 你的博客地址 |
| 项目名称和链接 | 你自己的项目 |

## 第三步：上传文件

把以下文件推送到你的 profile 仓库：

```
.
├── .github/
│   └── workflows/
│       └── snake.yml          # 自动生成吃豆蛇动画
└── README.md                  # 主页内容
```

## 第四步：启用 Snake 动画

1. 进入仓库 → **Settings** → **Actions** → **General**
2. 确保 Workflow permissions 设置为 **Read and write permissions**
3. 进入 **Actions** 标签页，手动运行一次 "Generate Snake Animation"
4. 运行成功后会在 `output` 分支生成 SVG 文件

## 第五步（可选）：启用 Spotify 卡片

要显示正在听的音乐，需要部署 [novatorem](https://github.com/novatorem/novatorem)：
1. Fork 那个仓库
2. 在 Vercel 上部署（需要 Spotify API 的 Client ID 和 Secret）
3. 把 README 中的 `YOUR_SPOTIFY_USER` 替换为你的 Spotify 用户名

## 主题配色

| 颜色 | 色号 | 用途 |
|------|------|------|
| 霓虹绿 | `#00ff41` | 主色调、标题、高亮 |
| 深黑 | `#0d1117` | 卡片背景 |
| 深蓝黑 | `#1a1a2e` | 徽章背景 |
| 浅灰 | `#c9d1d9` | 正文文字 |
